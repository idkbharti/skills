# Sample Report (HYPOTHETICAL DATA, SHORT EXTRACT)

> **This example uses fictional companies and made-up numbers. It shows the structure and the math only, in a shortened form. A real DEEP report is much longer: it lists all ex-dates, gates every stock, scores 10+ stocks and deep-dives 3-4 picks. It is not real data and not a recommendation.**

# Dividend Skill Report
Date: [example] | Window: [example] | Budget: Rs 50,000 | Risk: Moderate | Mode: DEEP
Assumptions: default risk, goal and holding period.

## 2. Dividend universe (extract)
Total ex-dates found: 40 (example). Source: exchange announcements + one calendar site.

## 3. Hard-gate screening (extract)
| Stock | Gate | Reason |
|-------|------|--------|
| EXAMPLE-CO | PASS | Regular interim dividend, liquid, ex-date in window |
| SPECIAL-CO | REJECT | Special one-off dividend |
| LOSS-CO | REJECT | Loss-making, dividend from reserves |
| MISSED-CO | REJECT | Last buy day already passed |

## 4. Scored stocks (extract of top row)
| Rank | Stock | Ex-Date | Dividend | Price | Tranche Yield | Annual Yield | Score | Max if verified | Confidence | Verdict |
|------|-------|---------|----------|-------|---------------|--------------|-------|-----------------|------------|---------|
| 1 | EXAMPLE-CO | dd-mmm | Rs 3.00 | Rs 100 | 3.0% | 4.0% | 84 | 88 | Medium | GOOD |

Filter breakdown: F1 23, F2 16, F3 17, F4 8, F5 10, F6 10 = 84. (Max 88 because the 5-day run-up could add up to 4 points... here shown only as an example of the "score range" rule.)

## 5. Deep dive: EXAMPLE-CO (extract)
**5-year dividend per share (fictional)**
| FY | DPS (Rs) | Change |
|----|----------|--------|
| FY22 | 2.0 | - |
| FY23 | 2.5 | up |
| FY24 | 2.5 | flat |
| FY25 | 3.0 | up |
| FY26 | 3.0 | flat |

No cut in 5 years, so Filter 3 gets the 3 points for this item.

**Last 5 closes (trap check, fictional):** 98.0, 98.5, 99.2, 99.8, 100.0 = +2.0% (under 3%, so 4 points).

**Math for Rs 50,000 (40% cap = Rs 20,000):** 200 shares x Rs 3 = Rs 600 gross.

**Scenarios (200 shares, before tax, costs about Rs 70 assumed)**
| Scenario | What happens | Result |
|----------|--------------|--------|
| A. Fast recovery | Price drops Rs 3 on ex-date, returns to Rs 100 in 5 days, sell 50% | Dividend Rs 600 stays, price effect about 0, minus costs = about Rs 530 |
| B. Slow recovery | Recovers to Rs 100 after 6 weeks, sell all | Same as A, but capital is locked up longer |
| C. No recovery | Stays at Rs 97 | Dividend Rs 600 minus price loss Rs 600 minus costs = about -Rs 70 |

Break-even: the price can fall Rs 3 after the ex-date before the dividend is wiped out.

## 8. Post-dividend Hold/Sell plan (extract)
| Stock | Buy By | Hold/Sell | Sell Trigger 1 | Stop Loss | Target 1 | Target 2 |
|-------|--------|-----------|----------------|-----------|----------|----------|
| EXAMPLE-CO | last trading day before ex-date | Score 75+ but sector neutral: hold until recovery, sell 50% | Rs 100 within 5 days | Rs 92 (8% below buy) | Rs 108 | Rs 117 |

## 12. Limits of this report
Example only. In a real report, list every unverified item and how it affects the score.

## 13. Disclaimer
Educational purposes only, not investment advice. Not a SEBI-registered adviser. Verify ex-date, dividend and price on NSE/BSE before acting. Dividends are taxable. Markets involve risk of loss.
