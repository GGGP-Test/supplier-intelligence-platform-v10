# 🎯 WARLORD PLATFORM: DATA INTELLIGENCE BUNDLE V3 (CAPACITY-OPTIMIZED)

## **Complete Buyer & Competitor Intelligence Architecture**

### **Zone Licensing Model | Capacity-Based Pricing | Ghost Company Detection | Government-Weighted Signals**

**Date:** January 3, 2026  
**Version:** 3.0 - Capacity Calculation Engine Integrated  
**Status:** Production-Ready Architecture  
**Platform:** Exclusive Zone Licensing + Capacity-Based Delivery + Intelligence System

---

## 📋 EXECUTIVE OVERVIEW

This document defines the **complete data intelligence infrastructure** for the WARLORD platform—a B2B supplier intelligence platform for packaging suppliers (SMBs in secondary packaging).

**Core Model:**
- Suppliers license **exclusive territories** (zones) for specific products
- One supplier per product per zone (e.g., "North Jersey - Stretch Wrap")
- We deliver **Buyer Intelligence** + **Competitor Intelligence** for that zone
- **NEW:** Buyer delivery volume calculated from supplier's TRUE operational capacity (not their claims)
- **NEW:** Pricing tiers based on calculated capacity with tweak wheel interface
- Bidding pool creates pricing pressure (10+ bidders = price increase)

**This Bundle Covers:**
1. How we extract and validate supplier profile + non-generic value propositions
2. **NEW:** How we calculate supplier's true operational capacity (revenue, AOV, frequency, close rate, sales team time)
3. How we find buyers across 9 foundational intelligence layers
4. How we score and prioritize buyers (urgency, velocity, confidence)
5. How we detect and steal competitors' buyers through review analysis
6. How we alert suppliers to competitive territorial threats
7. **NEW:** Capacity-based pricing tiers with flexible delivery volumes
8. Data refresh cycles, automation levels, cost structure
9. KYB verification with deposit monetization + bid visibility
10. Ghost company detection as premium add-on

---

## TABLE OF CONTENTS

1. [PART 1: Onboarding Seed Data Collection](#part-1)
   - 1.1: Supplier Profile Extraction (ENHANCED)
   - 1.2: Portfolio Strategy Seed (The "70/30 Rule")
   - 1.3: Multi-Platform Revenue Validation (Cross-Check Hierarchy)
   - **1.4: Operational Capacity Calculation Engine (NEW)**
2. [PART 2: Foundational Data Layers (Entry Point)](#part-2)
3. [PART 3: Signal Aggregation Hub](#part-3)
4. [PART 4: Government Records (Layer 4A)](#part-4)
5. [PART 5: Financial Intelligence (Layer 5A)](#part-5)
6. [PART 6: Commercial Real Estate Intelligence (Layer 5B)](#part-6)
7. [PART 7: Licensing & Compliance (Layer 5C)](#part-7)
8. [PART 8: Ghost Company Detection (Premium Add-On)](#part-8)
9. [PART 9: Data Refresh Cycles](#part-9)
10. [PART 10: Buyer Prioritization Logic (UPDATED)](#part-10)
11. [PART 11: KYB Verification Workflow](#part-11)
12. [PART 12: Capacity-Based Pricing Logic (UPDATED)](#part-12)
13. [PART 13: Zone Segmentation](#part-13)
14. [PART 14: Cost Breakdown & Resource Allocation (UPDATED)](#part-14)
15. [PART 15: Implementation Roadmap](#part-15)

---

# PART 1: ONBOARDING SEED DATA COLLECTION {#part-1}

## **Capturing Supplier Profile, Value Proposition & Operational Capacity**

### **Context:**

Before we pull any buyer data, we need to understand the **supplier's business reality**. This isn't just demographics—it's operational constraints, portfolio preferences, capacity limits, AND **their actual differentiation** against competitors.

**CRITICAL ENHANCEMENT (V3):** We now calculate their **true operational capacity** using independent data sources and smart questioning—NOT just trusting their self-reported numbers. This becomes the foundation for pricing tiers and buyer delivery volumes.

**Integration with Bundle 1:** Bundle 1 defines onboarding questions. Bundle 2 uses answers as **seeds** (not rules) to guide buyer prioritization and detect which competitors' buyers are most vulnerable to the supplier's specific value prop.

---

## 1.1: SUPPLIER PROFILE EXTRACTION (Phase 1 - Day 0) - ENHANCED

**What We Collect During Onboarding:**

├─ Business Legal Name + DBA names
├─ Website domain (e.g., toms-packaging.com)
├─ Primary product(s): User selects from visual cards after we crawl their site
├─ Zone selection: Which geographic zone do they want to license?
├─ Revenue range: Self-reported (validated later via hierarchical cross-check in 1.3)
├─ Current customer count: Self-reported (validated later via cross-check in 1.4)
├─ Shipping capacity: How many pallets per shipment? (Tom's constraint: 2+ pallets)
├─ Freight constraints: 3PL relationships? Warehouses in multiple states?
├─ Portfolio preference: Whale hunters / Flow-focused / 70/30 Rule (our recommendation)
├─ **NEW: Top Customer Concentration Analysis**
│   └─ "What percentage of your revenue came from your **top 3 most-paying customers** for [Primary Product] in the last 12 months?"
│       ├─ Option A: 0-30% (diversified base)
│       ├─ Option B: 31-60% (moderate concentration)
│       └─ Option C: 61-100% (whale-dependent)
│   └─ IF they select Option C (61-100%):
│       THEN ask: "For your remaining customers (outside top 3), what's a typical order size for [Primary Product]?"
│           ├─ Option A: $1K-$5K
│           ├─ Option B: $5K-$15K
│           └─ Option C: $15K-$50K+
├─ **NEW: Flow vs. Whale Deal Size Definition**
│   └─ "Based on your business, what's your typical **flow buyer** order size for [Primary Product]?"
│       └─ (Open input or range selection: $500-$2K, $2K-$5K, $5K-$10K)
│   └─ "And what's your typical **whale buyer** order size?"
│       └─ (Open input or range selection: $15K-$30K, $30K-$75K, $75K+)
├─ **NEW: Purchase Frequency Questions**
│   └─ "For your flow buyers ([defined range above]), how often do they typically reorder?"
│       ├─ Monthly
│       ├─ Every 3 months
│       ├─ Every 6 months
│       └─ Annually
│   └─ "For your whale buyers ([defined range above]), what's their typical reorder cycle?"
│       ├─ Monthly
│       ├─ Every 3-6 months
│       ├─ Annually
│       └─ Project-based (unpredictable)
├─ **NEW: Sales Process Mapping (Visual Cards - For Close Rate Inference)**
│   └─ "Which option best describes your typical sales process for [Primary Product]?"
│       ├─ **Option A (Sample-Driven):** Lead → Sample Sent → Quote → Sale
│       │   └─ (AI infers: 30-50% close rate - high conversion due to tangible proof)
│       ├─ **Option B (Direct Sales):** Lead → Sales Call/Meeting → Quote → Sale
│       │   └─ (AI infers: 15-25% close rate - standard B2B conversion)
│       ├─ **Option C (Relationship-Based):** Lead → Multiple Touchpoints → Quote → Sale
│       │   └─ (AI infers: 10-20% close rate - longer cycle, more nurturing)
│       └─ **Option D (Trade Show/Referral):** Lead (warm) → Quick Quote → Sale
│           └─ (AI infers: 40-60% close rate - pre-qualified, high intent)
├─ Close rate context: How do they close? (Sample-driven = Tom's edge)
├─ VALUE PROPOSITION (NON-GENERIC): What makes them different from competitors?
│   └─ If answer is generic ("best prices", "good service"), triggers AI follow-up questioning
├─ AI FOLLOW-UP QUESTIONING (If Needed):
│   └─ "Between these two scenarios:
│       A) Buyer needs 10K stretch wrap rolls by Friday (urgent, minimal specs)
│       B) Buyer needs 10K rolls with custom thickness + recycled material (3 weeks, complex)
│       Which one would you close faster? Why? What's your advantage?"
│   └─ This reveals their true operational strength (speed vs. customization vs. cost)
├─ Operational Strength Categorization (AI-inferred from answers):
│   ├─ Speed Leader: Fast fulfillment, low setup time, minimal customization
│   ├─ Quality/Customization: Premium specs, material options, technical support
│   ├─ Cost Leader: Bulk efficiency, low overhead, price-focused buyers
│   ├─ Hybrid: Mix of above (most common for SMBs)
│   └─ Niche Specialist: Specific industry verticals (pharmaceutical, food, etc.)
├─ Value Prop Strength Score (0-100): How clear/defensible is their differentiation?
│   ├─ 0-30: Commodity (no real differentiation, competes on price only)
│   ├─ 31-60: Weak Differentiation (some edge, not defensible)
│   ├─ 61-85: Strong Differentiation (clear advantage, defensible)
│   └─ 86-100: Defensible Moat (significant competitive advantage)
└─ Decision-maker contact: CEO, VP Sales, Owner (extracted from domain)

**Automation:**
- **Website crawl:** Scrape their site for product listings (95% automated via Apify, Playwright)
- **Product visual cards:** Show them what we found—"We see you sell Stretch Wrap, Tape, Pallets. Pick your primary."
- **If single product:** Auto-select, ask for confirmation
- **If multiple products:** Force choice—one product per zone license
- **Value Prop AI Scoring:** 100% automated (GPT-4/Claude analyzes answers, generates follow-up questions, categorizes strength)
- **Sales Process Visual Cards:** 100% automated selection, AI infers close rate from pattern

**Cross-Check Logic (Critical):**

```
IF supplier claims "100 customers" BUT tax records show "10 deals"
  THEN cap buyer delivery at 15-20/month (conservative start)
  AND notify supplier: "We're starting conservatively based on market data"

IF supplier claims "$3M revenue" BUT Secretary of State shows "Suspended status"
  THEN flag for manual review before approval

IF supplier website is <1 year old
  THEN flag for manual review before approval

IF value prop answer is too generic (scored 0-30)
  THEN AI generates follow-up scenarios to uncover real differentiation
  THEN re-score after follow-up
  IF still generic after follow-up
    THEN notify: "Your value prop isn't clear yet. We recommend focusing on ONE competitive advantage before scaling."

IF top 3 customers = 61-100% concentration
  THEN flag as "Whale-Dependent" → prioritize flow buyer delivery to diversify risk
  THEN calculate flow AOV separately from whale AOV in Section 1.4
```

**Output:**
- **Supplier Profile Card** (stored in database)
- Includes: Zone, Product, Portfolio Seed, Top Customer Concentration %, Flow/Whale Deal Size Definitions, Purchase Frequencies, Sales Process Type, Inferred Close Rate, Verified Status, **Operational Strength Category**, **Value Prop Strength Score (0-100)**
- This data feeds directly into **Section 1.4 (Capacity Calculation)** and competitor buyer detection (Part 2.6)

---

## 1.2: PORTFOLIO STRATEGY SEED (The "70/30 Rule")

**The Question We Ask:**

> "Which buyer strategy fits your business best?"
>
> **Option A: Whale Hunters**  
> Focus on large deals ($50K-$500K+). High reward, high risk. Long sales cycles.
>
> **Option B: Flow Focused**  
> Focus on steady cash flow ($3K-$10K deals). Predictable revenue. Shorter cycles.
>
> **Option C: The 70/30 Rule** (Recommended)  
> 70% flow customers (steady cash) + 30% whale hunting (growth engine). Balanced risk.

**Why This Matters:**
- **Seed, not rule:** If they pick "Whales Only," we still deliver flow customers mixed in
- **Tom's Trap education:** We explain why over-reliance on whales = extinction risk
- **Prioritization hint:** If they pick Flow, we frontload smaller buyers; if Whales, we frontload bigger buyers
- **Reality check:** Most suppliers **think** they want whales, but their business needs flow

**Automation:**
- Visual card selection (100% self-serve)
- AI summary after selection: "You chose 70/30. Here's what that means for your first 50 buyers..."

**Output:**
- **Portfolio Seed:** Stored in Supplier Profile Card
- Used to **rank** buyers (not filter them out)

---

## 1.3: MULTI-PLATFORM REVENUE VALIDATION (Cross-Check Hierarchy)

**Why:**
Suppliers often overestimate capacity or underestimate constraints. We validate revenue before delivering data using a **hierarchical fallback system**.

**Sources for Cross-Check (In Priority Order):**

**TIER 1 (Highest Confidence):**
├─ D&B Report (if available): Revenue range, employee count, PAYDEX
├─ Secretary of State Tax Records (where public): Tax filings, IRS liens, state revenue data

**TIER 2 (High Confidence):**
├─ LinkedIn: Employee count + hiring trends → revenue proxy
│  └─ Formula: (Employees × $200K avg revenue per employee) ÷ Margin = estimated revenue
├─ Website analysis: Copyright year, social proof, customer logos, case studies
└─ Google Query Search: "[Company Name/Website] + revenue" 
    └─ Top 3 results mentioning the EXACT company get aggregated for range estimate

**TIER 3 (Medium Confidence):**
├─ ZoomInfo / RocketReach / Apollo: Company intelligence platforms
├─ Industry report matching (e.g., "average packaging supplier revenue in New Jersey")
└─ Customer logo analysis (recognizable brands often correlate with higher revenue)

**TIER 4 (Fallback - Use Only If Tiers 1-3 Exhausted):**
├─ Website traffic estimate (SimilarWeb): Traffic proxy (often unreliable)
└─ Manual outreach: Email/call supplier for verification

**Validation Logic:**

```
STEP 1: Query Tier 1 Sources (D&B + SoS)
  IF revenue found in both sources within 20% variance
    THEN confidence = HIGH (85%+), use estimated range

  IF revenue found in one source only
    THEN cross-check with Tier 2

STEP 2: If Tier 1 Incomplete, Query Tier 2 (LinkedIn + Google Search)
  IF LinkedIn employee count × $200K correlates with Google search results (within 25%)
    THEN confidence = MEDIUM-HIGH (70-80%), use range

  IF no correlation
    THEN query Tier 3

STEP 3: If Tier 2 Incomplete, Query Tier 3 (ZoomInfo + Industry Report)
  IF ZoomInfo + industry report correlate (within 30%)
    THEN confidence = MEDIUM (60-70%), use range

  IF no correlation
    THEN flag for manual verification, set to "Unknown" (don't guess)

STEP 4: Final Revenue Assignment
  IF claimed $5M BUT data shows $500K-$1M
    THEN use our data ($500K-$1M range) for capacity calculations
    THEN confidence = 70% (conflict between claim and data)
    THEN handle silently (don't alert supplier to discrepancy yet)

  IF claimed $5M AND all sources confirm $4.5M-$5.5M
    THEN confidence = 90%, proceed with full buyer delivery

  IF claimed $5M BUT no sources confirm (1% of cases)
    THEN flag for manual review, offer conservative 50 buyers/month baseline
```

**Output:**
- **Validated Revenue Range** (confidence score 0-100%)
- **Employee Count Estimate** (used in 1.4 for sales team capacity)
- Risk flags for sales team (prepayment required? trial period?)
- **Feeds directly into Section 1.4 capacity calculations**

---

## 1.4: OPERATIONAL CAPACITY CALCULATION ENGINE (NEW) {#section-1-4}

### **The Core Innovation: Calculate TRUE Monthly Buyer Capacity**

**Goal:** Determine how many buyers per month the supplier can realistically handle based on:
1. **Validated Revenue** (from Section 1.3, not their claims)
2. **Average Order Value (AOV)** - separated into Flow AOV and Whale AOV
3. **Purchase Frequency** - how often customers reorder
4. **Inferred Close Rate** - from sales process type (Section 1.1)
5. **Sales Team Time Capacity** - how many hours per week they have for sales
6. **Operational Baseline** - minimum 50 buyers/month regardless of size

This calculation determines:
- How many buyers we deliver per month
- Which pricing tier they should start at
- Whether to stretch them 40-50% above current capacity

---

### **STEP 1: Calculate Average Order Value (AOV)**

**Challenge:** One whale customer can skew AOV heavily. We need to separate flow AOV from whale AOV.

**Methodology:**

```
IF Top 3 Customer Concentration = 61-100% (Option C from Section 1.1)
  THEN:
    // Calculate whale revenue and whale customer count
    Whale_Revenue = Total_Revenue × (Top_3_Concentration_% / 100)
    Whale_Customer_Count = 3 (their top 3)
    
    // Calculate flow revenue and customer count
    Flow_Revenue = Total_Revenue - Whale_Revenue
    Flow_Customer_Count = Total_Customer_Count - 3
    
    // Calculate separate AOVs
    Whale_AOV = Whale_Revenue / Whale_Customer_Count
    Flow_AOV = Flow_Revenue / Flow_Customer_Count
    
    // Use flow AOV for capacity calculations (more stable)
    Working_AOV = Flow_AOV

ELSE IF Top 3 Customer Concentration = 31-60% (Option B)
  THEN:
    // Moderate concentration, use overall AOV with slight adjustment
    Working_AOV = Total_Revenue / Total_Customer_Count × 0.85
    // (0.85 adjustment accounts for top customer skew without full separation)

ELSE (Concentration = 0-30%, Option A - diversified)
  THEN:
    // Clean distribution, use straight AOV
    Working_AOV = Total_Revenue / Total_Customer_Count
```

**Cross-Validation with Onboarding Answers:**

```
// Supplier told us their typical flow deal size in Section 1.1
Stated_Flow_Deal_Size = Answer from "typical flow buyer order size"

IF ABS(Working_AOV - Stated_Flow_Deal_Size) / Working_AOV > 0.30
  THEN:
    // More than 30% variance = potential inconsistency
    Confidence_Score = Confidence_Score - 10
    // Use our calculated AOV (data > claims)
    Final_AOV = Working_AOV
ELSE:
  THEN:
    // Answers align with data, boost confidence
    Confidence_Score = Confidence_Score + 5
    Final_AOV = (Working_AOV + Stated_Flow_Deal_Size) / 2  // Average the two
```

**Industry Pricing Fallback (If No AOV Data Available):**

```
IF Total_Revenue = "Unknown" OR Total_Customer_Count = "Unknown"
  THEN:
    // Use industry averages for primary product + competitor pricing
    
    STEP 1: Query industry average pricing for [Primary Product] in [Zone]
      Example: "Stretch wrap average price per case New Jersey"
      Sources: Trade publications, competitor public pricing, industry reports
    
    STEP 2: Query 5-10 competitors in zone, scrape public pricing (if available)
      Calculate: Median_Competitor_Price
    
    STEP 3: Triangulate
      Industry_AOV_Estimate = (Industry_Average + Median_Competitor_Price) / 2
      Confidence = 65% (lower confidence, but usable)
    
    Final_AOV = Industry_AOV_Estimate
```

**Output from STEP 1:**
- **Final_AOV:** $X (e.g., $4,500)
- **Confidence Score:** 70-90%
- **Whale AOV** (if separated): $X
- **Flow AOV** (if separated): $X

---

### **STEP 2: Calculate Monthly Customer Value (Revenue Per Month)**

**Challenge:** Customers don't all buy every month. Purchase frequency varies between flow and whale buyers.

**Methodology:**

```
// From Section 1.1, we asked about purchase frequency

Flow_Buyer_Frequency = Answer from "flow buyers reorder cycle"
  Options were: Monthly / Every 3 months / Every 6 months / Annually

Whale_Buyer_Frequency = Answer from "whale buyers reorder cycle"
  Options were: Monthly / Every 3-6 months / Annually / Project-based

// Convert to monthly frequency multiplier
Flow_Frequency_Multiplier = 
  IF Monthly → 1.0
  IF Every 3 months → 0.33
  IF Every 6 months → 0.17
  IF Annually → 0.08

Whale_Frequency_Multiplier = 
  IF Monthly → 1.0
  IF Every 3-6 months → 0.25  // (average of 3 and 6 months)
  IF Annually → 0.08
  IF Project-based → 0.15  // (assume ~2 projects per year on average)

// Calculate monthly revenue contribution
IF we separated Flow and Whale:
  Flow_Monthly_Revenue = Flow_Revenue × Flow_Frequency_Multiplier
  Whale_Monthly_Revenue = Whale_Revenue × Whale_Frequency_Multiplier
  Total_Monthly_Customer_Value = Flow_Monthly_Revenue + Whale_Monthly_Revenue
ELSE:
  Total_Monthly_Customer_Value = Total_Revenue × Flow_Frequency_Multiplier
```

**Example:**

```
Supplier: $5M annual revenue, 625 customers/year
Top 3 customers = 70% of revenue (Whale-Dependent)

Whale Revenue = $5M × 0.70 = $3.5M
Flow Revenue = $5M × 0.30 = $1.5M

Whale AOV = $3.5M / 3 = $1,166,667 per whale
Flow AOV = $1.5M / 622 = $2,412 per flow customer

Flow buyers reorder: Every 3 months (0.33 multiplier)
Whale buyers reorder: Annually (0.08 multiplier)

Flow Monthly Revenue = $1.5M × 0.33 = $495,000/month
Whale Monthly Revenue = $3.5M × 0.08 = $280,000/month

Total Monthly Customer Value = $495K + $280K = $775,000/month
```

**Output from STEP 2:**
- **Total Monthly Customer Value:** $775,000/month
- **Flow Monthly Revenue:** $495,000/month
- **Whale Monthly Revenue:** $280,000/month

---

### **STEP 3: Infer Close Rate from Sales Process**

**Challenge:** Suppliers lie about close rates. We infer it from their sales process type instead.

**Methodology:**

```
// From Section 1.1, we asked them to select their sales process using visual cards

Sales_Process_Type = Answer from "sales process mapping"

Close_Rate_Range = 
  IF "Sample-Driven" (Lead → Sample → Quote → Sale)
    THEN Close_Rate = 30-50%  // High conversion, tangible proof
    Use_Midpoint = 40%
  
  IF "Direct Sales" (Lead → Sales Call → Quote → Sale)
    THEN Close_Rate = 15-25%  // Standard B2B
    Use_Midpoint = 20%
  
  IF "Relationship-Based" (Lead → Multiple Touchpoints → Quote → Sale)
    THEN Close_Rate = 10-20%  // Longer nurturing
    Use_Midpoint = 15%
  
  IF "Trade Show/Referral" (Warm Lead → Quick Quote → Sale)
    THEN Close_Rate = 40-60%  // Pre-qualified
    Use_Midpoint = 50%

Final_Close_Rate = Use_Midpoint
```

**Industry Benchmark Adjustment:**

```
// B2B packaging industry baseline: 10-20% close rate for cold leads
// If supplier's process suggests higher, we believe it (sample advantage is real)

IF Final_Close_Rate < 15%
  THEN Final_Close_Rate = 15%  // Floor at industry minimum

IF Final_Close_Rate > 60%
  THEN Final_Close_Rate = 60%  // Cap at realistic maximum
```

**WARLORD Lead Quality Boost:**

```
// Our buyers are 50% higher quality than cold leads (pre-qualified via signals)

Supplier_Base_Close_Rate = Final_Close_Rate
WARLORD_Adjusted_Close_Rate = Supplier_Base_Close_Rate × 1.5

// Example: If supplier normally closes 20%, with our buyers they close 30%
```

**Output from STEP 3:**
- **Supplier Base Close Rate:** 20%
- **WARLORD Adjusted Close Rate:** 30%

---

### **STEP 4: Calculate Current Monthly Sales Volume**

**Methodology:**

```
// How many sales are they currently closing per month?

Current_Monthly_Sales = Total_Monthly_Customer_Value / Final_AOV

// Example:
// $775,000 per month / $2,412 per flow order = 321 sales per month
```

**Reverse-Calculate Lead Volume (Optional - For Context):**

```
// How many leads do they need to hit current sales volume?

Estimated_Monthly_Leads = Current_Monthly_Sales / Supplier_Base_Close_Rate

// Example:
// 321 sales / 0.20 close rate = 1,605 leads per month currently
```

**Output from STEP 4:**
- **Current Monthly Sales:** 321 orders/month
- **Estimated Current Lead Volume:** 1,605 leads/month

---

### **STEP 5: Calculate Sales Team Time Capacity**

**Challenge:** Don't overload their sales team. Calculate how much time they have for new buyers.

**Methodology:**

```
// From Section 1.3, we validated employee count via LinkedIn/D&B

Total_Employees = Validated_Employee_Count

// Estimate how many are in sales/operations (involved in closing)
IF Total_Employees <= 5
  THEN Sales_Team_Size = Total_Employees × 0.8  // Small shop, most people sell
ELSE IF Total_Employees 6-20
  THEN Sales_Team_Size = Total_Employees × 0.5  // Growing, 50% in sales/ops
ELSE IF Total_Employees 21-50
  THEN Sales_Team_Size = Total_Employees × 0.3  // More admin/support
ELSE
  THEN Sales_Team_Size = Total_Employees × 0.2  // Larger org, specialized roles

// Calculate weekly sales hours available
Hours_Per_Salesperson_Per_Week = 40 hours
Sales_Focus_Time_% = 0.60  // 60% of time on selling (rest = admin, meetings, etc.)

Total_Weekly_Sales_Hours = Sales_Team_Size × Hours_Per_Salesperson_Per_Week × Sales_Focus_Time_%

// Example: 2 salespeople × 40 hours × 0.60 = 48 hours/week for sales
```

**Calculate Hours Per Buyer Close:**

```
// How long does it take them to close one buyer?

Hours_Per_Buyer = 
  IF Sales_Process = "Sample-Driven"
    THEN 3 hours  // (Sample prep + follow-up + quote + close)
  IF Sales_Process = "Direct Sales"
    THEN 4 hours  // (Multiple calls + quote + negotiation)
  IF Sales_Process = "Relationship-Based"
    THEN 6 hours  // (Longer nurturing, multiple touchpoints)
  IF Sales_Process = "Trade Show/Referral"
    THEN 2 hours  // (Pre-qualified, quick close)

// Example: Sample-driven = 3 hours per buyer
```

**Calculate Current Time Utilization:**

```
Current_Weekly_Time_Used = Current_Monthly_Sales / 4 × Hours_Per_Buyer

// Example:
// 321 sales per month / 4 weeks = 80 sales per week
// 80 sales × 3 hours each = 240 hours per week currently used

Current_Time_Utilization_% = Current_Weekly_Time_Used / Total_Weekly_Sales_Hours

// Example:
// 240 hours / 48 hours = 500% utilization
// (This means either our estimates are off, OR they're swamped and need help)
```

**50% Buffer Capacity:**

```
// We can push them 50% above current capacity

Max_Weekly_Sales_Hours_With_Buffer = Total_Weekly_Sales_Hours × 1.5

// Example:
// 48 hours × 1.5 = 72 hours per week maximum

Max_Buyers_Per_Week_With_Buffer = Max_Weekly_Sales_Hours_With_Buffer / Hours_Per_Buyer
Max_Buyers_Per_Month_With_Buffer = Max_Buyers_Per_Week_With_Buffer × 4

// Example:
// 72 hours / 3 hours per buyer = 24 buyers per week
// 24 × 4 = 96 buyers per month (capacity cap)
```

**Sanity Check:**

```
IF Current_Time_Utilization_% > 200%
  THEN:
    // Our estimates are likely off, use operational baseline instead
    Flag = "Capacity calculation uncertain, using baseline"
    Use_Operational_Baseline = TRUE
```

**Output from STEP 5:**
- **Sales Team Size:** 2 people
- **Total Weekly Sales Hours:** 48 hours
- **Hours Per Buyer:** 3 hours
- **Current Time Utilization:** 500% (flagged as uncertain)
- **Max Buyers Per Month (50% buffer):** 96 buyers/month

---

### **STEP 6: Final Capacity Recommendation**

**Methodology:**

```
// Calculate WARLORD recommended buyer delivery volume

WARLORD_Buyer_Recommendation = 
  Method 1 (Revenue-Based): Current_Monthly_Sales × (WARLORD_Adjusted_Close_Rate / Supplier_Base_Close_Rate) × 1.4
  Method 2 (Time-Based): Max_Buyers_Per_Month_With_Buffer
  
  // Use the LOWER of the two (don't overwhelm them)
  Recommended_Buyers = MIN(Method 1, Method 2)
  
  // Apply minimum baseline (50 buyers/month floor)
  IF Recommended_Buyers < 50
    THEN Recommended_Buyers = 50

// Apply confidence adjustment
IF Confidence_Score < 70%
  THEN Recommended_Buyers = Recommended_Buyers × 0.8  // Conservative start
```

**Example Calculation:**

```
Method 1 (Revenue-Based):
  321 current sales × (30% WARLORD close / 20% supplier close) × 1.4
  = 321 × 1.5 × 1.4 = 674 buyers/month (revenue supports this)

Method 2 (Time-Based):
  96 buyers/month (time capacity cap with 50% buffer)

Recommended = MIN(674, 96) = 96 buyers/month

Apply minimum:
  MAX(96, 50) = 96 buyers/month

Confidence = 75%
  No adjustment needed (>70%)

FINAL RECOMMENDATION: 96 buyers/month
```

**Pricing Tier Assignment:**

```
// From Part 12 (updated pricing tiers)

IF Recommended_Buyers <= 50
  THEN Starting_Tier = "Up to 50 buyers" at $2,000/month ($66/day)

IF Recommended_Buyers 51-100
  THEN Starting_Tier = "Up to 100 buyers" at $3,600/month ($120/day)

IF Recommended_Buyers 101-250
  THEN Starting_Tier = "Up to 250 buyers" at $7,200/month ($240/day)

IF Recommended_Buyers 251+
  THEN Starting_Tier = "Up to 1000 buyers" at $13,500/month ($450/day)

// In our example: 96 buyers → "Up to 100 buyers" tier at $120/day
```

**Output from STEP 6:**
- **Recommended Monthly Buyer Delivery:** 96 buyers/month
- **Starting Pricing Tier:** "Up to 100 buyers" at $3,600/month
- **Calculation Confidence:** 75%
- **Notes:** "Time capacity is the limiting factor, not revenue capacity"

---

### **COMPLETE OPERATIONAL CAPACITY OUTPUT (What We Store)**

**Supplier Capacity Profile:**

```json
{
  "supplier_id": "SUP-00123",
  "zone": "North Jersey - Stretch Wrap",
  "validated_revenue": "$5M (confidence: 85%)",
  "validated_employees": 8,
  "sales_team_size_estimate": 2,
  
  "aov_analysis": {
    "top_customer_concentration": "70% (3 customers)",
    "whale_aov": "$1,166,667",
    "flow_aov": "$2,412",
    "working_aov": "$2,412",
    "confidence": "80%"
  },
  
  "frequency_analysis": {
    "flow_reorder_cycle": "Every 3 months",
    "whale_reorder_cycle": "Annually",
    "flow_monthly_revenue": "$495,000",
    "whale_monthly_revenue": "$280,000",
    "total_monthly_value": "$775,000"
  },
  
  "close_rate_analysis": {
    "sales_process": "Sample-Driven",
    "supplier_base_close_rate": "40%",
    "warlord_adjusted_close_rate": "60%",
    "hours_per_buyer": 3
  },
  
  "capacity_analysis": {
    "current_monthly_sales": 321,
    "current_weekly_sales_hours": 48,
    "max_buyers_with_buffer": 96,
    "time_capacity_limiting_factor": true
  },
  
  "recommendation": {
    "recommended_buyers_per_month": 96,
    "starting_pricing_tier": "Up to 100 buyers at $120/day",
    "calculation_confidence": "75%",
    "notes": "Time capacity is limiting factor. Consider hiring +1 salesperson to scale."
  }
}
```

**What Supplier Sees (Dashboard Summary):**

═══════════════════════════════════════════════════════
**YOUR CAPACITY ANALYSIS**

Based on your revenue, sales process, and team size, we recommend:

**📊 Recommended Plan:** Up to 100 Buyer Intelligence Reports/Month  
**💰 Price:** $3,600/month ($120/day)

**Why this recommendation?**
├─ Your current sales volume: ~321 orders/month
├─ Your sales team capacity: 2 people × 48 hours/week
├─ With WARLORD's higher-quality buyers, we estimate you can handle 96-100/month
├─ This is 50% above your current workload—challenging but achievable

**Want to scale faster?**
├─ Hire +1 salesperson → Move to "Up to 250 buyers/month" tier
├─ Automate quoting → Save 30% time per buyer
└─ Current tier has tweak wheel: Adjust 50-150 buyers as needed

═══════════════════════════════════════════════════════

---

**This capacity calculation now flows into:**
- **Part 10:** Buyer delivery volume (we deliver what they can handle)
- **Part 12:** Pricing tier assignment (capacity = price, not claims)
- **Part 14:** Cost structure (margin calculations based on actual delivery volume)

---

# PART 2: FOUNDATIONAL DATA LAYERS (Entry Point) {#part-2}

## **Layer 1-2: Company Profile → Competitor Mapping**

### **Context:**

These layers establish the **foundation** for all downstream intelligence. We start with the supplier's business domain, extract everything public, then map their competitive landscape to find **vulnerable competitor buyers**.

**Automation:** 85-100%  
**Cost (Phase 1):** $0-50/month (free APIs + scraping)  
**Cost (Phase 2):** $200-500/month (premium LinkedIn, Apollo, enrichment)

---

## 2.1: LAYER 1A - COMPANY PROFILE EXTRACTION

**What We Extract:**

FROM: Supplier's website domain (e.g., widget-corp.com)

├─ Legal business name
├─ DBA names (doing business as)
├─ HQ address + regional locations
├─ Industry classification (SIC code inference)
├─ Product catalog (scraped from site)
├─ Contact info (phone, email, support@)
├─ Copyright year (business age proxy)
├─ Customer logos (if displayed on site)
├─ Social proof (testimonials, case studies)
└─ Website traffic estimate (SimilarWeb, Alexa)

**Tools:**
- **SoS records:** Email verification, DBA discovery, government records on tax + permits
- **Apify web scraper:** Product catalog, contact info
- **WHOIS lookup:** Domain registration date
- **SimilarWeb API:** Traffic estimate (free tier)
- **Clearbit API:** Company enrichment ($50/mo)

**Output:**
- **Company Profile Object** (JSON)
- Used in Layer 1B to find decision-makers and build buyer personas

---

## 2.2: LAYER 1B - EMAIL DOMAIN & DECISION-MAKER INTELLIGENCE

**Critical Entry Point:** Everything flows from the email domain.

**What We Extract:**

FROM: Email domain + LinkedIn

├─ Decision-maker emails: CEO, VP Sales, VP Operations, Owner
├─ Organizational structure: Who reports to whom?
├─ LinkedIn profiles: Job titles, tenure, background
├─ Contact info enrichment: Direct phone numbers, mobile
├─ Email pattern identification: firstname.lastname@domain.com
└─ Key stakeholder list (for competitor outreach blocking)

**Tools:**
- **SoS records:** Email verification, DBA match, government records
- **Hunter.io:** Email pattern detection ($50/mo)
- **Apollo.io:** Contact enrichment ($100/mo Phase 2)
- **LinkedIn Sales Navigator:** Phase 2 ($80/mo)
- **Manual LinkedIn search:** Phase 1 (free)

**Output:**
- **Decision-Maker Contact List** (names, emails, titles)
- Used in competitor intelligence (Layer 2A)

---

## 2.3: LAYER 1C - MULTI-PLATFORM PRESENCE & ACTIVITY

**What We Track:**

├─ LinkedIn: Company page followers, employee count, job postings, company updates
├─ Facebook Business Page: Followers, review count, activity
├─ Instagram (if relevant): Follower growth, post frequency
├─ Reddit: Mentions in industry subreddits (packaging, manufacturing, logistics)
├─ Google Reviews: Review count + sentiment + volume trending (Rising or falling)
├─ Google Search Query: "[CompanyName OR Website] + reviews" → Top 3 review platforms
├─ News API: Press releases, announcements, funding news
├─ BBB Profile: Rating, complaint history, years in business
└─ Marketplace Reviews (Amazon, Etsy, eBay, Shopify): Volume trending + sentiment

**Why:**
- **Growth signals:** LinkedIn follower surge = hiring spree = scaling
- **Social proof:** Google reviews mentioning "fast shipping" = packaging need
- **Legitimacy check:** BBB profile + reviews = established business
- **Volume trending:** Review count spike or decline = demand shift

**Tools:**
- LinkedIn API (limited free, $80/mo paid)
- Facebook Graph API (free)
- Reddit API (free)
- Google Places API (free tier: 100 lookups/day)
- News API (free tier: 100 articles/day)

**Automation:** 100% (API-driven)

**Output:**
- **Social Presence Score** (0-100)
- **Growth Velocity** (follower growth %, review count trend)
- Signals feed into Layer 3B (urgency/velocity scoring)

---

## 2.4: LAYER 1E - AI-POWERED INFERENCE

**What We Infer:**

FROM: All Layer 1 data aggregated

├─ Industry classification: Manufacturing/ Other Packaging companies / E-commerce / Pharma / Food & Beverage / Transportation / Storage
├─ Company size estimate: <10 / 10-50 / 50-200 / 200+
├─ Revenue range estimate: $0-$500K / $500K-$2M / $2M-$10M / $10M+
├─ Growth trajectory: Scaling (hockey stick) / Growing (steady) / Stable / Declining
├─ Buyer profile generation: Who do they sell to? (inferred from testimonials, case studies)
├─ Packaging need estimate: Volume per week (based on industry + size)
└─ Urgency baseline: Hot (recent signals) / Warm (moderate) / Cool (no recent signals)

**Method:**
- **AI Models:** GPT-4/Claude/Perplexity/Vertex API with structured output
- **Prompt:** Feed all Layer 1 data → Ask: "What's their revenue range? Growth stage? Packaging volume? Industry focus?"
- **Reasoning:** Multi-model inference (if 2+ models agree, confidence boost)

**Automation:** 100% (AI model)

**Cost:** $0.10-$0.50 per inference (varies by model)

**Output:**
- **Inferred Business Profile** (added to Buyer Intelligence Card)

---

## 2.5: LAYER 2A - DIRECT COMPETITOR DISCOVERY

**What We Find:**

FROM: Supplier's industry + product + location

├─ Direct competitors: Who else sells stretch wrap in North Jersey?
├─ Indirect competitors: Who sells substitute products (shrink wrap vs. stretch)?
├─ Market leaders: Top 3-5 players in the region
├─ Using third parties: Apollo, Instantly.ai, ZoomInfo, Rocketreach, LinkedIn, etc.
├─ Pricing signals: Public pricing (if available on competitor sites)
├─ Product mix: What products do THEY offer vs. what supplier offers?
└─ Market positioning: Premium / Mid-market / Budget

**Tools:**
- **Google Search Queries:**
  - "[Supplier Product] supplier [Location]"
  - "[Supplier CompanyName] alternative"
  - "[Supplier ProductName] [Location]"
  - (Scrape top 20 results)
- **LinkedIn Company Search:** Industry = "Packaging" + Location = "New Jersey"
- **Yellow Pages / Yelp:** Business directory scraping
- **Trade associations:** Packaging industry associations member lists

**Automation:** 85% (search + scraping automated, manual verification)

**Output:**
- **Competitor List** (10-20 competitors per zone)
- Used in Layer 2B for buyer-stealing analysis

---

## 2.6: LAYER 2B - COMPETITOR BUYER-STEALING INTELLIGENCE

### **Strategy: From "Competitor Strength Score" to "Buyer Stealing Opportunity Score"**

**GOAL 1: Steal Competitor Buyers Through Review Analysis**

We analyze competitor reviews to find **unhappy or underserved buyers** that match the supplier's value prop.

**What We Collect Per Competitor Review:**

FOR EACH COMPETITOR REVIEW:

├─ Review Platform: Google, Yelp, BBB, Trustpilot, or platform found via "[Competitor] + reviews"
├─ Review Recency: 0-6 months (HOT) | 6-12 months (WARM) | 12+ months (COOL)
├─ Review Sentiment: 
│   ├─ Positive (5 stars): Praise, nothing to steal, but figure out the buyer business to replicate the buyer business later for the supplier (cause they are already buying from competition)
│   ├─ Mixed (3-4 stars): Praise + one complaint = OPPORTUNITY + replicate the buyer business later for the supplier as a new buyer discovery (If not added before)
│   └─ Negative (1-2 stars): Severe problem = HIGH OPPORTUNITY + replicate the buyer business later for the supplier as a new buyer discovery (If not added before)
├─ Review Content Analysis:
│   ├─ What specific problem does the buyer mention?
│   │   ├─ Slow delivery? → Supplier speed leader advantage
│   │   ├─ Poor quality/specs? → Supplier customization advantage
│   │   ├─ Too expensive? → Supplier cost leader advantage
│   │   └─ Bad customer service? → Supplier service advantage
│   ├─ Does review mention company size, order volume, or use case?
│   │   └─ This helps us find the exact buyer contact to approach
│   └─ Review language analysis: Professional/B2B language? Yes = actual business buyer
├─ Opportunity Score: (Review Severity × Supplier Advantage Match × Recency)
│   ├─ 80-100: URGENT - Buyer unhappy, supplier has clear advantage, recent review
│   ├─ 60-79: WARM - Buyer has complaint, supplier can solve, somewhat recent
│   ├─ 40-59: COOL - Buyer complaint exists, supplier advantage unclear, older
│   └─ 0-39: COLD - No clear opportunity or too old
├─ Supplier Fit Score: Does supplier's operational strength (from Part 1.1) match buyer's complaint?
│   ├─ IF buyer complains "slow shipping" AND supplier = Speed Leader → +30
│   ├─ IF buyer complains "high price" AND supplier = Cost Leader → +25
│   ├─ IF buyer needs "custom specs" AND supplier = Quality/Customization → +30
│   └─ IF no match → +0
└─ Contact Extraction: Can we identify the buyer company name from review context?
    ├─ IF review mentions buyer's company name → Extract for outreach + replicate the buyer business later for the supplier as a new buyer discovery (If not added before)
    ├─ IF review mentions buyer's product/use case → Infer buyer industry + replicate the buyer industry later for the supplier as a new buyer discovery (If not added before)
    └─ This allows us to DIRECTLY suggest this buyer to supplier

**GOAL 2: Alert Supplier to Territorial Competitor Threats**

We monitor competitor activity in the supplier's licensed zone to notify of competitive pressure.

FOR COMPETITOR ACTIVITY:

├─ New Location Permits (in zone or adjacent): Company expanding footprint
├─ New Job Postings (in zone or adjacent): Sales/operations hiring = expansion
├─ New LinkedIn Updates: Product launches, facility expansions, partnership announcements
└─ Pricing Changes: Public price updates on competitor website

---

## 2.7: COMPETITOR BUYER-STEALING FORMULA

**Buyer Stealing Opportunity Score:**

```
Opportunity_Score = (Review_Severity × 0.35) + (Supplier_Fit × 0.30) + (Recency_Weight × 0.25) + (Buyer_Profile_Match × 0.10)
```

WHERE:

**Review_Severity** = Based on star rating and complaint severity
├─ 1-star with specific problem: 100
├─ 2-star with clear complaint: 80
├─ 3-star with one major complaint: 60
├─ 4-star with minor complaint: 30
└─ 5-star (no problem): 0

**Supplier_Fit** = Does supplier's operational strength solve buyer's complaint?
├─ Perfect match (supplier strength = buyer need): 100
├─ Good match (supplier strength addresses 70%+ of complaint): 75
├─ Partial match (supplier strength addresses 40-70% of complaint): 50
├─ Poor match (supplier strength doesn't address complaint): 0
└─ Default if no clear complaint: 30

**Recency_Weight** = How fresh is the review?
├─ 0-6 months: 100
├─ 6-12 months: 65
├─ 12-18 months: 40
└─ 18+ months: 15

**Buyer_Profile_Match** = Does buyer's size/industry match supplier's ideal customer?
├─ Perfect match (size + industry align with supplier portfolio seed): 100
├─ Good match (size matches or industry matches): 75
├─ No clear match: 30

**Output: Buyer Stealing Recommendations**

When Opportunity_Score ≥ 70, supplier sees:

═══════════════════════════════════════════════════════════════
COMPETITOR BUYER OPPORTUNITY

Competitor: XYZ Packaging Inc.
Their Buyer's Complaint: "Delivery took 4 weeks, we needed stock in 2 days"
Your Advantage: SPEED LEADER - Average 3-day delivery

Action Items:
├─ 🎯 Buyer Company: ABC Manufacturing (inferred from review)
├─ 📞 Find Contact: VP Operations (likely decision-maker)
├─ 💬 Pitch: "We know you had supply delays with XYZ. We deliver in 3 days. Sample ready Friday?"
├─ 📊 Confidence: 85% (recent review, clear need, perfect fit)
└─ 💰 Deal Size Est: $15K-$30K/year (based on buyer industry)

═══════════════════════════════════════════════════════════════

---

## 2.8: COMPETITOR TERRITORIAL ALERT SYSTEM

**What We Monitor (Per Zone):**

FOR COMPETITOR ACTIVITY:

├─ New Building Permits (Zone ± 5 miles):
│   └─ IF competitor opens new location = ALERT ("Competitor expanding nearby, increase presence")
├─ New Job Postings (Zone):
│   └─ IF competitor posts 2+ sales jobs = ALERT ("Competitor hiring sales team in your zone")
├─ Pricing Changes (Public website):
│   └─ IF competitor prices drop >10% = ALERT ("Competitor price pressure detected")
└─ New LinkedIn Updates:
    └─ IF competitor announces product line or partnership = ALERT ("New competitive offering")

**ALERT_SEVERITY:**
├─ RED: Competitor expansion in zone (new location, multiple hires)
├─ YELLOW: Competitor activity in adjacent zone (nearby threat)
└─ GREEN: Competitor activity outside zone (monitor only)

**Monthly Territorial Report for Supplier:**

═══════════════════════════════════════════════════════════════
ZONE COMPETITIVE PRESSURE REPORT - North Jersey (Stretch Wrap)

Current Status: 🟡 YELLOW - Moderate Pressure

Threats Detected:
├─ XYZ Packaging: New warehouse permit filed 15 miles away (building 30K sq ft facility)
│   └─ Action: Notify local customers of your capacity, offer expanded service area
├─ ABC Supplies: 2 new sales positions posted (zone)
│   └─ Action: Consider hiring +1 sales rep to match coverage
└─ DEF Materials: Price reduction 8% (public pricing)
    └─ Action: Review margins, consider promotional offer to key accounts

Buyer Stealing Opportunities: 12 this month
├─ 3 HIGH (Opportunity_Score 80+)
├─ 5 WARM (Opportunity_Score 60-79)
└─ 4 COOL (Opportunity_Score 40-59)

═══════════════════════════════════════════════════════════════

---

## 2.9: LAYER 2C - SUPPLIER'S CURRENT CUSTOMER PROFILE

**What We Find:**

FROM: Supplier's direct customer file upload + website + LinkedIn + news

├─ Supplier's current customer base file upload: OPTIONAL "Upload your customers to exclude them AND to teach us about who buys fastest."
├─ Customer logos displayed on site
├─ Testimonials mentioning company names (to clone the perfect buyer profile)
├─ LinkedIn connections (CEO connected to which companies?)
├─ Case studies naming customers
├─ News mentions: "Company X partners with [supplier]"
└─ Inferred customer list: Who are they likely selling to?

**Why This Matters:**
- **Gap analysis:** If supplier sells to Company A, and competitor sells to Company B, we prioritize Company B
- **Avoid duplication:** Don't recommend buyers they already have
- **Clone perfect buyer:** Use existing happy customers to find similar prospects

**Tools:**
- Website scraper (Apify OR Google)
- LinkedIn manual review (Phase 1)
- News API search for supplier mentions
- **CSV Upload:** Direct supplier import of current customer list

**Automation:** 75% (scraping automated, inference manual)

**Output:**
- **Current Customer List** (names, industries)
- **Perfect Buyer Persona** (inferred from happy customer profiles)
- Used to filter buyer recommendations (exclude existing customers)

---

# PART 3: SIGNAL AGGREGATION HUB (Layer 3B) {#part-3}

## **Unified Urgency, Velocity, Confidence, Alert Scoring**

### **Context:**

All signals from Layers 1-5 flow into this hub. We apply **weighted scoring** to produce buyer priority rankings.

**Weighting (Optimized):**
- **Government signals:** 35% (highest authority—permits, UCC, SBA loans)
- **Financial signals:** 20% (D&B, tax, bank activity)
- **Platform signals:** 25% (LinkedIn, social, website traffic, ad spend)
- **Compliance signals:** 20% (licenses, certifications, inspections)

---

## 3.1: URGENCY SCORE (0-100)

**Definition:** How soon does this buyer need packaging?

**High Urgency Signals (NEW EXPANSIONS):**

├─ Building permit issued (last 6 months): +7 to +9
├─ UCC filing (inventory collateral): +6 to +8
├─ Recent SBA loan (7a/504): +6 to +8
├─ LinkedIn hiring spree (5+ jobs posted): +5 to +7
├─ Website traffic spike (+100% in 30 days): +6 to +8
├─ Marketplace sales surge (Amazon/eBay/Etsy/Shopify reviews up 50%): +6 to +8
├─ Google reviews mentioning "packaging" or "shipping": +2
├─ Platform reviews with specific competitor complaints solved by supplier: +7 to +9
├─ Google/Meta/IG/TikTok Ad CREATIVE VOLUME SPIKE (5+ new creatives in 30 days): +7 to +9
├─ Google/Meta/IG/TikTok Ad BUDGET SPIKE (50%+ spend increase in 30 days): +7 to +9
├─ Social media mentions (new product launch): +3 to +5
└─ Seasonal Demand Signal (e.g., retail holiday hiring surge → packaging need): +4 to +6

**Negative Urgency Signals:**

├─ Active IRS tax lien: -5 (cash flow problem, low priority)
├─ Bankruptcy filing (active): -10 (avoid)
├─ Suspended business license: -8 (not operating)
├─ Very low credit score (D&B PAYDEX <30): -2
└─ Website down/inactive: -5 (dormant)

**Urgency Formula:**

```
Base Urgency = 50 (neutral)

Urgency Score = Base + Σ(Signal × Weight × Time Decay)

Time Decay (How fresh is the signal?):
  ├─ 0-6 months old: 100% strength
  ├─ 6-12 months old: 50% strength
  ├─ 12-18 months old: 25% strength
  └─ 18+ months old: 10% strength

Cap: 100 maximum
```

**EXAMPLES:**
├─ Building permit 3 months ago: 50 + (8 × 1.0) = 58 (base + fresh signal)
├─ Ad spend spike 2 weeks ago: 50 + (8 × 1.0) + (8 × 1.0) = 66 (multiple fresh signals)
└─ Google reviews mention 8 months ago: 50 + (2 × 0.5) = 51 (stale signal, minimal boost)

**Output:**
- **Urgency Score (0-100)** per buyer
- Used to rank buyers: High urgency = deliver first

---

## 3.2: VELOCITY SCORE (0-100)

**Definition:** How fast is this buyer growing?

**High Velocity Signals:**

├─ UCC filing (inventory/equipment): +7 to +9
├─ Recent SBA loan: +7 to +9
├─ LinkedIn hiring spree: +7
├─ Facility square footage increase: +5 to +7
├─ Property value up 20%+ YoY: +5 to +7
├─ Multiple refinancing events (12 months): +7
├─ Marketplace review growth (+50% MoM): +6 to +8
├─ Social follower growth (+50% MoM): +5 to +7
├─ Tax lien resolved (sign of recovery): +3 to +5
├─ Google/Meta/IG/TikTok Ad creative volume spike: +7
├─ Google/Meta/IG/TikTok Ad budget spike: +7
├─ New product launch announcements: +4 to +6
└─ Seasonal Demand Ramp (retail hiring Oct-Dec → Q1 inventory building): +5 to +7

**Velocity Formula:**

```
Velocity Score = Σ(Growth Signal × Weight)

Interpretation:
  ├─ 80-100: Aggressive scaling (hockey stick growth)
  ├─ 60-79: Strong growth trajectory
  ├─ 40-59: Moderate growth
  ├─ 20-39: Stable/early stage
  └─ 0-19: Declining/dormant
```

**Output:**
- **Velocity Score (0-100)** per buyer
- High velocity = future volume potential (prioritize for whale hunters)

---

## 3.3: CONFIDENCE LEVEL (0-100%)

**Definition:** How reliable is our data?

**Confidence Boosters:**

├─ Active business license verified: +2
├─ ISO 9001 certified: +1
├─ Clean inspection record (OSHA/EPA): +1
├─ D&B PAYDEX score 80+: +3
├─ D&B PAYDEX improving (12-month trend): +3
├─ Tax lien resolved: +2
├─ Forgiven PPP loan: +2
├─ Multiple data sources confirm (3+ sources agree): +5
└─ Recent data (<30 days old): +3

**Confidence Reducers:**

├─ Missing business license: -5
├─ No D&B record: -10
├─ Recent OSHA violation (unresolved): -3
├─ Data older than 30 days: -2
├─ Conflicting signals (LinkedIn says 50 employees, SoS says 5): -5
└─ Website unreachable: -7

**Confidence Formula:**

```
Base Confidence = 80%

Confidence = Base + Boosters - Reducers

Min: 40% | Max: 100%

Interpretation:
  ├─ 90-100%: Verified, reliable data
  ├─ 75-89%: Good confidence, minor gaps
  ├─ 60-74%: Moderate confidence, some gaps
  └─ <60%: Low confidence, significant gaps (flag for manual review)
```

**Output:**
- **Confidence % per buyer**
- Low confidence = manual review before delivery to supplier

---

## 3.4: ALERT ASSESSMENT (RED/YELLOW/GREEN)

**Definition:** Payment risk + operational risk combined.

**Red Flags (High Alert):**

├─ Active bankruptcy filing
├─ Active IRS tax lien
├─ Multiple judgments (3+ in last 2 years)
├─ Business license revoked/suspended
├─ D&B PAYDEX <30 (chronic late payer)
└─ Multiple active OSHA violations

**Yellow Flags (Moderate Alert):**

├─ Recent lien (1-2 years old, now resolved)
├─ D&B PAYDEX 50-70 (marginal payer)
├─ Late tax filing pattern
├─ Recent OSHA violation (resolved)
└─ Declining website traffic (-50% YoY)

**Green Light (Low Alert):**

├─ Clean legal record
├─ D&B PAYDEX 80+
├─ Active business license
├─ Clean inspection record
└─ Growing trajectory

**Output:**
- **Alert Level:** RED / YELLOW / GREEN
- **Recommended Terms:**
  - RED = Prepayment required / Proceed with caution
  - YELLOW = Net 30, require deposit
  - GREEN = Net 60+, standard terms

---

## 3.5: FINAL BUYER INTELLIGENCE CARD (Output)

**What Supplier Sees:**

═══════════════════════════════════════════════════════════════
BUYER: Acme Manufacturing Inc.
Location: Newark, NJ (North Jersey Zone)
Industry: Food & Beverage Packaging
═══════════════════════════════════════════════════════════════

📊 INTELLIGENCE SUMMARY:
├─ Urgency Score: 87/100 (🔥 HOT - Recent expansion)
├─ Velocity Score: 72/100 (📈 Strong Growth)
├─ Confidence Level: 91% (✅ Verified)
└─ Alert Level: 🟢 GREEN (Reliable payer)

💼 BUSINESS PROFILE:
├─ Employees: 25-50 (growing)
├─ Revenue Estimate: $2M-$5M
├─ Facility Size: 45,000 sq ft (warehouse)
└─ Packaging Volume Estimate: 500-800 boxes/week

🎯 KEY SIGNALS:
├─ ✅ Building permit issued 4 months ago ($120K expansion)
├─ ✅ SBA 7(a) loan secured ($250K, 6 months ago)
├─ ✅ LinkedIn: 8 new job postings (warehouse staff, ops manager)
├─ ✅ Google reviews: 15 new reviews mentioning "fast shipping"
├─ ✅ Meta Ads Library: 6 new ad creatives in last 30 days (scaling demand)
└─ ✅ D&B PAYDEX: 85 (pays on time)

💡 RECOMMENDED APPROACH:
├─ Contact: John Doe, VP Operations (email: john@acme.com)
├─ Your Advantage: [Pulled from non-generic onboarding answer, e.g., "Sample-based sales"]
├─ Offer: Sample shipment (your strength: 60% close rate on samples)
├─ Pitch: "We see you're expanding. Let's cut your packaging costs 30%."
├─ Terms: Net 60 (low alert level)
└─ Follow-up: Call in 1 week after sample delivery

📞 CONTACT INFO:
├─ Main: (973) 555-1234
├─ Direct: john@acme.com (VP Operations)
└─ LinkedIn: linkedin.com/in/johndoe

═══════════════════════════════════════════════════════════════

**This card is delivered to supplier in dashboard.**

---

# PART 4: GOVERNMENT RECORDS (Layer 4A) {#part-4}

## **80%+ Automation | Highest Authority Weight (35%)**

### **Context:**

Government data is the **most reliable** signal. If a permit is filed, a loan is issued, or a lien is released, it's **factual**, not inferred.

**Phase 1 Approach:** Manual lookups (free/low-cost), secretary of state + basic court records  
**Phase 2 Approach:** Full API automation ($800-2,900/month)

---

### **Sub-Layers (4.1-4.6):**

**4.1: Secretary of State Registration**
- Business legal name, status (Active/Suspended/Dissolved), incorporation date, officer names, DBA names
- **Signal:** Active status = +2 confidence | Suspended = RED flag | Recent filing = possible new entrant

**4.2: Federal & State Court Records**
- Bankruptcy filings, IRS tax liens, SBA liens, civil judgments
- **Signal:** Active bankruptcy = RED (-10 urgency) | Resolved lien = +3 velocity (recovery) | Clean record = +2 confidence

**4.3: Building Permits & Property Records**
- Facility expansion permits, square footage change, property assessment trends
- **🔥 CRITICAL:** Building permit (last 6 months) = +7 to +9 urgency (packaging need incoming)
- **Volume estimation:** Facility size = packaging volume proxy (10K sq ft = 20-50 boxes/week)

**4.4: UCC Financing Statements**
- Inventory or equipment collateral filed (shows financing for expansion)
- **🔥 CRITICAL:** Recent UCC filing = +6 to +8 urgency + +7 to +9 velocity (company scaling)

**4.5: Trade Name Registrations**
- DBA names, name change history (strategic pivots, rebranding)
- **Signal:** Recent name change = note for research (possible market shift)

**4.6: Environmental & Regulatory Compliance**
- OSHA violations, EPA compliance status, health inspections
- **Signal:** Clean record = +1 confidence | Recent unresolved violation = -3 confidence

**Tools (Phase 1):** Free SoS websites (manual), PACER (federal courts), county/state databases  
**Tools (Phase 2):** SoS bulk APIs ($100-500/month), UniCourt/CourtListener ($200-800/month), BuildFax ($300-800/month)

**Cost:** Phase 1 $0-50/lookup | Phase 2 $300-1,000/month

---

# PART 5: FINANCIAL INTELLIGENCE (Layer 5A) {#part-5}

## **85%+ Automation | 20% Weight**

### **Context:**

Financial data answers: **Can they pay? Are they growing?** Critical for alert assessment and velocity scoring.

---

### **Sub-Layers (5.1-5.4):**

**5.1: Business Credit Score & Payment History (D&B)**
- PAYDEX score (0-100), payment index, credit limit recommendations, payment trend
- **Signal:** PAYDEX 80+ = safe terms (Net 60+) | PAYDEX 30-49 = RED alert | Improving trend = +3 velocity

**5.2: SBA Loan & Financing History**
- Recent SBA 7(a) loans (working capital), SBA 504 (equipment), PPP forgiveness status
- **🔥 CRITICAL:** Recent SBA loan = +6 to +8 urgency + +7 to +9 velocity (expansion capital confirmed)

**5.3: Tax Filing Patterns**
- IRS lien status, state tax lien status, filing consistency
- **Signal:** Active IRS lien = RED (-5 urgency, severe cash flow) | Resolved lien = +4 velocity (recovery)

**5.4: Business Bank Account Proxies**
- Active Stripe/Square/PayPal accounts, e-commerce platform usage, payment processor adoption
- **Signal:** Multiple payment processors = +6 velocity (multi-channel sales growth)

**Tools:** D&B API ($20-100/month), SBA loan database (free), IRS lien database (free, manual)

**Cost:** Phase 1 $20-100/month | Phase 2 $50-200/month

---

# PART 6: COMMERCIAL REAL ESTATE INTELLIGENCE (Layer 5B) {#part-6}

## **70%+ Automation | Capacity Estimation Focus**

### **Context:**

**Facility size = packaging volume.** A 10K sq ft warehouse needs 20-50 boxes/week. A 100K sq ft facility needs 5,000+ boxes/week. This is a **direct revenue multiplier**.

---

### **Volume Estimation Formula:**

```
10K sq ft = 20-50 boxes/week = $3K-$10K/year packaging spend
50K sq ft = 500-1,000 boxes/week = $50K-$150K/year
100K sq ft = 5,000+ boxes/week = $500K-$1M+/year

Refined Estimation (considering buyer industry):
├─ E-commerce (high packaging need): Multiply by 1.5×
├─ 3PLs/Warehousing (high packaging need): Multiply by 1.6×
├─ Manufacturing (moderate need): Multiply by 1.0×
├─ Transportation/storage (High packaging need): Multiply by 1.5×
├─ Other packaging companies (High packaging need): Multiply by 1.45x
├─ Food & Beverage (high packaging need): Multiply by 1.3×
└─ Pharmaceutical (low volume, high specs): Multiply by 0.6×
```

**Signals Generated:**
- Building permit + facility expansion = +7 to +9 urgency (expansion phase)
- Property value up 20%+ YoY = +5 velocity (facility upgrade)
- New larger facility acquisition = +7 urgency (capacity scaling)

**Tools:** County assessor (free, Phase 1) | CoStar API ($300-1,000/month, Phase 2)

**Cost:** Phase 1 $0 | Phase 2 $300-1,000/month

---

# PART 7: LICENSING & COMPLIANCE (Layer 5C) {#part-7}

## **75%+ Automation | Legitimacy Confirmation**

### **Context:**

Confirms buyer is **legally operating** and **compliant**. Critical for confidence scoring.

---

### **Coverage:**

- **Active Business License Verification:** Status (Active/Expired/Suspended), issue/expiration dates
  - **Signal:** Active = +2 confidence | Expiring soon = YELLOW flag
- **Industry-Specific Certifications:** ISO 9001, FEMA/HAZMAT, food safety certifications
  - **Signal:** ISO certified = +1 confidence (quality-focused)
- **Inspection Records:** OSHA violations, EPA compliance, health department inspections
  - **Signal:** Clean record = +1 confidence | Active violations = -3 confidence

**Tools:** City/county license databases (free) | OSHA database (free) | EPA enforcement (free)

**Cost:** Phase 1 $5-25/lookup | Phase 2 $100-400/month

---

# PART 8: GHOST as well as COMPETITOR COMPANY DETECTION (Premium Add-On for ghost companies, but also used for competitor company detection from all platforms to check and hunt for reviews, sentiments, and also check if the competitor is present on any of the platforms to check the reviews and hunt for buyers, Same competitor discovery/buyer discovery strategy applies for in here, as we covered earlier above) {#part-8}

## **The "Invisible Market" Layer**

### **Context:**

Ghost companies are **$500K-$3M revenue businesses** operating from residential addresses, shared spaces, 3PLs, or rented facilities. They're invisible to traditional B2B databases but buy **$3K-$8K packaging/year** and pay fast.

**Why Suppliers Want Them:**
- Low competition (competitors don't find them)
- Cash flow customers (small, frequent orders)
- More ghost companies exist than visible companies

**Pricing Model:**
- **Base license:** $2,000/month (visible companies only)
- **Ghost add-on:** +$500-$1,000/month (adds 10-20 ghost buyers/month)

---

### **Detection Methodology:**

**8.1: E-Commerce Platform Detection**
- Shopify stores, WooCommerce, BigCommerce, Wix, Squarespace
- **Signal:** Active Shopify store + 50+ products = 50-200 boxes/month estimate

**8.2: Amazon FBA/FBM Seller Detection**
- Seller storefront lookup, product count, review analysis
- **Signal:** 100+ products + 500+ reviews = 500-1,000 boxes/month estimate (FBA prep)

**8.3: Etsy Seller Detection**
- Shop URL, product listings, review count, shipping origin
- **Signal:** 1,000+ sales = 100-300 boxes/month estimate

**8.4: Ad Spend Inference**
- Meta Ads Library, Google Ads transparency, TikTok Ads Library
- **Signal:** 10+ active Meta ads = $100-300/day spend = 50-150 boxes/week estimate

**8.5: Building-by-Building Scan**
- Zone boundaries, filter for business signals (Google Maps, SoS, LinkedIn, USPS), cross-match with e-commerce platforms
- **Output:** 5,000-8,000 ghost companies per zone, 10-20 delivered/month to supplier

**Tools:** BuiltWith API ($50/mo) | Jungle Scout ($50/mo) | Keepa ($20/mo) | Manual Apify scraping ($100/mo)

**Cost:** Phase 2 $180-500/month for ghost layer

---

# PART 9: DATA REFRESH CYCLES {#part-9}

## **How Often We Update Each Layer**

### **Refresh Schedule:**

**Daily Refresh (Real-Time Signals):**
- LinkedIn job postings, company updates, follower count
- Google Reviews new reviews, mentions
- Social media follower growth (Facebook, Instagram, Twitter)
- News API press releases
- Ad spend (Meta/Google Ads Library)

**Weekly Refresh (Government & Legal):**
- Secretary of State status changes, new filings
- Court records (liens, judgments, bankruptcies)
- UCC filings
- Building permits
- Business licenses
- Environmental compliance

**Monthly Refresh (Financial & Real Estate):**
- D&B PAYDEX updates
- SBA loans issued
- Property assessments, lease expirations
- Tax liens

**Quarterly Refresh (Compliance):**
- ISO certifications
- OSHA inspections
- EPA compliance
- Health department inspections

**Data Staleness Penalties:**

```
Data <7 days old: No penalty
Data 7-30 days old: -2 confidence
Data 30-90 days old: -5 confidence
Data >90 days old: -10 confidence (flag for manual refresh)
```

---

# PART 10: BUYER PRIORITIZATION LOGIC (UPDATED) {#part-10}

## **Lowest Hanging Fruit Ranking + Capacity-Based Delivery**

### **Context (V3 Update):**

Buyer prioritization now considers **supplier's calculated operational capacity** (from Section 1.4). We deliver the number of buyers they can actually handle, not an arbitrary 50/month.

---

### **Prioritization Formula:**

```
Prioritization Score = (Urgency × 0.4) + (Velocity × 0.2) + (Deal Size × 0.2) + (Confidence × 0.1) + (Supplier Fit × 0.1)
```

**EXAMPLE RANKING:**
├─ Buyer A: 87 (High urgency 85, strong signals, $20K deal, high confidence)
├─ Buyer B: 82 (Moderate urgency 75, high velocity 80, $50K deal)
└─ Buyer C: 75 (High urgency 80, low confidence 65, $5K deal)

---

### **DELIVERY CADENCE (Capacity-Based, NEW):**

**OLD MODEL (V2):** Always deliver 50 buyers/month regardless of supplier size

**NEW MODEL (V3):** Deliver based on calculated capacity from Section 1.4

```
Recommended_Buyers_Per_Month = From Section 1.4 Capacity Calculation

IF Recommended_Buyers <= 50
  THEN Weekly_Delivery = 12-13 buyers/week (evenly distributed)

IF Recommended_Buyers 51-100
  THEN Weekly_Delivery = 25 buyers/week

IF Recommended_Buyers 101-250
  THEN Weekly_Delivery = 60 buyers/week

IF Recommended_Buyers 251+
  THEN Weekly_Delivery = 250 buyers/week (capped at 1000/month max)

// Distribute by priority score
Week 1: Top 25% (highest priority scores)
Week 2: Next 25%
Week 3: Next 25%
Week 4: Final 25%
```

**Example (Supplier with 96 buyers/month capacity):**

```
Total monthly delivery: 96 buyers
Weekly delivery: 24 buyers/week

Week 1: 24 buyers (Priority Score 85-100)
Week 2: 24 buyers (Priority Score 75-84)
Week 3: 24 buyers (Priority Score 65-74)
Week 4: 24 buyers (Priority Score 55-64)
```

---

### **URGENCY-BASED ACCELERATION (Unchanged):**

```
IF new buyer with Urgency >90 discovered mid-month
  THEN push out-of-cycle immediately
  NOTIFY: "🔥 HOT LEAD: Building permit issued 2 weeks ago"
```

---

### **TWEAK WHEEL ADJUSTMENTS (NEW):**

**Suppliers can adjust their monthly delivery volume via dashboard tweak wheel.**

```
IF Supplier selects "Up to 100 buyers/month" tier
  THEN Tweak Wheel Range = 50-150 buyers/month
  Base Price = $120/day
  
  IF Supplier adjusts to 75 buyers
    THEN Pro-rate: $120/day × (75/100) = $90/day
  
  IF Supplier adjusts to 125 buyers
    THEN Pro-rate: $120/day × (125/100) = $150/day (capped at next tier price)
```

**Dashboard Tweak Wheel Interface:**

═══════════════════════════════════════════════════════════════
YOUR MONTHLY BUYER DELIVERY

Current: 96 buyers/month at $120/day

[<———————————●—————————>]
50          100        150

Adjust your delivery volume anytime. Price adjusts automatically.

- Less buyers = Lower price (if you're overwhelmed)
- More buyers = Higher price (if you're ready to scale)

═══════════════════════════════════════════════════════════════

---

# PART 11: KYB VERIFICATION WORKFLOW {#part-11}

## **Bidding Pool Gatekeeper with Monetization**

### **Context:**

When a zone is full, competitors join the **bidding pool** to claim the zone when it becomes available. We verify they're **real, legitimate competitors**—not bad actors, resellers, or fake companies.

**CRITICAL ADDITION:** Bidders must pay **$100 deposit** to join, with visibility to **current highest bid**.

---

### **KYB Requirements (Phase 1):**

**Verification Checklist:**

1. **WEBSITE AGE CHECK**
   ├─ Requirement: Website must be 1+ year old
   └─ Exception: Website <1 year BUT SoS registration >3 years = OK

2. **BUSINESS REGISTRATION CHECK**
   ├─ Requirement: Active status in SoS database
   └─ Red flag: Suspended/Dissolved = REJECT

3. **PRODUCT MATCH CHECK**
   ├─ Requirement: Bidder sells same product as zone
   └─ Exception: Multiple products, one matching = OK

4. **TAX FILING CHECK**
   ├─ Requirement: No active IRS tax liens
   └─ Red flag: Active lien = REJECT

5. **CONTACT VERIFICATION**
   ├─ Requirement: Valid business email (not Gmail/Yahoo)
   └─ Red flag: Personal email = require upgrade to proceed

6. **DEPOSIT PAYMENT**
   ├─ Requirement: $100 minimum deposit to join bidding pool
   └─ Refundable IF bid is not won (goes to winner's first month billing if they win)

---

### **Verification Flow:**

```
Bidder submits: Company name, website, product, email, deposit payment ($100)
  ↓
Step 1: Validate deposit payment
  ↓
Step 2: Crawl website → Extract products
  ↓
Step 3: Check SoS: Is business active?
  ↓
Step 4: Check website age: >1 year?
  ↓
Step 5: Check tax liens: Any active?
  ↓
IF all pass → Verified ✅ (allow to join bidding pool, show current highest bid)
IF any fail → Manual review OR reject (refund deposit)
```

---

### **Bidding Pool Display (To Bidders):**

═══════════════════════════════════════════════════════════════
BIDDING POOL: North Jersey - Stretch Wrap
Current Highest Bid: $2,150/month (by XYZ Packaging Inc.)
Your Deposit: $100 (will be applied to first month if you win)

Your Bid: $__________ /month 

Note: Minimum bid is $100 above current highest ($2,250 minimum)

═══════════════════════════════════════════════════════════════

---

### **Disqualification Triggers:**

**Payment Default (6-month ban):**
```
Bidder wins zone → Doesn't pay within 14 days
Ban: 6 months before allowed to bid again
Deposit: Forfeited
```

**Fraud/Misrepresentation (Permanent ban):**
```
Claimed to sell Product X → Website shows Product Y
Fake business registration
Deposit: Forfeited
Ban: Permanent
```

**Competitor Intel Scraping (Permanent ban):**
```
Bidder signs up, accesses competitor data, immediately cancels
Deposit: Forfeited
Ban: Permanent + legal action
```

---

# PART 12: CAPACITY-BASED PRICING LOGIC (UPDATED) {#part-12}

## **Pricing Tiers = Calculated Capacity (Not Claims)**

### **Context (V3 Update):**

**OLD MODEL (V2):** Base price $2,000/month for 30-50 buyers, with bidding pool pressure increasing price.

**NEW MODEL (V3):** Pricing tiers based on **calculated operational capacity** (Section 1.4), with flexible tweak wheel for suppliers to adjust delivery volume.

---

### **PRICING STRUCTURE (UPDATED):**

**Primary Zone License (Capacity-Based Tiers):**

```
TIER 1: "Up to 50 Buyers/Month"
├─ Price: $2,000/month ($66/day)
├─ Includes: 30-50 buyer intelligence reports/month
├─ Includes: Competitor intelligence
├─ Includes: Territorial alerts
├─ Includes: Buyer stealing opportunities
├─ Tweak Wheel Range: 20-75 buyers/month
└─ Target Supplier: Small operations, 1-2 salespeople, $500K-$2M revenue

TIER 2: "Up to 100 Buyers/Month"
├─ Price: $3,600/month ($120/day)
├─ Includes: 50-100 buyer intelligence reports/month
├─ Includes: All Tier 1 features
├─ Tweak Wheel Range: 50-150 buyers/month
└─ Target Supplier: Growing operations, 2-4 salespeople, $2M-$5M revenue

TIER 3: "Up to 250 Buyers/Month"
├─ Price: $7,200/month ($240/day)
├─ Includes: 100-250 buyer intelligence reports/month
├─ Includes: All Tier 2 features
├─ Tweak Wheel Range: 150-350 buyers/month
└─ Target Supplier: Scaling operations, 5-10 salespeople, $5M-$15M revenue

TIER 4: "Up to 1000 Buyers/Month"
├─ Price: $13,500/month ($450/day)
├─ Includes: 250-1000 buyer intelligence reports/month
├─ Includes: All Tier 3 features
├─ Includes: Dedicated account manager
├─ Tweak Wheel Range: 500-1000 buyers/month (capped)
└─ Target Supplier: Enterprise operations, 10+ salespeople, $15M+ revenue
```

**Add-On Zone License:**
```
Additional Zone (Same Product, Different Geography):
├─ Price: $1,000-$1,500/month (per additional zone)
├─ Discount: 3+ zones = 10% off each add-on zone
└─ Includes: All features of primary zone
```

**Ghost Intelligence Add-On:**
```
Ghost Company Detection Layer:
├─ Price: +$500-$1,000/month (on top of base tier)
├─ Adds: 10-20 ghost buyers/month
├─ Includes: E-commerce detection, Amazon FBA, Etsy, ad spend inference
└─ Optional: Available for any tier
```

**Bidding Pool Deposit:**
```
Entry Fee: $100 (refundable to winner's first billing, forfeited if lost)
```

---

### **TIER ASSIGNMENT LOGIC:**

**Automatic Tier Recommendation (From Section 1.4):**

```
Recommended_Buyers_Per_Month = Calculated in Section 1.4

IF Recommended_Buyers <= 50
  THEN Assign_Tier = "Tier 1: Up to 50 buyers at $66/day"

IF Recommended_Buyers 51-100
  THEN Assign_Tier = "Tier 2: Up to 100 buyers at $120/day"

IF Recommended_Buyers 101-250
  THEN Assign_Tier = "Tier 3: Up to 250 buyers at $240/day"

IF Recommended_Buyers 251+
  THEN Assign_Tier = "Tier 4: Up to 1000 buyers at $450/day"
```

**Example (From Section 1.4):**

```
Supplier: $5M revenue, 2 salespeople, sample-driven sales
Calculated Capacity: 96 buyers/month
Assigned Tier: "Up to 100 buyers" at $3,600/month ($120/day)
```

---

### **TWEAK WHEEL PRICING ADJUSTMENTS:**

**How It Works:**

```
Supplier starts at recommended tier (e.g., "Up to 100 buyers")
Dashboard includes tweak wheel to adjust delivery volume within range

Tweak Range for "Up to 100 buyers" tier: 50-150 buyers/month
Base Price: $120/day

IF Supplier adjusts DOWN to 75 buyers:
  Pro-Rate Factor = 75 / 100 = 0.75
  Adjusted Price = $120 × 0.75 = $90/day
  
IF Supplier adjusts UP to 125 buyers:
  Pro-Rate Factor = 125 / 100 = 1.25
  Adjusted Price = $120 × 1.25 = $150/day
  (Note: Capped at Tier 3 starting price of $240/day to avoid tier overlap)

IF Supplier wants >150 buyers:
  Prompt: "You're ready for Tier 3! Upgrade to 'Up to 250 buyers' at $240/day"
```

**Dashboard UI:**

═══════════════════════════════════════════════════════════════
YOUR PLAN: Up to 100 Buyers/Month

Current Delivery: 96 buyers/month
Current Price: $3,600/month ($120/day)

**Adjust Your Delivery:**

[<———————————●—————————>]
50          100        150

- 50 buyers: $1,500/month ($50/day)
- 75 buyers: $2,700/month ($90/day)
- 100 buyers: $3,600/month ($120/day) ← Current
- 125 buyers: $4,500/month ($150/day)
- 150 buyers: $5,400/month ($180/day)

Need more than 150? Upgrade to "Up to 250 buyers" tier at $240/day

═══════════════════════════════════════════════════════════════

---

### **PRICE INCREASE TRIGGER (Bidding Pool Pressure):**

**OLD MODEL (V2):** Bidding pool size increases price for current licensee.

**NEW MODEL (V3):** Bidding pool creates **renewal price pressure**, but base tiers remain capacity-based.

```
BIDDING POOL SIZE THRESHOLDS:

0-3 bidders: No price increase (zone not competitive)
4-6 bidders: +$100/month at renewal (light competition)
7-9 bidders: +$200/month at renewal (moderate competition)
10-15 bidders: +$300/month at renewal (strong competition)
16-20 bidders: +$400/month at renewal (intense competition)
20+ bidders: +$500/month at renewal (maximum cap)

EXAMPLE:
├─ Year 1: 0 bidders → Tier 2 at $3,600/month
├─ Year 2: 8 bidders → Renewal at $3,800/month (+$200)
├─ Year 3: 14 bidders → Renewal at $4,100/month (+$300)
└─ Year 4: 25 bidders → Renewal at $4,500/month (+$400, capped)
```

**What Licensee Sees (Renewal Notice):**

═══════════════════════════════════════════════════════════════
RENEWAL NOTICE: North Jersey - Stretch Wrap

Your current price: $3,600/month
Renewal price (Year 2): $3,800/month (+$200)

**Why the increase?**
8 verified competitors are in the bidding pool for your zone.
This reflects the high demand for this territory.

**Your options:**
1. Renew at $3,800/month (secure your zone for another year)
2. Decline renewal (zone goes to highest bidder in pool)

Note: Current highest bid in pool is $4,000/month.
By renewing, you save $200/month vs. losing the zone.

═══════════════════════════════════════════════════════════════

---

### **REVENUE PROJECTIONS (V3 Model):**

**At Scale (50 Suppliers, 3 Zones, Mixed Tiers):**

```
Tier Distribution (Estimated):
├─ Tier 1 (Up to 50): 15 suppliers × $2,000 = $30,000/month
├─ Tier 2 (Up to 100): 20 suppliers × $3,600 = $72,000/month
├─ Tier 3 (Up to 250): 10 suppliers × $7,200 = $72,000/month
└─ Tier 4 (Up to 1000): 5 suppliers × $13,500 = $67,500/month

Ghost Add-On (30% take rate):
├─ 15 suppliers × $750 avg = $11,250/month

Bidding Pool Deposits:
├─ 100 bidders × $100 = $10,000 one-time (not recurring)

TOTAL MONTHLY REVENUE: $252,750/month
ANNUAL REVENUE: $3,033,000/year

Operating Costs (Phase 2, Full Automation):
├─ Tools/APIs: $15,000/month
├─ Labor: $10,000/month
└─ TOTAL COST: $25,000/month

GROSS MARGIN: 90.1% ($227,750 profit/month)
```

---

# PART 13: ZONE SEGMENTATION {#part-13}

## **Geography, Economics, Competitive Intensity**

### **Initial Target Zones (Proof of Concept - Q1 2026):**

**New Jersey (3 Primary Zones):**

1. **North Jersey Zone:** Northern counties (Bergen, Hudson, Essex, Union)
   - Market size: 2.8M population, ~15,000 packaging-using businesses
   - Competition: 25-30 major players
   - Entry cost: High (dense market, strong competition)
   - Recommendation: Start here (proven market demand, established competitors = buyers)

2. **Central Jersey Zone:** Central counties (Morris, Passaic, Somerset, Hunterdon)
   - Market size: 2.1M population, ~10,000 businesses
   - Competition: 15-20 major players
   - Entry cost: Medium
   - Recommendation: Second zone (moderate competition, easier to dominate)

3. **South Jersey Zone:** Southern counties (Camden, Burlington, Atlantic, Cape May)
   - Market size: 1.8M population, ~8,000 businesses
   - Competition: 12-18 major players
   - Entry cost: Medium-Low
   - Recommendation: Third zone (less dense competition, growth market)

**Expansion Plan (Q2-Q4 2026):**
- Pennsylvania (Philadelphia region, Pittsburgh region) = 3 zones
- New York (NYC metro, upstate) = 3 zones
- Connecticut (Fairfield County, rest of state) = 2 zones
- Massachusetts (Boston metro, Western MA) = 2 zones

**Total Addressable Market (by Year 2):**
- ~150 US geographic zones
- ~500K packaging-using businesses in target verticals
- ~$40B annual packaging spend

---

# PART 14: COST BREAKDOWN & RESOURCE ALLOCATION (UPDATED) {#part-14}

## **Phase 1 (Manual, 12 Weeks) & Phase 2 (Automated, 12 Weeks)**

### **Context (V3 Update):**

Cost structure now accounts for **variable delivery volumes** based on supplier capacity (not fixed 50 buyers/month).

---

### **Phase 1 Costs (Per Zone):**

**Monthly Operating Costs:**

**Tier 1 Data Sources (Highest ROI):**
├─ D&B PAYDEX: $20-50/month
├─ SimilarWeb API (free tier): $0
├─ Google Places/News API: $0
├─ Hunter.io: $50/month
└─ Subtotal: $70-100/month

**Tier 2 Data Sources:**
├─ WHOIS + Free SoS lookups: $0
├─ Free LinkedIn searches: $0
├─ Manual building permit research: $0 (time-intensive, ~40 hours/month)
├─ Manual court record lookups: $0 (time-intensive, ~30 hours/month)
└─ Subtotal: $0/month (labor cost only)

**TOTAL PHASE 1 TOOLS:** $70-100/month per zone  
**LABOR COST:** 70 hours/month × $30/hour = $2,100/month per zone  
**TOTAL PHASE 1:** $2,170-2,200/month per zone

**Buyer Delivery Cost (Variable by Tier):**

```
Cost Per Buyer Delivered = $2,170 / Buyers_Delivered_Per_Month

Tier 1 (50 buyers): $2,170 / 50 = $43.40/buyer
Tier 2 (100 buyers): $2,170 / 100 = $21.70/buyer
Tier 3 (250 buyers): $2,170 / 250 = $8.68/buyer
Tier 4 (1000 buyers): $2,170 / 1000 = $2.17/buyer

Gross Margin by Tier:
├─ Tier 1: $2,000 revenue - $2,170 cost = -$170 (loss at Phase 1)
├─ Tier 2: $3,600 revenue - $2,170 cost = $1,430 (66% margin)
├─ Tier 3: $7,200 revenue - $2,170 cost = $5,030 (70% margin)
└─ Tier 4: $13,500 revenue - $2,170 cost = $11,330 (84% margin)

Note: Tier 1 requires Phase 2 automation to be profitable.
```

---

### **Phase 2 Costs (Automated, Monthly):**

**Data API Stack:**

**Tier 1 (Must-Have):**
├─ D&B PAYDEX (at scale): $50-100/month
├─ SoS Bulk API: $200-500/month
├─ Court Records (UniCourt/CourtListener): $200-800/month
├─ BuildFax (permits): $300-800/month
└─ Subtotal: $750-2,200/month

**Tier 2 (Nice-to-Have):**
├─ CoStar (commercial real estate): $300-1,000/month
├─ Apollo.io (contact enrichment): $100/month
├─ LinkedIn Sales Navigator: $80/month
├─ Clearbit (company enrichment): $50/month
└─ Subtotal: $530-1,230/month

**Ghost Company Detection (Premium):**
├─ BuiltWith: $50/month
├─ Jungle Scout: $50/month
├─ Keepa: $20/month
├─ Apify (advanced scraping): $100-500/month
└─ Subtotal: $220-620/month

**AI Inference (GPT-4/Claude/Vertex):**
├─ Variable cost: $0.30/buyer × Buyers_Delivered_Per_Month
├─ Tier 1 (50 buyers): $15/month
├─ Tier 2 (100 buyers): $30/month
├─ Tier 3 (250 buyers): $75/month
└─ Tier 4 (1000 buyers): $300/month

**TOTAL PHASE 2 TOOLS:** $1,515-4,050/month + AI variable  
**LABOR COST:** 20 hours/month × $30/hour = $600/month (mostly QA, automated)  
**TOTAL PHASE 2 (Base):** $2,115-4,650/month per zone

**Buyer Delivery Cost (Phase 2, Variable):**

```
Cost Per Buyer Delivered = ($2,115 + AI_Cost) / Buyers_Delivered_Per_Month

Tier 1 (50 buyers): ($2,115 + $15) / 50 = $42.60/buyer
Tier 2 (100 buyers): ($2,115 + $30) / 100 = $21.45/buyer
Tier 3 (250 buyers): ($2,115 + $75) / 250 = $8.76/buyer
Tier 4 (1000 buyers): ($2,115 + $300) / 1000 = $2.42/buyer

Gross Margin by Tier (Phase 2):
├─ Tier 1: $2,000 revenue - $2,130 cost = -$130 (still slight loss, needs scale)
├─ Tier 2: $3,600 revenue - $2,145 cost = $1,455 (68% margin) ✅
├─ Tier 3: $7,200 revenue - $2,190 cost = $5,010 (70% margin) ✅
└─ Tier 4: $13,500 revenue - $2,415 cost = $11,085 (82% margin) ✅
```

**Margin Improvement Strategy:**

```
Tier 1 suppliers are loss leaders initially (or break-even in Phase 2).
Strategy:
├─ Use Tier 1 to acquire customers quickly
├─ Upsell to Tier 2-3 as they grow (capacity expansion)
├─ Most suppliers will naturally scale to Tier 2+ within 6-12 months
└─ 70%+ margin on Tier 2-4 offsets any Tier 1 losses
```

---

### **At Scale (50 Suppliers, 3 Zones, Mixed Tiers):**

**Revenue:**
```
Tier Distribution:
├─ Tier 1 (15 suppliers): $30,000/month
├─ Tier 2 (20 suppliers): $72,000/month
├─ Tier 3 (10 suppliers): $72,000/month
├─ Tier 4 (5 suppliers): $67,500/month
└─ Ghost Add-On (15 suppliers): $11,250/month

TOTAL REVENUE: $252,750/month ($3,033,000/year)
```

**Costs:**
```
Tool Cost (Phase 2, 3 zones): $4,650 × 3 = $13,950/month
Labor Cost (Phase 2, 3 zones): $600 × 3 = $1,800/month
AI Inference (avg $100/supplier): $100 × 50 = $5,000/month

TOTAL COST: $20,750/month ($249,000/year)
```

**Gross Margin:**
```
Profit: $252,750 - $20,750 = $232,000/month
Margin: 91.8%
Annual Profit: $2,784,000/year
```

---

# PART 15: IMPLEMENTATION ROADMAP {#part-15}

## **12-Week Phase 1 (Manual) + 12-Week Phase 2 (Automated)**

### **Phase 1: Proof of Concept (Weeks 1-12)**

**Weeks 1-3: Infrastructure Setup**
- [ ] Supplier onboarding system (value prop + portfolio + capacity calculation engine)
- [ ] Dashboard design (buyer cards, competitor alerts, territorial reports, tweak wheel UI)
- [ ] Data storage architecture (database schema for 9 layers + scoring + capacity profiles)
- [ ] QA/testing framework

**Weeks 4-6: Initial Data Collection**
- [ ] Recruit 3-5 pilot suppliers (North Jersey, stretch wrap)
- [ ] Run capacity calculations (Section 1.4) for each pilot
- [ ] Manual data collection (all 9 layers, variable buyers per supplier based on capacity)
- [ ] Confidence scoring assignment (manual validation of AI inferences)
- [ ] First buyer delivery (capacity-based volume per supplier)

**Weeks 7-9: Iteration & Refinement**
- [ ] Supplier feedback on buyer quality, accuracy, actionability
- [ ] Validate capacity calculations (did we deliver the right volume?)
- [ ] Refine competitor intelligence (test buyer-stealing methodology)
- [ ] Adjust signal weights based on close rate feedback
- [ ] Test tweak wheel UI (do suppliers adjust volumes?)
- [ ] Expand to 5-10 suppliers

**Weeks 10-12: Measurement & Optimization**
- [ ] Track supplier close rates, conversion, feedback
- [ ] Calculate buyer quality scores (% of "good fits" that convert)
- [ ] Identify and fix signal blind spots (missed opportunities, false positives)
- [ ] Validate pricing tiers (are margins accurate?)
- [ ] Document operational playbook for Phase 2 automation

### **Phase 2: Automation (Weeks 13-24)**

**Weeks 13-15: API Integration**
- [ ] Integrate D&B, SoS bulk API, court records, permits
- [ ] Build automated refresh pipelines (daily/weekly/monthly schedules)
- [ ] Implement scoring automation (urgency/velocity/confidence formulas)
- [ ] Automate capacity calculation engine (Section 1.4)
- [ ] QA on data quality, staleness penalties

**Weeks 16-18: Competitor Intelligence Automation**
- [ ] Automate competitor discovery (Google search + LinkedIn scraping)
- [ ] Implement buyer-stealing opportunity detection (review sentiment analysis)
- [ ] Build territorial alert system (competitive pressure scoring)
- [ ] Generate automated monthly competitive reports

**Weeks 19-21: Ghost Company Detection**
- [ ] Integrate Shopify, Amazon FBA, Etsy detection
- [ ] Build building-by-building scan automation
- [ ] Implement ad spend inference (Meta/Google/TikTok APIs)
- [ ] Deploy ghost buyer prioritization logic

**Weeks 22-24: Scale & Optimization**
- [ ] Onboard 20-30 suppliers across 3 NJ zones
- [ ] Monitor system performance (latency, accuracy, cost)
- [ ] Implement auto-scaling for data refresh pipelines
- [ ] Deploy tweak wheel UI for all suppliers
- [ ] Prepare for expansion to PA, NY, CT, MA

### **Success Metrics (End of Phase 2):**

- **System Automation:** 90%+ (only QA exceptions manual)
- **Data Accuracy:** 85%+ confidence average per buyer
- **Buyer Quality:** 70%+ "good fit" rate (supplier can close)
- **Supplier Satisfaction:** 4/5+ stars on usefulness
- **Cost Per Buyer:** <$25 (at scale, Phase 2)
- **Gross Margin:** >90%
- **Capacity Calculation Accuracy:** 80%+ (delivery volume matches supplier feedback)

---

## **KEY ENHANCEMENTS SUMMARY (V3 vs. V2)**

### **What's NEW in V3:**

1. **Operational Capacity Calculation Engine (Section 1.4):**
   - Independent revenue validation (D&B + LinkedIn + Google, hierarchical fallback)
   - AOV calculation (separated flow vs. whale for accuracy)
   - Purchase frequency analysis (monthly vs. quarterly vs. annual)
   - Close rate inference from sales process type (not asking directly)
   - Sales team time capacity calculation (50% buffer above current workload)
   - Minimum 50 buyers/month baseline regardless of size
   - Outputs: Recommended buyers/month + pricing tier assignment

2. **Enhanced Onboarding Questions (Section 1.1):**
   - Top 3 customer concentration analysis (whale dependency detection)
   - Flow vs. whale deal size definition (supplier-specific)
   - Purchase frequency questions (reorder cycles)
   - Sales process mapping with visual cards (close rate inference)

3. **Capacity-Based Pricing Tiers (Part 12):**
   - Tier 1: Up to 50 buyers at $2,000/month ($66/day)
   - Tier 2: Up to 100 buyers at $3,600/month ($120/day)
   - Tier 3: Up to 250 buyers at $7,200/month ($240/day)
   - Tier 4: Up to 1000 buyers at $13,500/month ($450/day)
   - Tweak wheel interface (flexible volume adjustment, pro-rated pricing)

4. **Capacity-Based Buyer Delivery (Part 10):**
   - Delivery volume = calculated capacity (not fixed 50/month)
   - Variable weekly delivery cadence (12-250 buyers/week)
   - Prioritization still uses urgency/velocity scoring

5. **Updated Cost Structure (Part 14):**
   - Variable cost per buyer (lower at higher tiers)
   - Margin analysis by tier (70-90% gross margin at Tier 2-4)
   - Tier 1 as loss leader/break-even (customer acquisition)

6. **Silent Conflict Handling:**
   - When supplier claims conflict with our data, use our data silently
   - No alerts to supplier about discrepancies (avoid confrontation)
   - Track confidence score decay internally

---

## **STATUS: 🟢 PRODUCTION-READY (V3)**

**Ready for implementation:**
- All intelligence layers defined and optimized
- All signals weighted and formulas complete
- **Operational capacity calculation engine fully specified**
- **Capacity-based pricing tiers designed with tweak wheel UI**
- All workflows mapped (onboarding → capacity calculation → buyer delivery → competitive alerts)
- All costs calculated (Phase 1 & Phase 2, variable by tier)
- Roadmap with weekly milestones

**Next Steps:**
1. ✅ Review Bundle 2 V3 completeness and capacity engine accuracy
2. → Build capacity calculation prototype (test with 3-5 pilot suppliers)
3. → Validate capacity formulas (does calculated volume match supplier reality?)
4. → Build tweak wheel UI prototype
5. → Begin Phase 1 pilot with 3-5 suppliers (North Jersey Stretch Wrap zone)

---

**END OF WARLORD BUNDLE 2 V3 - CAPACITY-OPTIMIZED**
