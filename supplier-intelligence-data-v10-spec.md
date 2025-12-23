# SUPPLIER INTELLIGENCE DATA V10 - PRODUCTION SPECIFICATION
## Complete Signal Scoring System & Data Architecture

---

## 📊 EXECUTIVE SUMMARY

**The Intelligence System** turns raw public data into actionable signals.

**The Process:**
1. **COLLECT** raw data from 6+ APIs
2. **DETECT** patterns (signal types)
3. **SCORE** each signal (0-100 points)
4. **APPLY** decay (age reduces score)
5. **COMBINE** all signals (weighted sum)
6. **LABEL** as word ("Aggressive", "Responsive", etc.)
7. **STORE** score snapshot (for analytics)
8. **DISPLAY** to supplier with context

---

# SECTION 1: DATA SOURCES
## Complete List of Public APIs & Data Feeds

### **TIER 1: GOVERNMENT DATA (Foundation)**

#### **A. Secretary of State Registrations**
```
API: State-specific APIs (varies by state)
Data: Company registrations, filing dates, status changes

Signals Available:
├─ New business registration (+2 pts)
├─ Change of address (+1 pt, could indicate relocation)
├─ Officer changes (+1 pt, leadership transition)
├─ Status changes (active, inactive, dissolved, etc.)
└─ Annual renewal (indicator of active business)

Cost: $2-5/month per supplier (bulk API)
Refresh Rate: 24-48 hours
Confidence: 95%+ (official government data)
```

#### **B. Building Permits & Property Records**
```
API: County APIs + SmartyStreets + DataLogix
Data: Property permits, zoning, facility size, expansions

Signals Available:
├─ Building expansion permit (+9 pts, VERY STRONG)
├─ Facility upgrade (+6 pts)
├─ New equipment permits (+5 pts)
├─ Zoning variance request (+3 pts, growth planning)
├─ Square footage increase (+7 pts, direct expansion)
└─ Property tax increase (+2 pts, higher valuation)

Cost: $15/month per supplier
Refresh Rate: 48-72 hours (varies by county)
Confidence: 90% (permitting lag varies)

Why Powerful:
"If they're expanding their facility, they need packaging supplies.
This is concrete evidence of growth."
```

#### **C. PACER (Court Records)**
```
API: PACER.gov (public, costs $0.10 per page)
Data: Bankruptcy filings, liens, lawsuits

Signals Available (RED FLAGS - NEGATIVE):
├─ IRS tax lien filed (-20 pts, CRITICAL WARNING)
├─ Bankruptcy chapter 11 (-15 pts, restructuring)
├─ Bankruptcy chapter 7 (-25 pts, LIQUIDATION - avoid)
├─ Judgment against company (-10 pts)
├─ Contractor lien (-5 pts, payment disputes)
└─ Lawsuit filed (-3 pts, operational stress)

Cost: $0.10 per page (pay-as-you-go, minimal)
Refresh Rate: 72-96 hours (court system lag)
Confidence: 100% (official court data)

Why Important:
"Don't waste time selling to companies in bankruptcy.
These are red flags, not deal-stoppers, but critical for timing."
```

---

### **TIER 2: FINANCIAL DATA (Confidence)**

#### **D. Dun & Bradstreet (D&B)**
```
API: D&B Bulk API
Data: Business financials, credit, employee count, growth

Signals Available:
├─ Revenue growth YoY (+8 pts per 10% growth)
├─ New loan taken (+6 pts, capital for expansion)
├─ Credit score increase (+3 pts, improving health)
├─ Employee count increase (+7 pts, hiring = growth)
├─ New facility opened (+9 pts, expansion)
├─ PAYDEX score >75 (+2 pts, reliable payer)
└─ Payment days trending down (+3 pts, healthier cash flow)

Cost: $20/month for bulk supplier access
Refresh Rate: 30-60 days (financial lag)
Confidence: 85% (1-2 month delay in reporting)

Why Valuable:
"D&B employee count is often more accurate than LinkedIn.
Revenue growth = budget for packaging.
PayDEX score = will they actually pay us?"
```

---

### **TIER 3: MARKETPLACE & PLATFORM DATA (Real-Time)**

#### **E. LinkedIn (Official API)**
```
API: LinkedIn Official API (free, approved enterprise partners)
Data: Job postings, company updates, employee growth, news

Signals Available:
├─ New job posting in operations/manufacturing (+7 pts)
├─ Job postings for packaging/supply chain (+9 pts, DIRECT)
├─ Large hiring spree (8+ jobs posted) (+8 pts)
├─ Follower count increase (>10%/mo) (+4 pts)
├─ Company announcement (expansion, partnership) (+6 pts)
├─ Employee badge updates (new locations) (+5 pts)
└─ Job postings filled quickly (low avg duration) (+2 pts, growth)

Cost: $3/month per supplier (free API, processing cost)
Refresh Rate: 24 hours
Confidence: 90% (not all jobs are real, but pattern is strong)

Why Powerful:
"Job postings are leading indicators.
If they're hiring supply chain managers, packaging transformation is coming."
```

#### **F. News APIs (NewsAPI, MediaStack)**
```
API: NewsAPI.com + MediaStack
Data: Press releases, news mentions, company announcements

Signals Available:
├─ Partnership announced (+7 pts, often requires new packaging)
├─ Product launch announced (+8 pts, NEW sales channel)
├─ Facility opening announced (+9 pts, explicit growth)
├─ Funding round closed (+8 pts, capital for growth)
├─ CEO/leadership change (+2 pts, operational shift)
├─ Acquisition of another company (+8 pts, combined packaging needs)
├─ Recall or crisis (+0 pts, skip for now)
└─ Industry award/recognition (+1 pt, prestige, not actionable)

Cost: $5/month per supplier (bulk queries)
Refresh Rate: 24 hours
Confidence: 85% (media source quality varies)

Why Valuable:
"News is public before the buyer even contacts a supplier.
If you read news BEFORE they call, you're ahead."
```

#### **G. Government RFQs (SAM.gov, GovWin)**
```
API: SAM.gov API (free)
Data: Federal contract opportunities, past performance, modifications

Signals Available:
├─ Active RFQ for packaging goods (+8 pts, DIRECT OPPORTUNITY)
├─ Contract modification (increased value) (+6 pts)
├─ Past contract with packaging keyword (+4 pts, repeat buyer)
├─ Contracting office location matches facility (+3 pts, proximity)
└─ Incumbent contractor listed (find competition) (market intel)

Cost: $10/month (bulk RFQ monitoring)
Refresh Rate: 24 hours
Confidence: 100% (official government data)

Why Critical:
"Government contracts = guaranteed payment.
If a buyer has active government contracts, they have stable revenue."
```

---

### **TIER 4: ALTERNATIVE DATA (Pattern Detection)**

#### **H. Website Traffic & SEO (SimilarWeb/SEMrush proxy)**
```
API: Indirect (scrape public data or use free tier)
Data: Website traffic, SEO indicators, page changes

Signals Available:
├─ Website traffic spike (>20% increase) (+5 pts)
├─ New product pages added (+4 pts)
├─ Website redesign (+2 pts, modernization)
├─ Mobile traffic increase (+1 pt, reach expansion)
└─ New keywords ranking (market expansion) (+3 pts)

Cost: $0-20/month (free tiers available)
Refresh Rate: 7-14 days (aggregated data)
Confidence: 70% (traffic data is noisy)

Why Useful:
"Website traffic increase = more sales conversations = more packaging needs.
It's a leading indicator, but weaker than direct signals."
```

#### **I. Marketplace Sales Data (Amazon, Shopify, eBay)**
```
API: Marketplace APIs (indirect via Helium10, Junglescout, etc.)
Data: Sales volume, pricing changes, review patterns

Signals Available:
├─ Sales rank improvement (+5 pts)
├─ Price increase (confident in demand) (+2 pts)
├─ New product variants (+4 pts, business expansion)
├─ Review volume spike (+6 pts, sales surge)
└─ Ad spend increase (tracked via visibility) (+3 pts)

Cost: $20-50/month (third-party tools)
Refresh Rate: 24-48 hours
Confidence: 75% (inferred, not direct access)

Why Valuable:
"Marketplace success = inventory growth = packaging demand.
You can see their sales success without asking them."
```

---

# SECTION 2: SIGNAL TYPES & BASE WEIGHTS
## How Each Data Point Becomes a Score

### **SIGNAL SCORING FORMULA**

```
Base Score = (Signal Points) × (Confidence Level) × (Recency Multiplier)

Example:
  Building expansion permit = +9 base points
  Confidence level = 95%
  Age = 3 days old
  Multiplier = 1.0 (full strength, not decayed yet)
  
  Final Score = 9 × 0.95 × 1.0 = 8.55 points
```

---

### **SIGNAL TYPE REFERENCE TABLE**

| Category | Signal Type | Source | Base Points | Confidence | Why This Matters |
|----------|-------------|--------|-------------|------------|------------------|
| **GOVERNMENT** | Building expansion | Permits | +9 | 95% | Expansion = packaging need |
| | Facility upgrade | Permits | +6 | 90% | Modernization |
| | New equipment | Permits | +5 | 85% | Capacity increase |
| | Facility relocation | SoS + Permits | +7 | 80% | New location = new supplier? |
| **FINANCIAL** | Revenue growth 10%+ | D&B | +8 | 85% | Budget for growth |
| | New loan | D&B | +6 | 75% | Capital for expansion |
| | Employee count +20% | D&B/LinkedIn | +7 | 90% | Growing operations |
| | PayDEX >75 | D&B | +2 | 100% | Reliable payer |
| **MARKETPLACE** | Job posting (packaging) | LinkedIn | +9 | 90% | Direct hiring signal |
| | Hiring spree (8+ jobs) | LinkedIn | +8 | 85% | Rapid scaling |
| | Product launch | News/LinkedIn | +8 | 80% | New sales channel |
| | Partnership announced | News | +7 | 75% | New revenue stream |
| | Funding round | News | +8 | 85% | Capital for growth |
| | Active RFQ (gov contract) | SAM.gov | +8 | 100% | Guaranteed revenue |
| **SENTIMENT** | Review mentions packaging | Reviews | +5 | 70% | Customer feedback |
| | Competitor dissatisfaction | Reviews | +6 | 60% | Switching opportunity |
| **RED FLAGS** | IRS Tax Lien | PACER | -20 | 100% | CRITICAL: Cash flow issue |
| | Bankruptcy Chapter 7 | PACER | -25 | 100% | LIQUIDATION: AVOID |
| | Bankruptcy Chapter 11 | PACER | -15 | 100% | Restructuring |
| | Judgment filed | PACER | -10 | 100% | Legal/payment issues |

---

# SECTION 3: SCORING ALGORITHM
## How Raw Signals Become Urgency Scores (0-100)

### **STEP 1: COLLECT ACTIVE SIGNALS**

```
For a given buyer (e.g., Widget Corp):

Active signals (age < 60 days):
  1. Building expansion permit [3 days old] = +8.55 pts
  2. LinkedIn hiring spree [5 days old] = +7.8 pts
  3. Revenue growth 15% [30 days old] = +7.0 pts
  4. Product launch news [2 days old] = +7.6 pts
  5. PayDEX score 82 [current] = +2.0 pts
  6. New loan obtained [25 days old] = +5.2 pts
  7. Website traffic +25% [10 days old] = +4.5 pts

Total raw points: 42.65
```

### **STEP 2: WEIGHT BY CATEGORY**

```
Signal weights (what matters most):

  Government signals: 35% weight
  Financial signals: 20% weight
  Marketplace signals: 25% weight
  Sentiment/Review signals: 5% weight
  Platform signals: 15% weight

Applying weights:
  Government: (8.55 + 7.0) × 0.35 = 5.44
  Financial: (7.8 + 2.0 + 5.2) × 0.20 = 3.0
  Marketplace: (7.6 + 4.5) × 0.25 = 3.03
  Sentiment: 0 × 0.05 = 0
  Platform: 7.6 × 0.15 = 1.14

Weighted subtotal: 12.61 points
```

### **STEP 3: APPLY BUYER TIER MULTIPLIER**

```
Buyer tier determines signal sensitivity:

  Tier A (Large, $10M+): × 1.2 (higher thresholds)
  Tier B ($3M-10M): × 1.0 (normal)
  Tier C ($500K-3M): × 0.9 (more sensitive)
  Tier D (Small, <$500K): × 0.8 (very sensitive)

Widget Corp = Tier B
Weighted points × 1.0 = 12.61
```

### **STEP 4: APPLY COMPETITOR MULTIPLIER**

```
If buyer is using competitor:

  Competitor has 1-star reviews: × 1.5
  Competitor has 2-star reviews: × 1.3
  Competitor has 3-star reviews: × 1.1
  Competitor has 4+ stars: × 1.0
  No competitor identified: × 1.0

Widget Corp uses Competitor Y (1-star reviews)
Points × 1.5 = 12.61 × 1.5 = 18.92
```

### **STEP 5: CAP AND CONVERT TO 0-100 SCALE**

```
Formula: (Points / 25) × 100

Why 25? Because 25 weighted points = very strong signal

Conversion:
  18.92 / 25 × 100 = 75.68

Final urgency score: 75.68 (rounds to 76)
```

---

### **STEP 6: MAP TO WORD LABEL**

```
Score ranges (by buyer tier):

Tier A Buyers:
  80+: "Strategic" (top opportunity)
  70-79: "Advancing" (strong growth)
  60-69: "Interested" (moderate signals)
  <60: "Early" (watching)

Tier B/C/D Buyers:
  75+: "Aggressive" (high urgency)
  65-74: "Responsive" (moderate urgency)
  50-64: "Steady" (patient growth)
  <50: "Emerging" (early stage)

Widget Corp: Tier B, Score 76
  → Label: "Aggressive"
  → Range: "75-78" (confidence band)
```

---

# SECTION 4: DECAY MECHANICS
## How Signals Age & Lose Value Over Time

### **THE PRINCIPLE**

```
"A hiring spree from 3 months ago doesn't mean they need packaging today.
A hiring spree from 3 days ago means they might."

Decay = signals lose potency with age
```

### **HALF-LIFE MODEL**

```
Half-life = how long until signal is worth 50% of original value

Examples:

  Building expansion permit:
    Half-life = 30 days
    After 30 days = 50% value
    After 60 days = 25% value
    After 90 days = 12.5% value
    After 120 days = 6.25% value (essentially dead)

  Job posting:
    Half-life = 14 days
    After 14 days = 50% value (filled or stale)
    After 28 days = 25% value
    After 42 days = 12.5% value

  Revenue growth:
    Half-life = 60 days
    After 60 days = 50% value
    After 120 days = 25% value (1 quarter later)
```

### **DECAY FORMULA**

```
Current Score = Original Score × (0.5)^(age_days / half_life_days)

Example: Building expansion permit
  Original score: +9 points
  Age: 7 days
  Half-life: 30 days
  
  Current score = 9 × (0.5)^(7/30)
               = 9 × (0.5)^0.233
               = 9 × 0.852
               = 7.67 points

Example: Job posting
  Original score: +8 points
  Age: 21 days
  Half-life: 14 days
  
  Current score = 8 × (0.5)^(21/14)
               = 8 × (0.5)^1.5
               = 8 × 0.354
               = 2.83 points
```

### **DECAY RATE BY SIGNAL TYPE**

| Signal Type | Half-Life | Expires | Why |
|-------------|-----------|---------|-----|
| Building permit | 30 days | 120 days | Expansion project duration |
| Job posting | 14 days | 60 days | Hiring window |
| Product launch | 45 days | 180 days | New product ramp |
| Facility opening | 60 days | 240 days | Integration period |
| Partnership news | 30 days | 120 days | Partnership execution |
| Funding round | 90 days | 360 days | Capital deployment |
| Revenue growth | 60 days | 240 days | Q over Q comparison |
| New loan | 45 days | 180 days | Capital allocation |

---

# SECTION 5: COMPETITOR MULTIPLIERS
## Adjusting Scores When Buyer Uses Competitor

### **COMPETITOR IMPACT**

```
If Widget Corp uses Competitor Y, and Competitor Y has weak reviews:

  This is a SWITCHING OPPORTUNITY
  
Multiplier increases urgency by signaling vulnerability
```

### **REVIEW-BASED MULTIPLIERS**

```
Competitor Y review data (from G2, Capterra, etc.):

  Average rating < 3 stars: × 1.8 (MAJOR switching risk)
  Average rating 3-3.5 stars: × 1.5 (moderate switching risk)
  Average rating 3.5-4 stars: × 1.2 (mild switching risk)
  Average rating 4+ stars: × 1.0 (loyal, not switching)

Review mentions to weight heavily:
  - "Late shipping": × 1.6 (pain point #1)
  - "Price increase": × 1.4 (pain point #2)
  - "Poor quality": × 1.5 (pain point #3)
  - "Bad customer service": × 1.3 (pain point #4)
```

### **EXAMPLE: MULTIPLIER IMPACT**

```
Base score (no competitor identified): 75

Scenario A: Widget Corp uses Competitor Y (1-star avg, "late shipping")
  Multiplier: × 1.8
  Final score: 75 × 1.8 = 135
  Capped at 100 (max scale)
  Result: Score 100 ("CRITICAL - Competitor vulnerability")

Scenario B: Widget Corp uses Competitor Y (4.5-star avg)
  Multiplier: × 1.0
  Final score: 75 × 1.0 = 75
  Result: Score 75 (normal "Aggressive")

Scenario C: Widget Corp uses Competitor Y (3-star avg, "price increase")
  Multiplier: × 1.4
  Final score: 75 × 1.4 = 105
  Capped at 100
  Result: Score 100 ("OPPORTUNITY - Competitor weakness")
```

---

# SECTION 6: RED FLAGS & CONFLICT DETECTION
## When NOT to Pursue (or Proceed Carefully)

### **HARD STOPS (Don't Call)**

```
⚠️ BANKRUPTCY CHAPTER 7 (Liquidation)
   Action: Remove from active list
   Reason: Company is closing
   Wait time: None (permanent)

⚠️ IRS TAX LIEN (Ongoing)
   Action: Flag but don't remove
   Reason: Cash flow crisis, but may still operate
   Note: Add 2-week delay to calling (let them stabilize)
   Multiplier: × 0.3 (reduce urgency)
```

### **CAUTIONS (Proceed Carefully)**

```
⚠️ BANKRUPTCY CHAPTER 11 (Restructuring)
   Action: Deprioritize, don't exclude
   Reason: In reorganization, may need packaging soon
   Wait time: 30-45 days (let them stabilize)
   Multiplier: × 0.6 (reduce urgency, wait for clarity)

⚠️ JUDGMENT FILED (Lawsuit lost)
   Action: Flag, call with caution
   Reason: May be distracted, cash tied up
   Wait time: 14-21 days (let them settle)
   Multiplier: × 0.7 (reduce urgency)

⚠️ PACER LIEN (Contractor dispute)
   Action: Flag, call with caution
   Reason: Supply chain tension, but usually temporary
   Wait time: 7-14 days
   Multiplier: × 0.8 (slight reduction)
```

### **SIGNAL CONFLICTS (Multiple opposing signals)**

```
Scenario: 
  Widget Corp filed bankruptcy Chapter 11 (red flag)
  BUT also posted 8 new job openings
  AND got building expansion permit

Conflict Resolution:
  1. Don't reject (bankruptcy doesn't invalidate growth)
  2. Use MOST RECENT signal for score
  3. Flag with context: "Company may be restructuring + expanding"
  4. Add note: "Likely using this growth as leverage for restructuring"
  5. Result: Score 60-70 (Responsive, not Aggressive)
  6. Message: "Call in 30 days after restructuring clarity"

Why This Matters:
"Sometimes bankruptcy + growth = best opportunity.
They're restructuring AND expanding = strategic pivot.
Wait for clarity, then strike."
```

---

# SECTION 7: DATA QUALITY & VALIDATION
## Making Sure Scores Are Trustworthy

### **CONFIDENCE SCORING**

```
Each buyer record has a confidence_level (0.0-1.0):

How it's calculated:
  Start: 100%
  - Missing D&B data: -10%
  - Missing SoS data: -5%
  - Missing LinkedIn data: -10%
  - Data older than 30 days: -5% per month
  - Conflicting signals: -10%
  
Minimum: 50% (still worth calling)

Display:
  Widget Corp confidence: 95%
  → Message: "Data refreshed 2 days ago"
  → User knows: "This is fresh, reliable intel"
```

### **VALIDATION CHECKS**

```
Before displaying buyer, system checks:

  [ ] Company exists (verified via SoS)
  [ ] Not liquidated (PACER check)
  [ ] Has facility location (permits or address data)
  [ ] Has estimated revenue (D&B or inference)
  [ ] Has contact info available (LinkedIn or public)
  [ ] Not flagged as spam/false business
  
If any check fails: Mark as "unverified", lower confidence
```

---

# SECTION 8: PERSONALIZATION BY SUPPLIER
## How Supplier Tier Changes Score Interpretation

### **TIER 1 SUPPLIERS ($199)**

```
They see: Only top 50-100 buyers (highest urgency)
Scoring: Standard algorithm (no customization)
Label range: "Aggressive" starts at 75

Reasons:
  - They're price-sensitive
  - Need high-confidence leads
  - Can't manage 500 leads
  → Show only 90th+ percentile
```

### **TIER 2 SUPPLIERS ($399)**

```
They see: Top 30-50 buyers + competitor buyers
Scoring: Standard algorithm + competitor multipliers
Label range: "Aggressive" starts at 75 (custom per supplier)

Personalization:
  - Feedback suggests their leads close at X% for "Aggressive"
  - Adjust threshold down if X% is low
  - Adjust up if X% is high
  → Optimize for their close rate
```

### **TIER 3+ SUPPLIERS ($699+)**

```
They see: Top 10-20 buyers + full SAM analysis
Scoring: Heavily customized based on feedback
Label ranges: Personalized per supplier

Personalization:
  - Last 30 feedback cards analyzed
  - "You close 65% on 'Aggressive' leads"
  - "You close 20% on 'Responsive' leads"
  - Adjust algorithm weights:
    - Increase hiring signal weight (+7 → +9)
    - Decrease permit signal weight (+9 → +7)
  → Over time, scores become SUPPLIER-SPECIFIC
```

---

# SECTION 9: PRODUCTION CHECKLIST

- [ ] All 9 data sources integrated (APIs configured)
- [ ] All signal types coded with correct point values
- [ ] Scoring algorithm implemented
- [ ] Decay formula working for all signal types
- [ ] Competitor multipliers active
- [ ] Red flag detection working (bankruptcy, liens)
- [ ] Signal conflict detection active
- [ ] Confidence scoring calculated
- [ ] Validation checks running before display
- [ ] Label mapping correct for all tiers
- [ ] Daily refresh updating all signals
- [ ] Personalization enabled for Tier 2+
- [ ] Load testing passed (100K+ buyers, 500+ suppliers)

---

# STATUS: 🟢 READY FOR CLAUDE AI CODE GENERATION

**All signals defined. All scoring formulas specified. All validation rules documented.**

**Ready to code the intelligence engine.**
