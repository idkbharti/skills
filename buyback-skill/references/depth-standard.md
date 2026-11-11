# Depth Standard (Minimum Quality of Every Buyback Report)

The report must be an exhaustive capital markets research report even when the user's prompt is only 3 or 4 simple words. If the analysis would fit into a single short conversational chat bubble, it does **not** meet this depth standard.

---

## Minimum Content Requirements

| # | Requirement | Standard Expected |
|---|---|---|
| **1** | **Buyback Universe** | Comprehensive table of all currently announced, upcoming, and open buybacks in India (NSE/BSE). |
| **2** | **Hard-Gate Screening** | Every candidate evaluated with explicit **PASS** or **REJECT** and reason (e.g. low premium, open-market route, high leverage). |
| **3** | **Scored Candidates** | All passing candidates scored out of 100 with breakdowns across all 5 scoring filters. |
| **4** | **Retail Quota Calculations** | Exact 15% SEBI retail quota size in ₹ Cr, number of shares reserved, and maximum retail eligible shares (`₹2,00,000 / Price`). |
| **5** | **Entitlement vs. Acceptance Analysis** | Base Entitlement Ratio (from LOF) vs. Estimated Acceptance Ratio (based on historical retail tendering patterns). |
| **6** | **Deep-Dive Company Profiles** | Top 2–4 buybacks examined in detail: business summary, balance sheet cash, debt/equity, promoter stake, post-buyback EPS accretion. |
| **7** | **Promoter Intent Disclosed** | Explicit confirmation of whether promoters intend to participate or abstain from tendering. |
| **8** | **3-Scenario Arbitrage P&L Model** | Rupee profit/loss calculated for Bull (100% price recovery), Base (5-8% normal dip), and Bear (12-15% correction). |
| **9** | **Break-Even Acceptance Ratio** | Exact minimum acceptance % required to avoid a loss under Base and Bear market conditions. |
| **10** | **Tax Impact (Finance Act 2024)** | Net returns calculated after Section 2(22)(f) deemed dividend taxation and capital loss (STCL) setoff for 10% and 30% tax slabs. |
| **11** | **Actionable Tender & Exit Plan** | Clear timeline with Buy-by Date, Record Date, Tender Window dates, and exit rule for unaccepted shares. |
| **12** | **Capital Allocation Schedule** | Exact share quantities, rupee outlay, expected accepted shares, and remaining cash for ₹50,000 and ₹2,00,000 budgets. |
| **13** | **Official Filings & Data Log** | Direct links to BSE/NSE corporate announcements, Letter of Offer (LOF), and Registrar portals. |
| **14** | **Disclaimer** | Standard regulatory disclaimer at the conclusion. |

---

## Banned Shortcuts

- **Never** confuse Open Market buybacks with Tender Offers without highlighting the lack of guaranteed retail acceptance.
- **Never** assume 100% acceptance ratio without warning the user of potential unaccepted share market risk.
- **Never** skip the ₹2,00,000 SEBI Small Shareholder cutoff calculation.
- **Never** ignore the post-Oct 1, 2024 deemed dividend tax rules (treating buyback gains as purely tax-free capital gains is outdated and wrong).
- **Never** evaluate only a single company when scanning for buybacks; always show the wider screening landscape first.

---

## Pre-Delivery Self-Check

Before outputting the final report, verify:
1. Did I check whether the offer is a **Tender Offer** or **Open Market**?
2. Did I compute the exact maximum retail shares allowed (`Floor(200000 / CMP)`)?
3. Did I calculate both the **Base Entitlement Ratio** and the realistic **Estimated Acceptance Ratio**?
4. Did I model all 3 post-buyback price scenarios with rupee calculations?
5. Did I calculate the break-even acceptance ratio?
6. Did I state whether promoters are tendering their shares?
7. Did I include the Finance Act 2024 deemed dividend tax treatment?
8. Are all filter scores correctly totaled to 100?

