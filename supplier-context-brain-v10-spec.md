# SUPPLIER CONTEXT BRAIN V10 - PRODUCTION SPECIFICATION
## Complete System Architecture for Code Generation

---

## 🧠 EXECUTIVE SUMMARY

**The Brain File** defines:
1. **Database Schema** (what we store)
2. **API Endpoints** (what the backend exposes)
3. **UI Components** (what suppliers see)
4. **Data Flows** (how data moves through system)
5. **Automation Logic** (24h refresh, feedback processing, score optimization)

---

# SECTION 1: DATABASE SCHEMA
## PostgreSQL/Firestore Tables & Relationships

### **TABLE 1: `suppliers`**

```sql
CREATE TABLE suppliers (
  id TEXT PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  company_name TEXT NOT NULL,
  
  -- From signup
  mov_value DECIMAL,           -- Minimum Order Value
  aov_value DECIMAL,           -- Average Order Value
  geographic_focus TEXT,       -- 'single_state' | 'regional' | 'national'
  focus_state TEXT,            -- Home state code (e.g., 'NJ')
  
  -- Deduced from public data
  estimated_revenue DECIMAL,   -- From D&B
  employee_count INTEGER,      -- From LinkedIn
  years_in_business INTEGER,   -- From SoS
  
  -- Tier assignment
  assigned_tier TEXT,          -- 'Tier1' | 'Tier2' | 'Tier3' | 'Tier4'
  monthly_price DECIMAL,       -- $199 | $399 | $699 | $999
  
  -- Subscription
  subscription_active BOOLEAN,
  subscription_start_date TIMESTAMP,
  subscription_end_date TIMESTAMP,
  
  -- Preferences
  competitor_focus TEXT ARRAY, -- ['Competitor A', 'Competitor B']
  industry TEXT,               -- 'e-commerce' | 'manufacturing' | etc.
  
  -- Engagement
  last_login TIMESTAMP,
  feedback_cards_submitted INTEGER DEFAULT 0,
  
  created_at TIMESTAMP,
  updated_at TIMESTAMP
);
```

---

### **TABLE 2: `buyers`**

```sql
CREATE TABLE buyers (
  id TEXT PRIMARY KEY,
  supplier_id TEXT NOT NULL,   -- FK to suppliers
  
  -- Core info
  company_name TEXT NOT NULL,
  ein TEXT UNIQUE,             -- Federal tax ID
  website TEXT,
  phone TEXT,
  primary_contact_name TEXT,
  primary_contact_email TEXT,
  
  -- Classification
  buyer_tier TEXT,             -- 'Tier A' | 'Tier B' | 'Tier C' | 'Tier D'
  industry TEXT,
  facility_type TEXT,          -- 'Manufacturing' | 'Warehouse' | 'Retail' | 'Mixed'
  facility_size_sqft INTEGER,
  annual_revenue DECIMAL,
  employee_count INTEGER,
  
  -- Urgency metadata
  urgency_score DECIMAL,       -- 0-100
  urgency_label TEXT,          -- 'Aggressive' | 'Responsive' | etc.
  urgency_score_range TEXT,    -- '75-78' (min-max for label)
  last_score_date TIMESTAMP,
  decay_half_life_days INTEGER,-- Determined by tier
  
  -- Tracking
  is_watched BOOLEAN DEFAULT FALSE,
  is_competitor_buyer BOOLEAN DEFAULT FALSE,
  competitor_name TEXT,        -- Which competitor supplies them
  competitor_review_score DECIMAL,
  competitor_pain_point TEXT,  -- 'Late shipping' | 'Price increase' | etc.
  
  -- Action tracking
  supplier_contacted_date TIMESTAMP,
  deal_closed_date TIMESTAMP,
  deal_amount DECIMAL,
  
  created_at TIMESTAMP,
  updated_at TIMESTAMP
);
```

---

### **TABLE 3: `signals`**

```sql
CREATE TABLE signals (
  id TEXT PRIMARY KEY,
  buyer_id TEXT NOT NULL,      -- FK to buyers
  
  -- Signal metadata
  signal_type TEXT NOT NULL,   -- 'permit' | 'hiring' | 'revenue_spike' | etc.
  signal_source TEXT NOT NULL, -- 'government' | 'linkedin' | 'marketplace' | etc.
  
  -- Raw signal
  signal_value TEXT,           -- Raw data: "Building expansion permit"
  signal_points DECIMAL,       -- Raw score before decay: +9
  signal_date TIMESTAMP,       -- When signal occurred
  
  -- Current state
  current_points DECIMAL,      -- Score after decay applied
  days_old INTEGER,            -- How old is this signal
  last_decay_calc TIMESTAMP,
  
  -- Metadata
  confidence_level DECIMAL,    -- 0.0-1.0 (50% = unconfirmed, 100% = verified)
  data_source_api TEXT,        -- Which API provided this data
  raw_data_json JSONB,         -- Full raw data for drill-down
  
  is_active BOOLEAN DEFAULT TRUE,
  expires_date TIMESTAMP,      -- When signal becomes negligible
  
  created_at TIMESTAMP,
  updated_at TIMESTAMP
);
```

---

### **TABLE 4: `scores_history`**

```sql
CREATE TABLE scores_history (
  id TEXT PRIMARY KEY,
  buyer_id TEXT NOT NULL,
  supplier_id TEXT NOT NULL,
  
  -- Score snapshot
  urgency_score DECIMAL,
  urgency_label TEXT,
  score_components JSONB,      -- {'government': 25, 'financial': 15, 'platform': 20, 'compliance': 12}
  multiplier_applied DECIMAL,  -- Competitor multiplier: 1.0, 1.5, 1.8, 2.0
  
  -- Signals active at time of scoring
  active_signals_count INTEGER,
  top_signals JSONB,           -- Array of top 5 signals contributing to score
  
  -- Red flags
  red_flags JSONB ARRAY,       -- ['IRS Tax Lien']
  signal_conflicts JSONB ARRAY,-- ['Expansion permit + Tax lien']
  
  calculated_at TIMESTAMP,
  
  created_at TIMESTAMP
);
```

---

### **TABLE 5: `feedback_cards`**

```sql
CREATE TABLE feedback_cards (
  id TEXT PRIMARY KEY,
  supplier_id TEXT NOT NULL,
  buyer_id TEXT NOT NULL,
  
  -- Question responses
  q1_closed_deal BOOLEAN,      -- "Did you close this deal?"
  q2_why_not TEXT,             -- "If NO, why?" (dropdown value)
  q3_timing TEXT,              -- "How was timing?" ('too_early' | 'perfect' | 'too_late')
  q4_want_more BOOLEAN,        -- "Want more like this?"
  q5_feedback TEXT,            -- "Any other feedback?" (free text)
  
  -- Context
  original_urgency_score DECIMAL,
  original_urgency_label TEXT,
  buyer_tier_at_time TEXT,
  
  submitted_at TIMESTAMP,
  days_between_lead_and_feedback INTEGER,
  
  created_at TIMESTAMP
);
```

---

### **TABLE 6: `feedback_analysis`**

```sql
CREATE TABLE feedback_analysis (
  id TEXT PRIMARY KEY,
  supplier_id TEXT NOT NULL,
  
  -- Metrics
  total_feedback_cards INTEGER,
  close_rate_percent DECIMAL,
  average_days_to_close INTEGER,
  
  -- By urgency label
  aggressive_close_rate DECIMAL,
  responsive_close_rate DECIMAL,
  steady_close_rate DECIMAL,
  
  -- By buyer tier
  tier_a_success DECIMAL,
  tier_b_success DECIMAL,
  tier_c_success DECIMAL,
  tier_d_success DECIMAL,
  
  -- Feedback reasons
  most_common_objection TEXT,  -- 'Already has supplier' | 'Price too high' | etc.
  timing_accuracy_percent DECIMAL,
  
  -- Optimization recommendations
  recommended_signal_weight_changes JSONB,
  recommended_buyer_volume_adjustment INTEGER,
  
  analysis_date TIMESTAMP,
  next_analysis_date TIMESTAMP,
  
  created_at TIMESTAMP
);
```

---

### **TABLE 7: `building_by_building_scans`**

```sql
CREATE TABLE building_by_building_scans (
  id TEXT PRIMARY KEY,
  supplier_id TEXT NOT NULL,
  
  -- Scope
  city TEXT,
  state TEXT,
  zip_codes TEXT ARRAY,
  
  -- Results
  total_buildings_scanned INTEGER,
  total_potential_buyers INTEGER,
  verified_buyers INTEGER,
  
  -- SAM Analysis
  estimated_addressable_market DECIMAL,
  percent_saturated DECIMAL,   -- "You can reach X% of your SAM"
  
  -- Buyer breakdown
  buyers_by_tier JSONB,        -- {'Tier A': 5, 'Tier B': 12, 'Tier C': 45, 'Tier D': 200}
  buyers_by_industry JSONB,
  
  -- Data freshness
  last_scan_date TIMESTAMP,
  next_rescan_date TIMESTAMP,
  
  created_at TIMESTAMP
);
```

---

# SECTION 2: API ENDPOINTS
## What the Backend Exposes (REST)

### **AUTHENTICATION**

```
POST /auth/signup
Body: { email, password, company_name, mov, aov, geographic_focus }
Response: { supplier_id, auth_token, tier, pricing }

POST /auth/login
Body: { email, password }
Response: { auth_token, supplier_id, tier, subscription_status }
```

---

### **BUYER DISCOVERY**

```
GET /buyers?limit=50&urgency_min=70&sort_by=urgency_desc
Response: [
  {
    id: "buyer-123",
    company_name: "Widget Corp",
    urgency_label: "Aggressive",
    urgency_score: 76,
    urgency_range: "75-78",
    primary_signal: "Building expansion permit",
    buyer_tier: "Tier C",
    facility_size: 50000,
    competitor_threat: "Competitor Y (1-star review)",
    red_flags: [],
    signal_conflicts: [],
    last_updated: "2025-12-23T00:00:00Z",
    next_rescore: "2025-12-24T00:00:00Z"
  }
]

GET /buyers/:id/full-intelligence
Response: Full buyer profile with all signals, red flags, competitor intel, etc.

GET /buyers/:id/why-aggressive
Response: Detailed explanation of urgency score (tooltip data)
```

---

### **COMPETITOR INTELLIGENCE** (Tier 2+ only)

```
GET /competitors/buyers?competitor_name="Competitor Y"
Response: List of all buyers using Competitor Y

GET /competitors/:id/threat-level
Response: { threat_level: "high", reason: "Recent 1-star review", likelihood_to_switch: 0.85 }

GET /competitors/map
Response: Visualization data for competitor mapping dashboard
```

---

### **BUILDING-BY-BUILDING** (Tier 3+ only)

```
GET /sam/city/:state/:city
Response: {
  total_potential_buyers: 1250,
  verified_buyers: 892,
  estimated_sam: "$45M annual revenue",
  buyers_by_tier: { A: 5, B: 18, C: 120, D: 749 },
  coverage_percent: 71
}

GET /sam/buildings?state=NJ&city=Newark&filter_by_size=50000+
Response: List of buildings matching criteria (for drill-down)

POST /sam/unlock-city
Body: { state, city }
Response: { success: true, unlock_type: 'referral' | 'purchase', expiry_date }
```

---

### **FEEDBACK COLLECTION**

```
POST /feedback/submit-card
Body: {
  buyer_id: "buyer-123",
  q1_closed_deal: false,
  q2_why_not: "Already has supplier",
  q3_timing: "too_early",
  q4_want_more: true,
  q5_feedback: "Great intel, just wrong timing"
}
Response: { success: true, message: "Thanks for the feedback!" }

GET /feedback/my-analysis
Response: {
  total_cards: 42,
  close_rate: 0.52,
  aggressive_close_rate: 0.68,
  recommended_changes: {...}
}
```

---

### **ACCOUNT & SUBSCRIPTION**

```
GET /account/me
Response: { supplier_id, email, company, tier, pricing, subscription_status }

POST /account/upgrade-tier
Body: { target_tier: "Tier2" }
Response: { success: true, new_price: 399, trial_days: 7 }

GET /account/referrals
Response: { referrals_made: 3, rewards_earned: ['Free month Tier 2', ...] }
```

---

# SECTION 3: UI COMPONENTS (Frontend)

### **MAIN DASHBOARD**

```
Layout:

┌─────────────────────────────────────────┐
│ Supplier Intelligence Platform          │ [Account] [Help]
├─────────────────────────────────────────┤
│                                         │
│ Welcome, [Company Name]!                │
│ Tier: [Tier 2]  |  Buyers Found: 892   │
│                                         │
│ ┌─────────────────────────────────┐   │
│ │ 🔴 URGENT (13 new)              │   │
│ │ ┌─────────────────────────────┐ │   │
│ │ │ Widget Corp                 │ │   │
│ │ │ Urgency: Aggressive (76)    │ │   │
│ │ │ [?] Why Aggressive?         │ │   │
│ │ │ Signal: Building permit     │ │   │
│ │ │ Competitor: Comp Y (review) │ │   │
│ │ │ [View Full Details]         │ │   │
│ │ └─────────────────────────────┘ │   │
│ └─────────────────────────────────┘   │
│                                         │
│ ┌─────────────────────────────────┐   │
│ │ 🟡 RESPONSIVE (42 updated)      │   │
│ │ [View List]                     │   │
│ └─────────────────────────────────┘   │
│                                         │
│ [Upgrade to Competitors' Intel] ➜      │
│ [Unlock Building-by-Building] ➜        │
│                                         │
└─────────────────────────────────────────┘
```

---

### **BUYER DETAIL CARD**

```
┌──────────────────────────────────────────┐
│ Widget Corp                       [Close]│
├──────────────────────────────────────────┤
│                                          │
│ 🎯 URGENCY SCORE: Aggressive (75-78)    │
│    [?] Explain why                      │
│                                          │
│ COMPANY INFO                             │
│ └─ Location: Newark, NJ                 │
│ └─ Facility: 50,000 sqft manufacturing  │
│ └─ Est. Revenue: $2.3M                  │
│ └─ Employees: 28                        │
│                                          │
│ TOP SIGNALS (Updated Yesterday)          │
│ ✅ Building expansion permit (+9 pts)    │
│    [7 days old, 50% strength]            │
│    [?] Why this matters                 │
│                                          │
│ ✅ LinkedIn hiring spree (+7 pts)        │
│    [4 days old, 60% strength]            │
│    [?] Why this matters                 │
│                                          │
│ ✅ Marketplace sales surge (+8 pts)      │
│    [2 days old, 90% strength]            │
│    [?] Why this matters                 │
│                                          │
│ COMPETITOR INTEL (Tier 2+ Feature)       │
│ 📌 Competitor Y supplies them            │
│    Recent 1-star review: "Late shipping" │
│    Likelihood to switch: 85%             │
│                                          │
│ RED FLAGS                                │
│ ⚠️ None                                  │
│                                          │
│ [👥 View Full Intelligence] [📋 Report]
│ [✉️ Send to Email] [📌 Save] [☎️ Call]  │
│                                          │
└──────────────────────────────────────────┘
```

---

### **FEEDBACK CARD (Post-Outreach)**

```
┌─────────────────────────────────────────┐
│ FEEDBACK: Widget Corp (2 weeks ago)     │
├─────────────────────────────────────────┤
│                                         │
│ Q1: Did you close this deal?            │
│     ⭕ Yes  ⭕ No (selected)            │
│                                         │
│ Q2: If NO, why?                         │
│     ✓ Already has supplier              │
│     □ Not ready to buy                  │
│     □ Price too high                    │
│     □ Wrong contact                     │
│     □ Other                             │
│                                         │
│ Q3: Was the timing...?                  │
│     □ Too early    □ Perfect  ✓ Too late│
│                                         │
│ Q4: Want more leads like this?          │
│     ✓ Yes  □ No                         │
│                                         │
│ Q5: Any other feedback?                 │
│     [Free text box]                     │
│     "Great intel but they just signed   │
│      a 2-year contract last month"      │
│                                         │
│ [Submit Feedback] [Cancel]              │
│                                         │
│ 💡 This helps us improve your leads!    │
│                                         │
└─────────────────────────────────────────┘
```

---

# SECTION 4: DATA FLOWS
## Complete Process From Signal to Score to Display

### **DAILY REFRESH FLOW (24-hour cycle)**

```
┌─ Cloud Functions Triggered (Midnight UTC)
│
├─ For each supplier:
│  ├─ Fetch all active buyers (supplier_id matches)
│  │
│  └─ For each buyer:
│     ├─ FETCH new signals from APIs
│     │  ├─ Secretary of State (updates)
│     │  ├─ Building permits (new)
│     │  ├─ LinkedIn API (job postings)
│     │  ├─ News APIs (mentions)
│     │  ├─ D&B updates
│     │  └─ Government records (liens, etc.)
│     │
│     ├─ DETECT new signals
│     │  └─ If new signal found:
│     │     └─ Create signal record
│     │     └─ Set initial points
│     │     └─ Reset decay timer
│     │
│     ├─ APPLY decay to existing signals
│     │  └─ For each signal:
│     │     ├─ Calculate days old
│     │     ├─ Look up half-life (from buyer_tier)
│     │     ├─ Apply formula: score × (0.5)^(t/half_life)
│     │     └─ Update current_points
│     │
│     ├─ RECALCULATE urgency score
│     │  ├─ Sum all active signals
│     │  ├─ Weight by category (Gov 35%, Fin 20%, etc.)
│     │  ├─ Check for red flags (IRS lien?)
│     │  ├─ Apply competitor multipliers
│     │  └─ Generate final score (0-100)
│     │
│     ├─ MAP to word label
│     │  └─ Based on score & buyer_tier:
│     │     ├─ Tier A: 80+ = "Strategic"
│     │     ├─ Tier B/C/D: 75+ = "Aggressive"
│     │     └─ etc.
│     │
│     ├─ STORE score snapshot
│     │  └─ Insert into scores_history table
│     │
│     └─ CHECK for significant change
│        └─ If score jumped (>10 points):
│           └─ Send notification email
│
└─ Repeat for all suppliers & buyers
```

---

### **FEEDBACK PROCESSING FLOW (Weekly)**

```
┌─ Scheduled job runs (Every Sunday)
│
├─ For each supplier with feedback cards:
│  ├─ Query all submitted feedback_cards (last 7 days)
│  │
│  ├─ ANALYZE patterns
│  │  ├─ Count close_rate = closed_deals / total_cards
│  │  ├─ Group by urgency_label
│  │  │  ├─ "Aggressive" leads: X% close rate
│  │  │  ├─ "Responsive" leads: Y% close rate
│  │  │  └─ etc.
│  │  ├─ Group by buyer_tier
│  │  │  ├─ Tier A leads: Z% close rate
│  │  │  └─ etc.
│  │  └─ Most common objection (from q2_why_not)
│  │
│  ├─ GENERATE recommendations
│  │  ├─ "Your 'Aggressive' leads close at 68%"
│  │  ├─ "Your Tier A buyers convert 80%"
│  │  ├─ "Most lose due to timing (too early)"
│  │  └─ "Consider lowering 'Responsive' threshold"
│  │
│  ├─ GENERATE weight adjustments
│  │  └─ If pattern emerges:
│  │     └─ Increase hiring signal weight from +7 to +8
│  │     └─ Decrease permit weight from +9 to +7
│  │
│  ├─ STORE analysis
│  │  └─ Insert into feedback_analysis table
│  │
│  └─ SEND optimization email
│     └─ "Here's how we're personalizing your intelligence..."
│
└─ A/B TEST new weights
   ├─ 50% of suppliers see old weights
   ├─ 50% see new weights
   └─ Track improvement in close rates
```

---

# SECTION 5: ERROR HANDLING

### **SCENARIO: API Failure (NewsAPI down)**

```
Detected: NewsAPI 503 error

Action:
├─ Log error
├─ Use cached data from 24h ago
├─ Mark signal confidence as 75% (down from 100%)
├─ Update buyer record:
│  └─ data_last_confirmed_at = 24h ago
├─ Schedule retry in 6 hours
└─ No impact to score (uses previous state)

User sees: "News data may be 1 day old (API delay)"
```

### **SCENARIO: Missing Data (No D&B record)**

```
Detected: D&B lookup returned no company match

Action:
├─ Don't add signal
├─ Flag confidence as 0% for D&B signals
├─ Try alternate lookup method
│  └─ Search by EIN instead of company name
├─ If still no match:
│  └─ Use estimated values from other sources
│  └─ Mark as "unconfirmed"
└─ Reduce urgency score by 5-10 points

User sees: "Financial data unavailable - confidence reduced"
```

### **SCENARIO: Conflicting Data (Bankrupt but hiring)**

```
Detected: 
├─ Bankruptcy filing detected
├─ BUT also 8 new LinkedIn job postings
├─ AND building permit issued

Action:
├─ Show ALL signals (no filtering)
├─ Flag as "signal conflict" (not red flag)
├─ Use most recent signal for scoring
│  └─ Permit is more recent than bankruptcy
│  └─ Use permit score (+9)
├─ Add note: "Company may be restructuring"
└─ Increase confidence check

User sees: "⚠️ Note: Bankruptcy doesn't invalidate growth signals"
```

---

# SECTION 6: PRODUCTION CHECKLIST

- [ ] All database tables created & indexed
- [ ] Foreign key relationships enforced
- [ ] API endpoints coded and tested
- [ ] Authentication (JWT tokens) working
- [ ] Daily refresh Cloud Function scheduled
- [ ] Weekly feedback analysis job scheduled
- [ ] Decay formula working for all tiers
- [ ] Multiplier logic (competitor intel) tested
- [ ] Red flag detection (IRS lien) working
- [ ] UI components rendering
- [ ] Feedback card collection active
- [ ] Email notifications sending
- [ ] Error handling for all API failures
- [ ] Caching strategy implemented (24h)
- [ ] Logging & monitoring active
- [ ] Load testing passed (500 suppliers, 100K buyers)

---

# STATUS: 🟢 READY FOR CLAUDE AI CODE GENERATION

**All data models defined. All endpoints specified. All flows documented.**

**Ready to code.**
