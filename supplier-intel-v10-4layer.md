# SUPPLIER INTELLIGENCE SYSTEM v10
## "The 4-Layer Reality" (Apify + Shipping + Social + Urgency)

---

## EXECUTIVE SUMMARY

**The Pivot:**
We are moving from "finding buyers" to **"owning the entire competitive intelligence supply chain."**

**The 4 Layers of Truth:**
1. **Buyer Discovery:** Who is buying packaging? (Base layer)
2. **Competitor Intelligence:** Who is your competitor selling to? (High value)
3. **Derived Demand:** Who is buying from your buyer? (Predictive)
4. **Urgency Scoring:** Who needs packaging RIGHT NOW? (Transactional)

**Legal Stance:**
- All data is inferred from public signals or legal commercial datasets.
- No hacking, no private email scraping, no trespassing.
- We use "Shadow Tracking" (inferred patterns) rather than illegal surveillance.

---

## LAYER 1: BUYER DISCOVERY (The Base)
*Who is buying packaging right now?*

### Data Sources (Automated via Apify + APIs)
1. **LinkedIn Hiring Signals:**
   - **Signal:** Hiring "Packaging Engineer", "Supply Chain Manager", "Logistics Coordinator".
   - **Inference:** Company is scaling operations = needs more packaging.
   - **Tool:** Apify LinkedIn Job Search Actor.

2. **Building Permits (County APIs):**
   - **Signal:** "New Warehouse Construction", "Facility Expansion", "Loading Dock Addition".
   - **Inference:** More physical space = more goods shipping = more packaging needed.
   - **Tool:** County API Aggregators / Scrapers.

3. **Government RFQs (SAM.gov / GovWin):**
   - **Signal:** Active solicitation for "Corrugated Boxes", "Poly Bags", "Shipping Supplies".
   - **Inference:** Direct, confirmed immediate need.
   - **Tool:** SAM.gov API.

4. **News & Press Releases (NewsAPI):**
   - **Signal:** "Series B Funding", "New Product Launch", "Opening New Distribution Center".
   - **Inference:** Growth capital deployed into inventory = packaging demand spike.
   - **Tool:** NewsAPI.

### Strategy
- **Goal:** Build the "Total Addressable Market" list.
- **Status:** 95% Automated.
- **Value:** Essential hygiene. Everyone needs this.

---

## LAYER 2: COMPETITOR INTELLIGENCE (The Goldmine)
*Who is your competitor selling to?*

**The Challenge:** We cannot legally track GPS of competitor trucks without consent.
**The Solution:** "Shadow Tracking" via Proxy Signals.

### Methodology 1: The "Review & Social" Shadow
*If a competitor sells to a brand, that brand often leaves a digital footprint.*

1. **Review Mining (The "Amazon/Etsy/Shopify" Loop):**
   - **Technique:** Monitor reviews on competitor's Google Maps / Trustpilot / Yelp profiles.
   - **Signal:** "Great service from [Competitor] for our [Product Line] launch!" - posted by "Jane D., Owner of [Brand X]".
   - **Inference:** [Brand X] buys from [Competitor].
   - **Action:** Add [Brand X] to target list. Tag as "Competitor: [Competitor Name]".

2. **Social Mention Tracking:**
   - **Technique:** Monitor LinkedIn/Twitter/IG for mentions of competitor brands.
   - **Signal:** Brand posts photo of warehouse, cardboard box has [Competitor Logo] visible.
   - **Inference:** Visual confirmation of supplier relationship.
   - **Tool:** Computer Vision on social posts (later stage) or keyword mentions.

### Methodology 2: Import/Export Data (Bill of Lading)
*For international or cross-border shipments, data is public.*

1. **Import Records (Enigma / Panjiva / ImportGenius APIs):**
   - **Signal:** "Consignee: [Competitor]" -> "Shipper: [Overseas Factory]" OR "Shipper: [Competitor]" -> "Consignee: [Buyer]".
   - **Inference:** Maps the supply chain. Publicly available customs data.
   - **Action:** If Competitor exports to [Buyer], we know the relationship volume and frequency.

### Methodology 3: The "Supplier-Reported" Trap (Crowdsourced)
*Our users tell us who they lost to.*

1. **The "Lost Deal" Database:**
   - **Mechanism:** When a user marks a deal "Lost" in our CRM, we ask "Who won?".
   - **Signal:** User selects "[Competitor Name]".
   - **Inference:** We map [Buyer] -> [Competitor] relationship.
   - **Scale:** Network effect. As we grow, this map becomes unbeatable.

---

## LAYER 3: DERIVED DEMAND (The Prediction)
*Who is buying from the buyer? (Calculating their need)*

**Logic:** If [Buyer X] sells 10,000 units of [Product Y], they need 10,000 units of [Packaging Z].

### Methodology 1: E-commerce Velocity Tracking
1. **Shopify/Amazon Store Analysis:**
   - **Technique:** Monitor "Best Sellers" rank changes or stock level drops (where visible).
   - **Signal:** [Brand X] selling out of "Holiday Gift Set".
   - **Inference:** They need immediate restocking of "Holiday Gift Set" packaging.
   - **Tool:** Apify E-commerce Scrapers (Amazon, Shopify).

2. **Ad Spend Acceleration:**
   - **Technique:** Monitor Facebook Ad Library / Google Ads Transparency Center.
   - **Signal:** [Brand X] launches 50 new active ads for "New Skin Cream".
   - **Inference:** High ad spend = expected high volume sales = high packaging demand.
   - **Action:** Alert supplier: "[Brand X] is scaling ads aggressively. Pitch now."

### Methodology 2: B2B Contract Visibility
1. **Public Government Contracts (Downstream):**
   - **Signal:** [Buyer X] wins contract to supply "20,000 Uniforms" to Army.
   - **Inference:** [Buyer X] needs packaging for 20,000 uniforms immediately.
   - **Action:** Alert supplier: "[Buyer X] just won Gov contract. Needs packaging."

---

## LAYER 4: URGENCY SCORING (The Transaction)
*Who needs it RIGHT NOW?*

**The "Urgency Score" (0-100):** A composite metric driving the dashboard.

### Scoring Factors
1. **The "Broken Chain" Signal (Score +40):**
   - **Signal:** Competitor (current supplier) announces layoffs, factory closure, or gets acquired.
   - **Inference:** Service levels will drop. Buyers are nervous.
   - **Action:** High urgency to switch.

2. **The "Growth Spike" Signal (Score +30):**
   - **Signal:** Buyer posts >5 supply chain jobs + Raises Funding + Launches new ads same week.
   - **Inference:** Supply chain is breaking under growth. They need help.

3. **The "Bad Review" Signal (Score +20):**
   - **Signal:** Buyer leaves 1-star review for current shipping/packaging provider.
   - **Inference:** Active pain. Looking for replacement.

4. **The "Seasonality" Signal (Score +10):**
   - **Signal:** It's August. Buyer is "Toy Brand".
   - **Inference:** Holiday packaging procurement happens NOW.

### Output
- **"High Urgency" List:** Top 10% of leads who have >80 Score.
- **Why:** "Competitor struggling + Funding raised + Hiring Logistics VP."

---

## TECHNICAL IMPLEMENTATION (12 Weeks)

**Week 1-4: The Foundation (Layer 1)**
- Build Apify Scrapers (LinkedIn, News, Gov).
- Database Schema: Buyers, Signals.
- Dashboard: List view.

**Week 5-8: The Competitor Layer (Layer 2)**
- Integrate Import/Export API (if budget allows) or build Review Scrapers.
- Build "Lost Deal" data collection form.
- Social mention tracking (keyword based).

**Week 9-10: The Derived Layer (Layer 3)**
- Build Ad Library monitor (Apify).
- E-commerce stock tracker (basic).

**Week 11-12: The Urgency Brain (Layer 4)**
- Write the scoring logic (Cloud Functions).
- Frontend visualization ("Urgency Score" badge).

---

## DATA HONESTY CHECK (v10)

| Intelligence | Method | Legal Status | Feasibility |
|---|---|---|---|
| **Buyer Hiring** | Public Job Posts | ✅ Green | High |
| **Competitor Customers** | Review Mining | ✅ Green | Medium |
| **Competitor Customers** | Import Data | ✅ Green | High (Paid Data) |
| **Competitor Customers** | GPS/Truck Tracking | ❌ Red | **Do Not Do** |
| **Competitor Customers** | Supplier Reported | ✅ Green | High |
| **Buyer Sales Volume** | Ad Library / Best Sellers | ✅ Green | Medium |
| **Urgency** | Composite Scoring | ✅ Green | High |

**Verdict:** We stripped the illegal "spy on trucks" idea and replaced it with "Shadow Tracking" (Reviews, Import Data, Social, User Reports). This is defensible, scalable, and legal.
