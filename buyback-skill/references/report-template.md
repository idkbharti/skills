# Standard Buyback Report Template

Every deep report produced by the Buyback Skill must follow this exact markdown structure.

---

```markdown
# Share Buyback Deep-Dive & Arbitrage Analysis (India: NSE/BSE)
**Analysis Date:** [YYYY-MM-DD] | **Assumptions:** Budget: ₹[X], Retail Quota (<₹2L), Tax Slab: [10% / 30%]

---

## Executive Summary
[A concise 3-4 sentence paragraph highlighting the overall market buyback environment, the most attractive risk-reward opportunity, and key upcoming record dates.]

- **Total Buybacks Screened:** [X]
- **Tender Offers Passing Gates:** [Y]
- **Top Conviction Arbitrage Pick:** [Company Name (TICKER)] (Score: [Score]/100)
- **Immediate Action Window:** [Next upcoming Buy-by Date]

---

## 1. Buyback Universe & Initial Screening

| Symbol | Company Name | Route | Offer Price | CMP | Premium (%) | Offer Size (₹ Cr) | Record Date | Status | Gate Status |
|---|---|---|---|---|---|---|---|---|---|
| SYMBOL1 | Company 1 Ltd | Tender Offer | ₹500 | ₹410 | +21.9% | ₹1,200 Cr | 2026-11-20 | Open to Buy | PASS |
| SYMBOL2 | Company 2 Ltd | Open Market | ₹250 | ₹248 | +0.8% | ₹150 Cr | N/A | Open Market | REJECT (Low spread) |

### Gate Rationale Log
- **[SYMBOL]**: REJECT — [State exact hard gate triggered, e.g. Open market route with CMP at ceiling price].
- **[SYMBOL]**: PASS — [Tender offer with healthy premium and clean balance sheet].

---

## 2. 100-Point Scoring & Ranking

| Rank | Symbol | Company Name | Premium (25) | Retail AR (25) | Health (20) | Promoter (15) | Valuation (15) | Total (/100) | Verdict |
|:---:|---|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **1** | TICKER1 | Company 1 | 20 | 20 | 18 | 15 | 12 | **85** | **GOOD** |
| **2** | TICKER2 | Company 2 | 15 | 15 | 16 | 10 | 10 | **66** | **NEUTRAL** |

---

## 3. Deep-Dive Profiles (Top Picks)

### Deep Dive 1: [Company Name] ([NSE:TICKER]) — Score: [X]/100 ([VERDICT])

#### A. Deal Parameters & Retail 15% Quota
- **Buyback Route:** Tender Offer via Stock Exchange Mechanism
- **Offer Price:** ₹[X] | **CMP:** ₹[Y] | **Gross Premium:** +[Z]%
- **Total Issue Size:** ₹[A] Cr ([B] shares, [C]% of paid-up equity)
- **SEBI 15% Retail Bucket:** ₹[D] Cr ([E] shares reserved for Small Shareholders)
- **Max Eligible Retail Shares:** **[F] shares** (`Floor(₹2,00,000 / CMP)`)
- **Base Entitlement Ratio (ER):** [X] shares for every [Y] shares held ([Z]%)
- **Estimated Acceptance Ratio (AR):** **[Expected AR]%** *(Based on retail participation history)*

#### B. Financial Strength & Downside Safety
- **Liquid Cash & Investments:** ₹[X] Cr (Covers [Y]% of total buyback size)
- **Debt-to-Equity:** [X]x (Net Cash / Debt-Free)
- **Profitability & ROE:** 3-Yr Revenue CAGR: [X]%, Latest ROE: [Y]%
- **EPS Accretion:** Pre-Buyback EPS: ₹[A] ➔ Post-Buyback Projected EPS: ₹[B] (+[C]%)
- **Valuation:** TTM P/E: [X]x vs Sector P/E: [Y]x

#### C. Promoter Participation & Governance
- **Current Promoter Stake:** [X]%
- **Promoter Intent:** [Abstaining / Participating Proportionately]
- **Post-Buyback Promoter Stake:** Projected to increase to [Y]%

---

## 4. The 3-Scenario Arbitrage P&L Matrix

**Investment Baseline:** Maximum Retail Allocation = [N] shares @ CMP ₹[P] (Total Outlay: ₹[C])  
**Tender Assumption:** All [N] shares tendered; Expected Acceptance = [A] shares ([AR]%), Unaccepted = [U] shares

| Scenario | Market Assumption | Post-Buyback Price ($P_{\text{post}}$) | Gain on Accepted Shares | P&L on Unaccepted Shares | Net Gross Profit | Net ROI (%) |
|---|---|:---:|:---:|:---:|:---:|:---:|
| **Scenario A (Bull)** | Full Price Recovery | ₹[P] (0% dip) | +₹[A_gain] | ₹0 | **+₹[Total]** | **+[X]%** |
| **Scenario B (Base)** | Normal Ex-Date Dip (6%) | ₹[P_base] (-6%) | +₹[A_gain] | -₹[U_loss] | **+₹[Total]** | **+[Y]%** |
| **Scenario C (Bear)** | Broader Correction (14%) | ₹[P_bear] (-14%) | +₹[A_gain] | -₹[U_loss] | **±₹[Total]** | **±[Z]%** |

- **Break-Even Acceptance Ratio ($AR_{\text{be}}$):** **[X]%** *(At a 6% post-buyback dip, the trade is in profit if at least [X]% of shares are accepted)*

---

## 5. Tax Impact & Net Returns (Finance Act 2024)

Under Section 2(22)(f), buyback payouts are treated as **Deemed Dividend** and taxed at slab rates, while the original cost generates an allowable **Capital Loss (STCL)**:

| Tax Bracket | Gross Profit | Deemed Dividend Tax | STCL Tax Shield (at 20% STCG) | Net Post-Tax Profit | Net Post-Tax ROI |
|---|:---:|:---:|:---:|:---:|:---:|
| **0% Tax Slab** (Income < Exemption) | ₹[G] | ₹0 | ₹0 | **+₹[Net]** | **+[X]%** |
| **10% Tax Slab** | ₹[G] | -₹[T10] | +₹[S10] | **+₹[Net]** | **+[Y]%** |
| **30% Tax Slab** | ₹[G] | -₹[T30] | +₹[S30] | **+₹[Net]** | **+[Z]%** |

---

## 6. Capital Allocation Schedule

| Portfolio Budget | Stock Pick | Target Shares | Total Outlay | Expected Accepted | Expected Cash Back | Remaining Cash |
|---|---|:---:|:---:|:---:|:---:|:---:|
| **₹50,000 Budget** | [Top Pick] | [Shares] | ₹[Outlay] | [Accepted] | ₹[Payout] | ₹[Cash] |
| **₹2,00,000 Budget** | [Top Pick] | [Max Retail] | ₹[Outlay] | [Accepted] | ₹[Payout] | ₹[Cash] |

---

## 7. Action Timeline & Execution Roadmap

- **Buy-by Date (T-1):** **[YYYY-MM-DD]** *(Must buy on or before this trading day)*
- **Record Date:** **[YYYY-MM-DD]** *(Must be in Demat as on this date)*
- **Tender Offer Window:** **[YYYY-MM-DD] to [YYYY-MM-DD]** *(Apply online via broker tender portal)*
- **Settlement & Payout:** **[YYYY-MM-DD]** *(Cash credited to bank, unaccepted shares returned to Demat)*
- **Unaccepted Shares Strategy:** [Immediate market exit on settlement day / Hold for fundamental compounding with stop-loss at ₹X]

---

## Regulatory Disclaimer
*This report is for educational and analytical purposes only and is not SEBI-registered investment advice. Share buybacks involve market risks, liquidity risks, and variable acceptance ratios. Verify all dates, circulars, and offer documents directly on BSE/NSE and SEBI portals before trading.*
```

