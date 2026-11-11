# Buyback Scoring Model (0–100 Points)

Five distinct evaluation filters add up to exactly 100 points. Always verify the **Step 0 Hard Gates** before scoring any company.

---

## Step 0: Hard Gates (Any single failure = REJECT immediately)

- **Route Failure**: Open Market buyback where the Current Market Price (CMP) is within 3% of, or exceeds, the maximum buyback ceiling price.
- **Insufficient Premium**: Tender offer price premium over CMP is less than 3% (inadequate buffer against transaction charges and price friction).
- **Missed Eligibility**: Record date has already passed and the investor holds zero shares.
- **Illiquid Trap**: Average daily traded value on NSE/BSE is below ₹1 Crore (prevents smooth liquidation of unaccepted shares).
- **Balance Sheet Overleverage**: Debt-to-Equity ratio exceeds 1.5x, or buyback is being funded via fresh debt issuance rather than accumulated free cash/reserves.
- **Regulatory Red Flags**: Company is categorized in ASM/GSM Stage 2+, or facing active SEBI/CBI investigations.

---

## Filter 1: Buyback Premium over CMP (25 Points)

Measures the gross arbitrage spread:
$$\text{Premium } (\%) = \frac{\text{Buyback Price} - \text{Current Market Price}}{\text{Current Market Price}} \times 100$$

| Gross Premium Spread | Points |
|---|---|
| **25.0% or higher** | 25 |
| **18.0% to 24.9%** | 20 |
| **12.0% to 17.9%** | 15 |
| **7.0% to 11.9%** | 10 |
| **3.0% to 6.9%** | 5 |
| **Below 3.0%** | 0 |

---

## Filter 2: Retail Acceptance Ratio (AR) Potential (25 Points)

Evaluates the expected percentage of tendered retail shares that will actually be accepted, based on the 15% SEBI retail quota vs. estimated small shareholder base.

| Estimated Acceptance Ratio (AR) | Points | Characteristics |
|---|---|---|
| **60.0% to 100%** | 25 | Small retail shareholder base, low retail ownership, high entitlement. |
| **40.0% to 59.9%** | 20 | Favorable retail quota; moderate retail participation. |
| **25.0% to 39.9%** | 15 | Standard tender offer dynamics; modest retail competition. |
| **15.0% to 24.9%** | 10 | High retail concentration; heavy tender competition expected. |
| **Under 15.0%** | 5 | Large retail float; tender acceptances will be heavily scaled down. |

---

## Filter 3: Fundamental & Balance Sheet Health (20 Points)

Ensures that the company is fundamentally robust so unaccepted shares can be held safely without capital erosion.

| Fundamental Metric | Points | Evaluation Threshold |
|---|---|---|
| **Cash Reserves Coverage** | 0–8 | Cash & liquid investments cover 100%+ of buyback outlay = 8<br>Covers 50%–99% = 5<br>Covers <50% = 2 |
| **Return on Equity (ROE)** | 0–4 | ROE > 15% = 4<br>ROE 10%–15% = 2<br>ROE < 10% = 0 |
| **Debt-to-Equity** | 0–4 | Net Cash / Debt-Free = 4<br>D/E between 0.1 and 0.5x = 2<br>D/E > 0.5x = 0 |
| **Operating Cash Flow** | 0–4 | Consistent positive CFO over last 3 years = 4<br>Inconsistent = 0 |

---

## Filter 4: Promoter Confidence & Shareholding (15 Points)

Promoter participation signaling is one of the most critical predictors of post-buyback performance.

| Promoter Intent & Holding | Points | Rationale |
|---|---|---|
| **Promoters Abstaining / Not Participating** | 15 | Maximum bullishness. Promoters choose not to sell, increasing their post-buyback ownership % automatically. |
| **Promoters Participating Proportionately** | 10 | Neutral/Standard. Promoters tender their exact proportionate entitlement, keeping their holding % flat. |
| **Promoters Over-Tendering / Diluting** | 0 | Bearish signal. Promoters taking cash out of the company while retail takes the brunt of unaccepted shares. |

---

## Filter 5: Downside Protection & Technical Support (15 Points)

Evaluates the price risk of unaccepted shares if the stock drops post record date.

| Valuation & Technical Metric | Points | Evaluation Rule |
|---|---|---|
| **Valuation (P/E vs. Sector)** | 0–8 | P/E is 20%+ below sector average = 8<br>P/E is roughly in line with sector = 4<br>P/E is 20%+ above sector = 0 |
| **Distance to 52-Week Low / Support** | 0–4 | Stock is within 15% of 52-week low/major support = 4<br>Middle of 52W range = 2<br>Trading at 52-week high = 0 |
| **Pre-Announcement Run-Up Trap Check** | 0–3 | Stock rose < 5% in the 5 trading days prior to record date = 3<br>Stock rose 5%–10% = 1<br>Stock surged > 10% on speculation = 0 |

---

## Score Summary & Verdict Bands

$$\text{Total Score} = \text{Filter 1} + \text{Filter 2} + \text{Filter 3} + \text{Filter 4} + \text{Filter 5} \quad (\text{Max: } 100)$$

| Total Score | Verdict | Strategy |
|---|---|---|
| **90–100** | **STRONG** | High-conviction arbitrage. High premium, generous retail quota, pristine balance sheet. |
| **75–89** | **GOOD** | Attractive risk-reward. Good premium, manageable unaccepted share downside. |
| **60–74** | **NEUTRAL** | Tactical play only. Low spread or moderate retail competition; tender only if comfortable holding stock. |
| **40–59** | **WEAK** | High risk. Small acceptance expected; high likelihood of post-record date price crash. |
| **Below 40** | **REJECT** | Avoid completely. Fails safety and return criteria. |

