# 12-WEEK LAUNCH PLAN v10
## "The 4-Layer Build" (Phased Complexity)

---

## OVERVIEW

**Philosophy:**
We do not build all 4 layers at once. That is suicide.
We build in **Phases of Value**.
Each phase unlocks a Pricing Tier.

**Timeline:**
- **Weeks 1-4:** Layer 1 (Discovery) -> Launch Tier 1 ($299).
- **Weeks 5-8:** Layer 4 (Urgency) + Layer 3 (Derived) -> Launch Tier 2/3 ($599/$899).
- **Weeks 9-12:** Layer 2 (Competitor) -> Launch Tier 4 ($1,299).

---

## PHASE 1: THE FOUNDATION (Weeks 1-4)
*Goal: Launch "Discovery" Tier ($299).*

**Week 1: Infrastructure & Database**
- Setup GCP / Firebase / Auth.
- Design DB Schema: `Buyers`, `Signals`.
- Setup Stripe Basic Plan.

**Week 2: Layer 1 Data Sources (Apify)**
- **Build:** LinkedIn Hiring Scraper (Apify Actor).
- **Build:** NewsAPI Integration.
- **Build:** County Permit Scraper (3-5 major counties test).
- **Verify:** Data flows into `Buyers` table.

**Week 3: Dashboard V1**
- **Frontend:** List view of Buyers.
- **Feature:** Filter by "Hiring", "Expanding", "Funded".
- **Feature:** "Track" button (add to watchlist).

**Week 4: Beta Launch (Tier 1)**
- Onboard 5 Beta Users.
- Manual "Concierge" onboarding (you run the scripts for them).
- **Result:** You have a working $299 product.

---

## PHASE 2: THE PREDICTION ENGINE (Weeks 5-8)
*Goal: Launch "Strategist" Tier ($899).*

**Week 5: Layer 4 (Urgency Scoring) Logic**
- **Code:** Write the Scoring Algorithm.
  - *IF (Hiring > 20%) AND (News = "Expansion") THEN Score = 80.*
- **Frontend:** Add "Urgency Score" badge (0-100) to Dashboard.

**Week 6: Layer 3 (Derived Demand) - Ad Library**
- **Build:** Facebook Ad Library Scraper (Apify).
- **Logic:** Detect "Active Ad Count" spikes.
- **Alert:** "Buyer X just launched 20 new ads."

**Week 7: Layer 3 (Derived Demand) - E-com**
- **Build:** Shopify/Amazon "Best Seller" tracker.
- **Logic:** Detect "Sold Out" or "New Arrival" tags.
- **Alert:** "Buyer Y has high stock velocity."

**Week 8: Upsell Launch (Tier 3)**
- Offer Beta Users upgrade to see "Urgency Scores".
- **Result:** You have a working $899 product.

---

## PHASE 3: THE COMPETITOR WEAPON (Weeks 9-12)
*Goal: Launch "Domination" Tier ($1,299).*

**Week 9: Layer 2 (Shadow Tracking) - Social/Reviews**
- **Build:** Review Monitoring (Google Maps / Trustpilot).
- **Logic:** Scan reviews for "Packaging" keywords or photos.
- **Link:** Map Reviewer Brand -> to -> Supplier (Competitor).

**Week 10: Layer 2 (Shadow Tracking) - Import Data**
- **Integrate:** ImportGenius / Panjiva API (Test Mode / Manual Export first).
- **Logic:** Match "Shipper: Competitor" to "Consignee: Buyer".
- **Frontend:** "Competitor Map" visualization.

**Week 11: The "Lost Deal" Database**
- **Feature:** "Add Competitor" button for Suppliers.
- **Feature:** "Report Lost Deal" form.
- **Logic:** Crowd-source the competitive map.

**Week 12: Full Launch (Tier 4)**
- Marketing: "Stop guessing. See who your competitors are failing."
- Onboard 5 "Type B" Suppliers ($2M+) on Tier 4.
- **Result:** You have a $1,299/mo Enterprise product.

---

## CRITICAL PATH RISKS & MITIGATION

1. **Risk:** Import Data API is too expensive ($500+/mo).
   - **Mitigation:** Start with manual exports (buy one report for $50) for specific competitors requested by Tier 4 users. Do not integrate full API until revenue supports it.

2. **Risk:** Review Mining yields low volume.
   - **Mitigation:** Focus on "Social Mentions" (Instagram tags) which are higher volume for e-commerce brands.

3. **Risk:** Complexity overload.
   - **Mitigation:** **Do not build everything.** Build "Concierge MVP". If a user pays $1,299, YOU manually go look up the import data once a month and upload it. Automate later.

---

## WEEKLY CHECKLIST (The "Monday Morning" Routine)

- **Monday:** Code/Build new features.
- **Wednesday:** Test with data (Manual runs).
- **Friday:** Demo to a Beta User / Get Feedback.
- **Sunday:** Plan next sprint.

---

## FINAL WORD

**You are building a Ferrari, not a Corolla.**
- **Tier 1 ($299)** is the Corolla. (Gets them from A to B).
- **Tier 4 ($1,299)** is the Ferrari. (Unfair advantage).

**Start by selling the Corolla (Week 4), but build the engine for the Ferrari (Week 12).**

**GO.**
