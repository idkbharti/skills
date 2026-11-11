# Post-Dividend Hold / Sell Plan

Every report MUST include this. The dividend is not free money: the price normally falls by about the dividend amount on the ex-date.

## Decision tree

1. Score 75 or more AND fundamentals strong (Filter 3 at 14+) AND sector tailwind (Filter 4 = 15): **HOLD for 3-12 months**.
2. Score 75 or more but sector is not a tailwind, OR score 60-74: **HOLD until price recovers to the pre-ex price, then sell 50% and hold the rest**.
3. Score below 60: **Capture-Only**. Sell on recovery after the ex-date.

If the user said "only for dividend", treat every pick as Capture-Only.

## Fields to give for each pick

| Field | Rule |
|-------|------|
| Buy By | Last trading day before the ex-date (T+1 settlement means the share must be bought at least one trading day before the ex-date). Verify on NSE/BSE. |
| Ex-Date / Record Date | From the exchange announcement |
| Buy Price | Price on the day of the report (state the date) |
| Expected ex-date drop | About the dividend amount |
| Sell Trigger 1 (quick exit) | Price recovers to Buy Price within 5 trading days: sell 50% |
| Sell Trigger 2 (full exit / stop loss) | Whichever comes first: price below the 52W low, OR 8% below Buy Price, OR fundamentals break (bad results, dividend cut): sell 100% |
| Hold Target 1 | Buy Price + Dividend + 5% (in 1-3 months) |
| Hold Target 2 | 52W High minus 10% (in 6-12 months). If this is lower than Target 1, show only Target 1 |
| Hold condition | Next quarter results are good AND the sector is still a tailwind AND no dividend cut. Review on every results date |
| No recovery in 15 days | Score 75+: keep holding if the hold condition is met. Score below 75: exit |

## Tax warning for short holds

If you buy within 3 months before the record date and sell within 3 months after it, a **capital loss** on that sale can be disallowed up to the dividend received (dividend stripping, Section 94(7), Income Tax Act). Show this warning for every Capture-Only pick. See `tax-and-costs.md`.

## Scenario table (required for every deep-dive pick)

Assume the price falls by the dividend on the ex-date. Show rupee profit/loss for the planned quantity, before tax and after estimated costs.

| Scenario | What happens | Result |
|----------|--------------|--------|
| A. Fast recovery | Price returns to the buy price within 5 trading days, sell 50% | Dividend + gain on 50%, costs |
| B. Slow recovery | Price recovers within 15 days to 1-3 months | Dividend + partial recovery |
| C. No recovery / further fall | Price stays at the ex-date price, or falls to the stop loss | Dividend minus price loss, costs |

Also show a break-even line: how far the price can fall after the ex-date before the dividend is fully wiped out (equal to the dividend per share).

## Exit checklist (review every results date)

- Results worse than expected, or margin falling for 2 quarters.
- Dividend cut or payout above 100% of cash flow.
- Sector turns to a headwind.
- Price below the stop loss.
- Any new negative event (rating cut, regulatory order, concession issue, promoter pledge).
