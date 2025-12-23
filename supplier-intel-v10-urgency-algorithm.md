# SUPPLIER INTELLIGENCE V10 - URGENCY SCORING ALGORITHM
## Complete Specification for Production Code

---

## 🎯 EXECUTIVE SUMMARY

**What This Does:**
The Urgency Scoring Algorithm converts raw buyer intelligence signals into a **word-based, human-readable urgency label** that tells suppliers exactly who to call and why.

**Output Format:**
```
Company: "Widget Corp"
Urgency Label: "Aggressive" (Range: 72-78)
Buyer Tier: Medium-sized ($500K-$2M revenue)
Primary Signal: Building expansion permit (7 days old)
Risk Flags: None
Competitor Threat: Competitor Y supplies them (recent 1-star review)
Decay Rate: 14-day half-life (responsive buyer)
Last Updated: Yesterday
Next Re-score: Tomorrow
Why Aggressive?: [Icon] Explains reasoning
```

---

# SECTION 1: BUYER TIER CLASSIFICATION
## How We Categorize Urgency Sensitivity

### **TIER D: Micro Buyers ("Agile")**
- **Annual Revenue:** $100K - $400K
- **AOV (Packaging Order):** $500 - $2K
- **Sensitivity:** VERY HIGH (reactive, price-sensitive)
- **Half-Life Decay:** 7 days
- **Personality:** Fast-moving, trend-reactive, small teams
- **Signal Interpretation:** Micro-signals have outsized impact
- **Example:** Etsy seller with 50 orders/month

### **TIER C: Small Buyers ("Responsive")**
- **Annual Revenue:** $400K - $2M
- **AOV:** $2K - $10K
- **Sensitivity:** HIGH (moderately reactive)
- **Half-Life Decay:** 14 days
- **Personality:** Growth-focused, opportunistic
- **Signal Interpretation:** Signals stick around longer
- **Example:** Small e-commerce brand scaling up

### **TIER B: Mid Buyers ("Stable")**
- **Annual Revenue:** $2M - $10M
- **AOV:** $10K - $50K
- **Sensitivity:** MEDIUM (predictable)
- **Half-Life Decay:** 30 days
- **Personality:** Process-driven, quarterly planning
- **Signal Interpretation:** Signals need time to translate to action
- **Example:** Regional distributor or manufacturer

### **TIER A: Enterprise Buyers ("Steady")**
- **Annual Revenue:** $10M+
- **AOV:** $50K+
- **Sensitivity:** LOW (stable, slow-moving)
- **Half-Life Decay:** 60 days
- **Personality:** Committee-driven, long sales cycles
- **Signal Interpretation:** Major signals only, take months to act
- **Example:** National retailer or large manufacturer

---

# SECTION 2: SIGNAL SCORING BY CATEGORY
## The Raw Point Values (Before Decay)

### **CATEGORY A: GOVERNMENT & EXPANSION SIGNALS**
*(Weight: 35% of final score)*

| Signal | Points | Tier D | Tier C | Tier B | Tier A | Why |
|--------|--------|--------|--------|--------|--------|-----|
| Building Expansion Permit (issued <30 days) | +9 | +9 | +9 | +9 | +8 | Direct facility growth signal |
| UCC Filing (Inventory/Equipment collateral) | +8 | +8 | +8 | +8 | +7 | Growth capital secured |
| SBA 7(a) Loan (business expansion) | +8 | +8 | +8 | +8 | +7 | Bank confidence + capital |
| SBA 504 Loan (facility/equipment) | +8 | +8 | +8 | +8 | +7 | Physical expansion happening |
| Facility Size Increase (property expansion) | +7 | +7 | +7 | +7 | +6 | Capacity scaling |
| Property Assessment Up 20%+ YoY | +6 | +6 | +6 | +6 | +5 | Growth trajectory confirmed |
| Trade Name Change (DBA) | +3 | +4 | +3 | +2 | +1 | Rebranding = pivot opportunity |
| Tax Lien Released (resolved) | +4 | +5 | +4 | +3 | +2 | Recovery from crisis |

---

### **CATEGORY B: FINANCIAL & PAYMENT SIGNALS**
*(Weight: 20% of final score)*

| Signal | Points | Interpretation |
|--------|--------|----------------|
| D&B PAYDEX Improving (80+) | +5 | Reliable payer, growing confidence |
| D&B PAYDEX 70-79 | +3 | Acceptable payer, some caution |
| Tax Lien Released | +4 | Cash flow recovered |
| Credit Limit Increase (D&B) | +3 | Bank sees improved creditworthiness |
| Recent SBA Loan (within 3 months) | +6 | Growth capital ACTIVE |
| Multiple UCC Refinances (12 months) | +4 | Constant capital cycling = growth |

---

### **CATEGORY C: PLATFORM & DIGITAL SIGNALS**
*(Weight: 25% of final score)*

| Signal | Points | Tier D | Tier C | Tier B | Tier A | Why |
|--------|--------|--------|--------|--------|--------|-----|
| Marketplace Reviews Up 50%+ (30-day) | +8 | +9 | +8 | +7 | +5 | Order volume surging |
| LinkedIn Hiring Spree (5+ postings) | +7 | +8 | +7 | +6 | +4 | Scaling operations |
| Ad Spend Spike (FB/Google +50%) | +6 | +7 | +6 | +5 | +3 | Expecting sales surge |
| Social Followers +50% MoM | +6 | +7 | +6 | +5 | +3 | Brand growth |
| Website Traffic +100% (30-day) | +5 | +6 | +5 | +4 | +2 | Demand acceleration |
| New Product Launch (web/marketplace) | +4 | +5 | +4 | +3 | +2 | Expansion into new category |

---

### **CATEGORY D: COMPLIANCE & VALIDATION SIGNALS**
*(Weight: 20% of final score)*

| Signal | Points | Interpretation |
|--------|--------|----------------|
| Active Business License (verified) | +2 | Legitimacy confirmation |
| ISO 9001 Certified | +3 | Quality-focused buyer |
| ISO 14001 Certified | +2 | Sustainability-focused |
| Clean OSHA/EPA Record | +2 | Operational stability |
| Recent Inspection Passed | +1 | Compliance maintained |

---

### **CATEGORY E: COMPETITOR INTELLIGENCE MULTIPLIERS**
*(Applied AFTER base score calculated)*

| Scenario | Multiplier | Example |
|----------|------------|----------|
| Supplier X gets 1-star review ("Late delivery") for Buyer Y | **×1.5** | Buyer is vulnerable, ready to switch |
| Competitor Layoffs detected for buyer's supplier | **×1.8** | Supplier instability = buyer panic |
| Competitor Bankruptcy filed | **×2.0** | Buyer MUST find new supplier NOW |
| Import Data shows recent vendor switch | **×1.3** | Buyer already shopping around |

---

# SECTION 3: DECAY MECHANICS (Half-Life Physics)
## How Signals Lose Strength Over Time

### **HYBRID DECAY FORMULA**

```
Score(t) = Initial_Score × (0.5)^(t / half_life)

Where:
- t = days since signal detected
- half_life = days until signal is 50% strength
```

### **DECAY SCHEDULES BY TIER**

**TIER D (Agile - 7 day half-life):**
```
Day 0:  Building Permit worth +9
Day 7:  Building Permit worth +4.5 (50% strength)
Day 14: Building Permit worth +2.25 (25% strength)
Day 21: Building Permit worth +1.1 (12% strength)
Day 30: Building Permit worth +0.3 (3% strength) → NEGLIGIBLE
```

**TIER C (Responsive - 14 day half-life):**
```
Day 0:  Building Permit worth +9
Day 14: Building Permit worth +4.5 (50% strength)
Day 28: Building Permit worth +2.25 (25% strength)
Day 42: Building Permit worth +1.1 (12% strength)
Day 60: Building Permit worth +0.28 (3% strength) → NEGLIGIBLE
```

**TIER B (Stable - 30 day half-life):**
```
Day 0:  Building Permit worth +9
Day 30: Building Permit worth +4.5 (50% strength)
Day 60: Building Permit worth +2.25 (25% strength)
Day 90: Building Permit worth +1.1 (12% strength)
Day 120: Building Permit worth +0.28 (3% strength) → NEGLIGIBLE
```

**TIER A (Steady - 60 day half-life):**
```
Day 0:  Building Permit worth +9
Day 60: Building Permit worth +4.5 (50% strength)
Day 120: Building Permit worth +2.25 (25% strength)
Day 180: Building Permit worth +1.1 (12% strength)
Day 240: Building Permit worth +0.28 (3% strength) → NEGLIGIBLE
```

### **IMPLEMENTATION RULE**
Once a signal falls below **0.5 points**, remove it from active scoring. (Negligible influence on final score.)

---

# SECTION 4: RED FLAG DETECTION
## When to Show WARNING Information (Not Filtered Out)

### **EXTREME RED FLAGS (Show with "⚠️ Review" Icon)**

**Trigger: Active IRS Tax Lien**
- **Meaning:** Company cannot pay federal taxes
- **Risk Level:** SEVERE (Cash flow crisis)
- **Display:** "⚠️ Tax debt active - verify payment terms"
- **Suppress Lead:** NO (Still show, let supplier decide)

**Trigger: IRS Tax Lien + ONE additional from below**
- Active Lawsuit >$100K: NO (Don't count as "2nd flag")
- OSHA Violations: NO (Don't count as "2nd flag")
- Recent Bankruptcy Dismissal: NO (Don't count as "2nd flag")
- Multiple Bankruptcies: NO (Don't count as "2nd flag")

**Result:** IRS Lien alone = Red flag shown. Needs extreme combo to trigger additional warnings.

---

### **SIGNAL CONFLICTS (Show as "ℹ️ Info" - No Warning)**

**Scenario A: Expansion Permit + Active Tax Lien**
- **Display:** "ℹ️ Growth signals present, but cash flow strain detected"
- **Action:** Show anyway. Supplier can assess risk.
- **Not a warning**, just context.

**Scenario B: Hiring Spree + CEO Recently Quit**
- **Display:** "ℹ️ Scaling plans may be changing with leadership shift"
- **Action:** Show anyway. Timing may shift, not deal-killer.
- **Not a warning**, just info.

**Scenario C: Ad Spend Spike + Bankruptcy Filed**
- **Display:** "ℹ️ Note: Bankruptcy status does not invalidate growth signals"
- **Action:** Show anyway. Company may be restructuring successfully.
- **Not extreme enough** to flag as warning.

---

# SECTION 5: FINAL SCORE CALCULATION
## From Points → Word Label

### **STEP 1: AGGREGATE SIGNALS**

```
Base_Score = (
  Government_Signals × 0.35 +
  Financial_Signals × 0.20 +
  Platform_Signals × 0.25 +
  Compliance_Signals × 0.20
)
```

### **STEP 2: APPLY DECAY**

For each signal, apply half-life formula based on buyer tier and signal age.

```
Decayed_Score = Base_Score (after applying all decay factors)
```

### **STEP 3: APPLY MULTIPLIERS**

If competitor intelligence detected:

```
Final_Score = Decayed_Score × Competitor_Multiplier
(If no competitor signal: Multiplier = 1.0)
```

### **STEP 4: MAP TO WORD LABEL**

```
Score Range → Label → Interpretation

85-100:    "On Fire" (Tier A only)     → Call NOW, deal closing soon
75-84:     "Aggressive" (All Tiers)    → High intent, act this week
65-74:     "Responsive" (All Tiers)    → Good fit, contact within 2 weeks
50-64:     "Steady" (Tier B/C/D)       → Viable, contact within month
35-49:     "Emerging" (Tier D/C only)  → Potential, monitor for signals
20-34:     "Dormant" (All Tiers)       → Low activity, check back later
0-19:      "Cold" (All Tiers)          → No signals, not a priority
```

---

### **SPECIAL CASE: Tier A (Enterprise)**

Tier A buyers move slower. Adjust thresholds:

```
Score Range → Label (Tier A)

80+:        "Strategic" (equivalent to "On Fire" for enterprises)
70-79:      "Emerging" (long sales cycle, but serious)
60-69:      "Tracked" (monitor, no action yet)
50-59:      "Listed" (in database, low priority)
<50:        "Archive" (not worth tracking)
```

---

# SECTION 6: FEEDBACK LOOP INTEGRATION
## How Supplier Feedback Reshapes Algorithm

### **THE FEEDBACK CARD (After Supplier Outreach)**

When supplier reports on a lead 14 days later:

```
Q1: "Did you close this deal?" 
    └─ Yes/No

Q2: "If NO, why?"
    ├─ Never responded
    ├─ Not ready to buy
    ├─ Already has supplier
    ├─ Price too high
    ├─ Not the right contact
    └─ Other reason (free text)

Q3: "How was the timing?"
    ├─ Too early (not ready yet)
    ├─ Perfect (right at decision point)
    └─ Too late (already committed)

Q4: "Want more leads like this?"
    └─ Yes/No

Q5: "Any other feedback?"
    └─ Free text field
```

### **HOW FEEDBACK RESHAPES SCORING**

**Pattern Detection:**
- If 70% of "Aggressive" leads for Supplier X never respond → Lower future "Aggressive" threshold
- If 90% close when "Perfect" timing selected → Weight decay slower for that supplier's industry
- If "Price too high" feedback common → Flag high-AOV buyers separately

**Per-Supplier Learning:**
Each supplier gets personalized signal weights based on THEIR feedback history:
- Supplier A: "Hiring signals matter most to our buyers" → Weight +7 → +9
- Supplier B: "Building permits have failed us" → Weight +9 → +5

**Algorithm Adaptation:**
Every 7 days:
1. Aggregate feedback from all suppliers using platform
2. Detect patterns (e.g., "Competitors' buyer intel has 85% accuracy")
3. Adjust weights for next scoring cycle
4. A/B test: Some suppliers see old weights, some see new
5. Monitor improvement in close rates

---

# SECTION 7: THE "WHY" EXPLANATIONS
## Transparency for Every Score Component

### **ON-HOVER TOOLTIPS (Every Signal)**

```
User hovers over: "⚠️ Aggressive (75-78)"

Tooltip appears:
"Why Aggressive?

✅ Building expansion permit issued 9 days ago (+8 points, decayed to +6.5)
   └─ New facility = new packaging needs within 60 days

✅ Hiring spree on LinkedIn: 8 open positions (+7 points, decayed to +5.2)
   └─ Growing staff = scaling operations = more orders

✅ D&B PAYDEX at 82 (+5 points, no decay)
   └─ Reliable payment history = low risk

✅ Marketplace reviews +60% (30-day period) (+8 points, decayed to +4.1)
   └─ Order volume surging = urgent packaging need

❌ No competitor intelligence: (×1.0 multiplier)
   └─ Not switching suppliers (low urgency multiplier)

Final Score: 6.5 + 5.2 + 5 + 4.1 = 20.8 (normalized to 75-78 range)

Next Re-score: Tomorrow (permits and reviews will re-decay)

[Learn more about this score] [View all signals for this buyer]"
```

### **FULL SIGNAL REPORT (Click "View All Signals")**

Supplier can drill into:
- Every data source checked (Gov, Financial, Platform)
- When data was last updated
- Confidence level (e.g., "100% verified via Secretary of State")
- Raw data (e.g., "SBA loan for $250K, approved 3/15/2025")

---

# SECTION 8: DAILY REFRESH & DECAY LOGIC
## Automated 24-Hour Scoring Cycle

### **AUTOMATED DAILY PROCESS (Cloud Functions)**

```
Every 24 hours (midnight UTC):

1. Query all active buyers for all suppliers
   └─ Filter: Last updated <24 hours ago

2. For each buyer:
   a) Fetch latest signals from all data sources
      ├─ Government (Secretary of State, court records, permits)
      ├─ Financial (D&B, SBA, tax liens)
      ├─ Platform (LinkedIn, News, Marketplace)
      └─ Compliance (Licenses, inspections)
   
   b) Detect NEW signals (since yesterday)
      └─ If new signal detected: Reset decay timer for that signal
   
   c) Re-apply all decay formulas
      └─ Calculate current score based on age of each signal
   
   d) Check for red flags
      └─ If IRS lien just appeared: Flag it
   
   e) Apply competitor multipliers
      └─ If competitor switch detected: Multiply score
   
   f) Recalculate final score & label
      └─ Map to "Aggressive", "Responsive", etc.

3. Update database:
   └─ Store new score, timestamp, decay rates

4. Send notifications to supplier (if score changed significantly):
   └─ "Widget Corp jumped from 'Responsive' to 'Aggressive' (new permit found)"

5. Log feedback metrics:
   └─ Track whether last score predicted actual outcome
```

### **ERROR HANDLING**

**Scenario: API Down (NewsAPI, LinkedIn)**
```
Action: Use cached data from 24h ago
Display: "Data last confirmed 1 day ago (API temporarily unavailable)"
Next retry: 6 hours
```

**Scenario: Government Data Delayed (County permits)**
```
Action: Use last known state, mark as "potentially outdated"
Display: "Permit data may be 2-3 days old (county processing delay)"
Confidence: Reduced from 100% to 75%
```

**Scenario: Conflicting Data (D&B says bankrupt, but SBA loan recent)**
```
Action: Show both pieces, let supplier interpret
Display: "Conflicting signals: Check with buyer before proceeding"
Score: Use most recent signal only (SBA loan = more current)
```

**Scenario: Buyer Deleted/No Longer Exists**
```
Action: Mark buyer as "Inactive" in database
Display: "This company no longer appears in government records"
Score: Set to 0 (company dissolved or disappeared)
```

---

# SECTION 9: PRODUCTION CHECKLIST

- [ ] Tier classification logic implemented
- [ ] All signal scoring values coded (Categories A-E)
- [ ] Decay formula (half-life physics) working for all tiers
- [ ] Multiplier logic for competitor intelligence
- [ ] Red flag detection (IRS lien only) working
- [ ] Signal conflict handling (show as info, not warnings)
- [ ] Word label mapping (Aggressive, Responsive, etc.) live
- [ ] Feedback card collection active
- [ ] Feedback analysis runs weekly
- [ ] Per-supplier weight adjustments implemented
- [ ] 24h refresh cycle automated
- [ ] Error handling for API failures
- [ ] Tooltip "Why" explanations showing
- [ ] Full signal report drill-down available
- [ ] Notifications sent when scores change significantly

---

# STATUS: 🟢 READY FOR CLAUDE AI CODE GENERATION

**All logic specified. All thresholds locked. All edge cases handled.**
