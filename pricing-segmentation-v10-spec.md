# PRICING & SEGMENTATION V10 - PRODUCTION SPECIFICATION
## How Suppliers Get Tiered & Priced

---

## 🎯 EXECUTIVE SUMMARY

**The Philosophy:**
We don't make assumptions about suppliers. We ask 2 critical questions, then segment everything else (pricing, features, buyer volume) based on their answers.

**The 2 Questions:**
1. **"What's your Minimum Order Value (MOV)?"** → Tells us who they're selling to
2. **"What's your Average Order Value (AOV)?"** → Tells us how much we should charge them

**Everything else** (company size, revenue, sensitivity, buyer volume recommendations) is deduced from public data.

---

# SECTION 1: ONBOARDING INTAKE QUESTIONS
## What We Ask Suppliers on Day 1

### **QUESTION 1: MINIMUM ORDER VALUE (MOV)**

```
"What's the smallest packaging order you typically handle?"

Example options:
└─ $10 - $50 (micro orders, hobby sellers)
└─ $50 - $500 (small e-commerce)
└─ $500 - $2,000 (growing brands)
└─ $2,000 - $10,000 (established brands)
└─ $10,000+ (enterprise/distributors)

OR: Custom text field for exact number
```

**What This Tells Us:**
- **MOV $10-50:** They're selling to "micro" buyers (price-sensitive, small teams)
  - Signal Sensitivity: EXTREME (tiny signals matter)
  - Decay Rate: Fast (7-14 days)
  - Our Approach: "Find bigger deals for you"

- **MOV $50-500:** They're selling to "small" e-commerce
  - Signal Sensitivity: HIGH
  - Decay Rate: Moderate (14-21 days)
  - Our Approach: Balanced intelligence

- **MOV $500-2K:** They're selling to "growing" brands
  - Signal Sensitivity: MEDIUM
  - Decay Rate: Longer (30 days)
  - Our Approach: Focus on mid-market buyers

- **MOV $2K+:** They're selling to "established" brands or enterprises
  - Signal Sensitivity: LOW (stable)
  - Decay Rate: Slow (45-60 days)
  - Our Approach: Enterprise-grade intelligence

---

### **QUESTION 2: AVERAGE ORDER VALUE (AOV)**

```
"What's your average packaging order value?"

Example options:
└─ $50 - $500
└─ $500 - $2,000
└─ $2,000 - $5,000
└─ $5,000 - $15,000
└─ $15,000+

OR: Custom text field for exact number
```

**What This Tells Us:**
- **AOV $50-500:** Low-ticket supplier
  - Monthly Buyer Volume Recommendation: 50-100 leads
  - Pricing Tier: $199/month (Tier 1)
  - Message: "Volume play - more leads, lower cost"

- **AOV $500-2K:** Mid-ticket supplier
  - Monthly Buyer Volume: 30-50 leads
  - Pricing Tier: $399/month (Tier 2)
  - Message: "Quality over quantity - verified buyers"

- **AOV $2K-5K:** High-ticket supplier
  - Monthly Buyer Volume: 15-30 leads
  - Pricing Tier: $699/month (Tier 3)
  - Message: "Enterprise intelligence - deep research"

- **AOV $5K-15K:** Very high-ticket
  - Monthly Buyer Volume: 10-20 leads
  - Pricing Tier: $999/month (Tier 4)
  - Message: "White-glove service - vetted opportunities"

- **AOV $15K+:** Enterprise
  - Monthly Buyer Volume: 8-15 leads
  - Pricing Tier: Custom (contact sales)
  - Message: "Bespoke intelligence - dedicated account"

---

### **OPTIONAL: GEOGRAPHIC FOCUS**

```
"What geographic regions are you targeting?"

Options:
└─ Single state (home state)
└─ Regional (5-state region)
└─ National (all 50 states)

Default: Home state
```

**Impact:**
- **Single State:** Base pricing
- **Regional:** +$100/month (building-by-building for 5 states)
- **National:** +$300/month (building-by-building for all states)

---

# SECTION 2: DEDUCED SUPPLIER TIER
## What We Determine from Public Data

Once supplier enters MOV/AOV, we scrape:

```
Supplier Company Data Collection:

1. Secretary of State Registration
   └─ Company revenue estimate (from business classification)
   └─ Number of employees (from LinkedIn data cross-ref)
   └─ Years in business

2. LinkedIn Company Profile
   └─ Employee count: 1-10 (startup) | 11-50 (small) | 51+ (established)
   └─ Employee growth trend (hiring spree = scaling)
   └┠ Job postings (vacancies indicate growth)

3. Financial Data (D&B)
   └┠ Estimated annual revenue
   └┠ PAYDEX score (payment reliability)
   └┠ Credit limit (bank confidence)

4. Website Data
   └┠ Website traffic (SEMrush/SimilarWeb proxy)
   └┠ Products offered (scope of business)
   └┠ Average product prices (AOV cross-check)

5. Marketplace Presence
   └┠ Shopify sales volume (if available via APIs)
   └┠ Amazon FBA ratings/volume
   └┠ eBay seller ratings

RESULT: Deduced Tier Classification
```

### **SUPPLIER TIER MATRIX**

| Tier | Annual Revenue | Employee Count | MOV Range | AOV Range | Pricing | Features |
|------|----------------|----------------|-----------|-----------|---------|----------|
| **Tier 1** | $400K-$1M | 1-5 | $10-$500 | $50-$500 | $199/mo | Basic buyer discovery |
| **Tier 2** | $1M-$3M | 5-15 | $50-$2K | $500-$2K | $399/mo | + Competitor buyers analysis |
| **Tier 3** | $3M-$10M | 15-50 | $500-$10K | $2K-$5K | $699/mo | + Building-by-building (1 city) |
| **Tier 4** | $10M+ | 50+ | $2K+ | $5K+ | $999/mo | + Multi-state building-by-building |

---

# SECTION 3: FEATURE GATES & UNLOCKS
## What Suppliers Get at Each Tier

### **TIER 1: "DISCOVERY" ($199/month)**

**Included:**
- ✅ Buyer Discovery (all sources)
- ✅ Basic Urgency Scores (0-100)
- ✅ 50-100 buyers/month recommended
- ✅ Daily data refresh
- ✅ Email notifications (daily digest)

**Locked Features:**
- ❌ Competitors' Buyer Intelligence (need Tier 2)
- ❌ Building-by-Building Analysis (need Tier 3)
- ❌ Feedback Card Optimization (basic only)

**Messaging:**
```
"We find growing companies in your space.
Start with Tier 1, see what works, expand from there."
```

---

### **TIER 2: "COMPETITIVE EDGE" ($399/month)**

**Included:**
- ✅ Everything from Tier 1
- ✅ **Competitors' Buyer Analysis**
  - "Which buyers are using your competitors?"
  - Import data cross-reference
  - Review mining for competitor weaknesses
  - Switching signals (dissatisfaction detection)
- ✅ 30-50 buyers/month recommended
- ✅ Competitor mapping dashboard

**Locked Features:**
- ❌ Building-by-Building (need Tier 3)

**Messaging:**
```
"Stop guessing. See exactly who your competitors are losing.
Call them. Win them."
```

---

### **TIER 3: "DOMINATION" ($699/month)**

**Included:**
- ✅ Everything from Tier 2
- ✅ **Building-by-Building Analysis (1 City Unlock)**
  - Free unlock for: Home state capital city OR supplier's home town
  - Map entire SAM in 1 geographic area
  - 100% coverage of potential buyers in zone
  - Confidence level: "$XM achievable revenue in your territory"
- ✅ 15-30 buyers/month recommended
- ✅ Advanced filtering (by facility size, growth rate, etc.)

**Locked Features:**
- ❌ Multi-State Building-by-Building (need Tier 4 or purchase)

**Messaging:**
```
"You'll never wonder 'am I missing buyers?' again.
Building-by-building analysis shows your entire market."
```

---

### **TIER 4: "SCALE" ($999/month)**

**Included:**
- ✅ Everything from Tier 3
- ✅ **Building-by-Building (Unlimited States)**
  - Unlock entire country SAM mapping
  - Focus on "hot zones" (you choose)
  - Confidence: "Here's 100% of viable buyers in every zone"
- ✅ 10-20 buyers/month recommended (quality focus)
- ✅ White-glove onboarding
- ✅ Custom reports
- ✅ Priority support

**Locked Features:**
- None (highest tier)

**Messaging:**
```
"You don't need 1,000 leads. You need the RIGHT 20.
We find them. We map them. We show you the whole market."
```

---

# SECTION 4: TIER EXPANSION MECHANICS
## How Suppliers Upgrade (Growth Loop)

### **TRIGGER: Supplier Asks to Expand**

```
Flow:

Supplier using Tier 1 sees:
"Want to unlock Competitors' Buyer Intelligence?"
[Yes, Upgrade] [Not Yet] [Learn More]

If [Yes, Upgrade]:
├─ Show Tier 2 features
├─ Confirm AOV (they may have grown)
├─ Show new monthly price ($399)
├─ 7-day free trial of Tier 2
└─ Auto-upgrade after 7 days (or cancel)
```

### **OPTIONAL: CITY-BY-CITY BUILDING UNLOCK**

```
Supplier using Tier 3 sees:
"Want to expand to neighboring states?"

Options:
├─ $300/mo: Add 5-state region
├─ $600/mo: Upgrade to multi-state (full Tier 4)
└─ $100/mo per additional city (pay-as-you-go)
```

---

# SECTION 5: VIRAL/REFERRAL LOOP
## The Incentive to Bring Competitors

### **THE PROBLEM**
Suppliers are naturally reluctant to bring competitors.
They see it as a threat, not an opportunity.

### **THE SOLUTION: UNLOCK PREMIUM FEATURES**

```
REFERRAL INCENTIVE STRUCTURE:

Supplier A brings Supplier B to platform

Supplier A gets:
├─ 30-day free access to Building-by-Building for 1 city
├─ OR: 1 month free Tier upgrade (Tier 1 → Tier 2)
├─ OR: Competitor Buyers Analysis enabled for free (1 month)
└─ Plus: Bragging rights ("You helped grow the community")

Supplier B (new referral) gets:
├─ 14-day free trial of their natural tier
├─ Priority onboarding
└─ First month at 50% discount
```

### **WHY THIS WORKS**
- Supplier A doesn't lose anything (trial period, no commitment)
- Supplier B gets value immediately
- We get a new customer with built-in trust
- Platform grows exponentially (network effects)

### **VIRAL MULTIPLIER**

```
Month 1: 10 suppliers
  └─ Average 2 referrals per supplier
  └─ = 20 new suppliers (30 total)

Month 2: 30 suppliers
  └─ Average 1.5 referrals per supplier
  └─ = 45 new suppliers (75 total)

Month 3: 75 suppliers
  └─ Growth slows (market saturation)
  └─ = 50 new suppliers (125 total)
```

---

# SECTION 6: PRICING STRATEGY BY SUPPLIER SIZE

### **THE COST STRUCTURE**

```
Per-Supplier Backend Costs:

1. Data APIs (fixed per supplier):
   └─ Secretary of State: $2/month
   └┠ News API: $5/month
   └┠ LinkedIn API: $3/month
   └┠ Government records (PACER, permits): $10/month
   └┠ D&B API: $20/month (bulk)
   └┠ Building permits/property: $15/month
   = ~$55/month base

2. Cloud Infrastructure (scales with volume):
   └┠ Cloud Functions (data refresh): $3-8/mo per supplier
   └┠ Firestore (database): $2-5/mo per supplier
   └┠ CDN (serving results): $1-2/mo per supplier
   = ~$8/month variable

3. Overhead (AI, support, etc):
   └┠ Per-supplier allocation: ~$20/month

TOTAL COST PER SUPPLIER: ~$83/month
```

### **MARGIN ANALYSIS**

| Tier | Price | Cost | Margin | Margin % |
|------|-------|------|--------|----------|
| Tier 1 | $199 | $83 | $116 | 58% |
| Tier 2 | $399 | $95 | $304 | 76% |
| Tier 3 | $699 | $110 | $589 | 84% |
| Tier 4 | $999 | $130 | $869 | 87% |

**Insight:** Higher tiers = more data required = slightly higher cost, but margins IMPROVE because price scales faster than cost.

---

# SECTION 7: SEGMENTATION PRESENTATION
## Same Data, Different Views (Per Tier)

### **THE PRINCIPLE: "All Buyers, Segmented Differently"**

```
Backend Process (Identical for all tiers):

Find 5,000 potential packaging buyers in USA
└┠ Run through urgency algorithm
└┠ Generate urgency scores (0-100)
└┠ Detect competitor intelligence
└┠ Flag red signals

RESULT: 5,000 buyers with full intelligence

Now we PRESENT differently:

Tier 1 Supplier:
  └┠ "50-100 buyers/month recommended"
  └┠ "Based on your MOV, here are buyers ready to buy"
  └┠ Shows: Top 50 by urgency score (Aggressive/Responsive)
  └┠ Hides: Competitor intel (teaser: "Upgrade for more")

Tier 2 Supplier:
  └┠ "30-50 buyers/month recommended"
  └┠ "Plus: See who your competitors are losing"
  └┠ Shows: Top 30 + all competitors' buyers (separate view)
  └┠ Hides: Building-by-building (teaser: "Upgrade for SAM analysis")

Tier 3 Supplier:
  └┠ "15-30 buyers/month recommended"
  └┠ "Plus: Full SAM map for 1 city"
  └┠ Shows: Top 15 + entire city SAM + competitor mapping
  └┠ Hides: Multi-state SAM (teaser: "Tier 4 for full country")

Tier 4 Supplier:
  └┠ "10-20 buyers/month recommended"
  └┠ "Plus: Entire country SAM mapping"
  └┠ Shows: Everything (top 10 + full national SAM + all competitor analysis)
  └┠ Nothing hidden
```

---

# SECTION 8: FEEDBACK CARD COLLECTION
## Gathering Data to Optimize Pricing

### **THE LOOP**

```
1. Supplier gets lead from us (Buyer X, "Aggressive" score 76)

2. Supplier reaches out (or doesn't)

3. 14 days later, we ask for feedback:
   └┠ "Did you close Buyer X?"
   └┠ "If not, why?"
   └┠ "How was the timing?"
   └┠ "Want more like this?"
   └┠ "Any other feedback?"

4. We analyze:
   └┠ "Aggressive" leads = X% close rate for Tier Y suppliers
   └┠ Pattern: Low MOV suppliers never close on Tier 1 leads
   └┠ Action: Create "Tier 1 Plus" with bigger deals only

5. Pricing optimization:
   └┠ If Tier 2 suppliers close at 65% rate, value is high → Keep price
   └┠ If Tier 1 suppliers close at 20% rate, value is low → Lower price
```

---

# SECTION 9: PRODUCTION CHECKLIST

- [ ] MOV/AOV intake questions implemented
- [ ] Tier classification logic based on deduced data
- [ ] Pricing tiers locked (Tier 1-4 with correct prices)
- [ ] Feature gates working (Tier 2 hides competitors, Tier 3 hides multi-state, etc.)
- [ ] Expansion flow working (Upgrade buttons functional)
- [ ] Building-by-building unlock (1 city free, additional cities $300+)
- [ ] Referral incentive tracking
- [ ] Feedback card collection automated
- [ ] Feedback analysis runs weekly
- [ ] Pricing adjustments (if needed) templated
- [ ] Margin calculations verified
- [ ] Viral loop metrics tracked (referral conversion rate)

---

# STATUS: 🟢 READY FOR CLAUDE AI CODE GENERATION

**All tiers defined. All features gated. All mechanics specified.**
