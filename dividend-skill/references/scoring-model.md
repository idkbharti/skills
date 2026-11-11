# Scoring Model (0-100)

Six scored filters add up to exactly 100. The 7th filter (investment efficiency) is used for ranking only. Check the gates first.

## Step 0: Hard gates (any one = REJECT, do not score)

- Dividend is special / one-off only.
- Company is loss-making, or the dividend is paid out of reserves.
- Average daily traded value below Rs 1 Cr.
- Ex-date already passed, or no trading day left to buy before it.
- Price rose more than 8% in the 5 trading days before the ex-date (run-up trap).
- Net dividend is zero or negative after estimated costs and tax (see `tax-and-costs.md`).

## Filter 1: Dividend yield (25 pts)

Tranche yield = Dividend per share / Current price.

| Tranche yield | Points |
|---------------|--------|
| 2.5% or more | 20 |
| 1.5% to under 2.5% | 16 |
| 1.0% to under 1.5% | 12 |
| 0.5% to under 1.0% | 6 |
| under 0.5% | 0 |

Annual yield = total dividends in the last 12 months / Current price.

| Annual yield | Points |
|--------------|--------|
| above 5% | 5 |
| 3% to 5% | 3 |
| 1% to under 3% | 1 |
| under 1% | 0 |

## Filter 2: Fair price / valuation (20 pts)

| Check | Points |
|-------|--------|
| Position in 52W range: bottom 25% = 8, middle 50% = 4, top 25% = 0 | 0-8 |
| PE vs sector PE: 30%+ below = 8, below = 4, above = 0 | 0-8 |
| P/B under 1.5 (PSU/value) or under 3 (quality) = 4, else 0 | 0-4 |

## Filter 3: Fundamental strength (20 pts)

| Check | Points |
|-------|--------|
| ROE: above 18% = 8, 12-18% = 5, below 12% = 2 | 2-8 |
| ROCE above 12% | 3 |
| Debt/Equity below 1 (or government-backed) | 3 |
| Profit growth positive (latest year) | 3 |
| Dividend never cut in the last 5 years | 3 |

## Filter 4: Sector and market cycle (15 pts)

Check: sector 1-month momentum, crude, interest rates, monsoon/rabi, government policy, global cues.

| Outlook | Points |
|---------|--------|
| Tailwind | 15 |
| Neutral | 8 |
| Headwind | 0 |

## Filter 5: Dividend quality (10 pts)

| Check | Points |
|-------|--------|
| Payout ratio 30-60% = 6; 20-30% or 60-80% = 4; above 80% = 1; special/one-off = 0 | 0-6 |
| Pays interim and final regularly (or a steady regular pattern) | 4 |

## Filter 6: Risk / trap score (10 pts)

| Check | Points |
|-------|--------|
| 5-day price run-up before ex-date: 3% or less = 4; 3-8% = 2 | 0-4 |
| Daily traded value: above Rs 10 Cr = 3; Rs 1-10 Cr = 2 | 0-3 |
| No pending negative event (bad results, regulatory action, high promoter pledge) | 3 |

## Filter 7: Investment efficiency (ranking only)

Dividend per Rs 10,000 = (10000 / Price) x Dividend per share.

Rank all picks by this number, highest first. Show it in the report as "Max dividend for minimum investment".

## Missing data

Any item that cannot be verified scores 0 and is marked "not verified". Do not estimate.

## Verdict bands

| Score | Verdict |
|-------|---------|
| 90-100 | STRONG |
| 75-89 | GOOD |
| 60-74 | NEUTRAL / TACTICAL |
| 40-59 | WEAK (avoid) |
| below 40 | REJECT |

## Score range rule (for unverified items)

When an item cannot be verified, it scores 0, but the report must show the effect:

- Show the score as **"Score X (up to Y if verified)"**, where Y adds the maximum points of every unverified item.
- Example: "Score 80 (up to 84 if the 5-day run-up is confirmed at 3% or less)".
- The verdict uses X, and the report must say if Y would change the verdict.

## Data confidence

Give each scored stock a data confidence label:
- **High**: all key numbers verified from 2 sources.
- **Medium**: some numbers from a single source or a conflict was resolved.
- **Low**: important items unverified. A Low-confidence stock cannot be a top pick unless nothing else qualifies, and must be flagged.

## Dividend history rule (Filter 3, "no cut in 5 years")

Use dividend per share, not payout ratio. List the last 5 years in a table. Any year with a lower total dividend per share than the year before counts as a cut. Interim cuts count too.

## Run-up check (Filter 6)

Use the last 5 trading-day closes. Compute % change from the close 5 trading days before the report date. If above 8%, REJECT (trap). If the closes cannot be found, mark "not verified" and apply the score range rule.

## Peer comparison for PE (Filter 2)

Name the peers and the sector PE used. If only a few peers exist, say so.
