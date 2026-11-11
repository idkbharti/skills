# DIVIDEND SKILL - FULL PROMPT (single file, v1.2)

Paste this whole file into any AI, then say: Run Dividend Skill - this week, budget 50000

---

# Dividend Capture + Hold/Sell Skill (India) - DEEP MODE

Version 1.2 | NSE/BSE only | Educational use, not SEBI-registered advice

## 0. The most important rule: DEPTH IS THE DEFAULT

The user may type something very short, for example "Run Dividend Skill this week" or "upcoming dividends, budget 50000". **Treat every such message as a request for the full deep report.** Do not give a short answer, a 3-stock answer, or a summary. The user does not need to say "detailed", "in depth" or "thorough".

Only use QUICK mode if the user clearly says "quick", "short" or "summary". Quick mode = ranked table + allocation + disclaimer.

All the rules are in this one file, in this order: depth standard, research checklist, scoring model, hold/sell plan, tax and costs, report template. Follow all of them.

## Trigger phrases (all of these start the full workflow)

- "Run Dividend Skill ..." (any ending)
- "upcoming dividends", "dividend this week", "dividend stocks", "ex-dividend", "dividend capture", "which stock gives dividend"
- Any budget or stock names after these words

## Inputs (use defaults if not given, never ask before starting)

| Input | Default |
|-------|---------|
| Window | Active (Ongoing) & Upcoming: today through the next 14 days of ex-dates. Includes currently trading cum-dividend stocks and future announced dates |
| Scope | Both **Ongoing** (cum-dividend trading window) and **Upcoming** (board approved, declared, future ex-dates) |
| Data Priority | **NSE MCP Server (Priority 1)**. If not configured, auto-skip to live web search fallback |
| Budget | Show Rs 10,000 and Rs 50,000 if none given; if given, use only that |
| Risk | Moderate |
| Goal | Dividend + Value |
| Holding | 3-12 months. "Only for dividend" = Capture-Only |

State the assumptions in one line at the top of the report. Do not stop to ask questions.

## Rules for the AI

1. **Data Source Priority (NSE MCP first):**
   - **Priority 1: NSE MCP Server.** If an NSE MCP tool/server is configured in your environment, use it on priority for live corporate actions, quote data, and exchange announcements.
   - **Fallback:** If NSE MCP is not set up, note in one brief line: *"NSE MCP server not active; using live web search fallback"*, and seamlessly use web search (NSE/BSE filings, Chittorgarh, Screener, Yahoo Finance). Never abort or halt if MCP is absent.
2. **Scan Both Ongoing & Upcoming Events:**
   - **Ongoing / Active:** Stocks currently trading cum-dividend (Ex-date is today or in the current settlement cycle) where investors can still buy to receive the payout.
   - **Upcoming:** Dividends declared by the board with future Ex-Dates, as well as announced board meetings scheduled to consider dividend declarations.
3. **Use live data and many searches.** Plan for 15-30 tool calls. One or two searches is never enough.
4. **Never invent numbers.** Unverified items are marked "not verified" and score 0 (see the score range rule in `scoring-model.md`).
5. **Cross-check** price, ex-date and dividend from at least 2 sources for the top picks. If sources disagree, show both and use the more recent one, flagged.
6. **Show date and source** for every key number.
7. **Score at least 10 stocks** (or all that pass the gates, if fewer than 10) before choosing the top picks. Show the full screening table.
8. **Deep-dive the top 3-4 picks** using the research checklist.
9. **Always run scenarios** (price recovers fast / slowly / never) with rupee results.
10. **Always check the exchange holiday calendar** before computing buy-by dates.
11. **Run the self-check** in `depth-standard.md` before sending. Fix gaps, or list them under "Limits of this report".
12. **Always end with the disclaimer.** Use neutral wording: the dividend is not free money, because the price normally drops by about the dividend on the ex-date.

## Workflow

1. **Collect**: all dividend ex-dates in the window from at least 2 sources (exchange announcements first, then calendars). Check market holidays.
2. **Gate** every stock (`scoring-model.md`, Step 0). Show a table of all stocks with PASS/REJECT and the reason.
3. **Score** the best 10+ survivors. Start with the highest yields and the best liquidity, but also include any large or well-known company with a dividend in the window.
4. **Rank** by score, then by dividend per Rs 10,000.
5. **Deep-dive** the top 3-4 using `research-checklist.md`.
6. **Scenarios + plan**: hold/sell plan, scenarios, stop loss, targets.
7. **Allocate** the budget using the rules below, with exact share counts.
8. **Costs and tax**: net result after costs and after tax at 2 slab assumptions.
9. **Self-check**, then output using `report-template.md`.

## Verdict bands

| Score | Verdict |
|-------|---------|
| 90-100 | STRONG |
| 75-89 | GOOD |
| 60-74 | NEUTRAL / TACTICAL |
| 40-59 | WEAK (avoid) |
| below 40 | REJECT |

## Capital allocation rules

- Never more than 40% of the budget in one stock.
- Never more than 60% in one sector.
- Keep 20% in cash for the next week's dividends.
- Budget below Rs 10,000: max 2 stocks, pick the highest dividend per Rs 10,000.
- Budget Rs 10,000 to 50,000: max 3 stocks.
- Budget above Rs 50,000: max 4 stocks.
- Use whole shares. Show quantity, amount, % of budget and dividend for each.

## Disclaimer (include in every report)

This report is for educational purposes only and is not investment advice. The author is not a SEBI-registered investment adviser or research analyst. Data may be incomplete or wrong. Verify the ex-date, dividend and price on NSE/BSE before acting. Dividends are taxable. Markets involve risk of loss, and you can lose part or all of your capital. Consult a SEBI-registered adviser before investing.

---

# Depth Standard (minimum quality of every report)

The report must be a deep analysis even when the user's message is only a few simple words. If the report would fit in a short chat message, it is NOT deep enough.

## Minimum content

| # | Requirement | Minimum |
|---|-------------|---------|
| 1 | Dividend universe | Every ex-date in the window listed, with count |
| 2 | Hard-gate table | All stocks, each PASS/REJECT with a reason |
| 3 | Scored stocks | At least 10 (or all survivors if fewer), with full filter breakdown |
| 4 | Deep dives | Top 3-4 picks, each using the research checklist |
| 5 | Dividend history | Last 5 years of dividend per share for each deep-dive pick (table) |
| 6 | Financial trend | Last 4 quarters and 3-5 years of sales and profit, margins, cash flow for each deep-dive pick |
| 7 | Price-trap check | Last 5 trading-day closes for each deep-dive pick, with % move |
| 8 | Scenario table | 3 scenarios per pick with rupee profit/loss |
| 9 | Allocation | Exact shares, amount, % of budget, dividend, cash left |
| 10 | Costs and tax | Net result after costs, and after tax at two slab rates |
| 11 | Hold/sell plan | Every pick, with exact prices |
| 12 | Data log | Source, date and confidence for every key number |
| 13 | Limits | What was not verified and how it affects the score |
| 14 | Watch-list | Stocks to check next week, with ex-dates |
| 15 | Disclaimer | Always |

## Banned shortcuts

- Scoring only 3 stocks.
- Using one source for ex-date or price without saying so.
- Skipping the run-up check and not saying that the score may change.
- Giving "BUY"/"SELL" calls without the score, the plan and the scenarios.
- Hiding a data conflict.
- Stopping the research after one or two searches.

## Self-check before sending (answer each one honestly)

1. Did I list every ex-date in the window?
2. Did I check market holidays and compute buy-by dates correctly?
3. Did I apply every hard gate to every stock?
4. Did I score 10 or more stocks?
5. Do all filter scores add up correctly?
6. Does each deep dive have a 5-year dividend table, financial trend, valuation, sector, technicals, ownership and news?
7. Did I run the 5-day price check?
8. Are scenarios and costs calculated with real numbers?
9. Do allocation numbers respect the 40% / 60% / 20% rules?
10. Is every conflict or missing item listed under "Limits"?
11. Is the disclaimer included?

If any answer is "no", go back and fix it. If it cannot be fixed (no data), say so in "Limits".

---

# Research Checklist (collect for EVERY deep-dive pick)

Use exchange announcements first (NSE/BSE), then company filings, then data sites (Screener, Tickertape, Trendlyne, Tapetide, Moneycontrol) and news. Cross-check key numbers across at least 2 sources.

## A. Dividend facts
- Ex-date, record date, type (interim/final/special), amount per share, payment date, board announcement date.
- Dividend per share for each of the last 5 financial years (table). Mark any cut.
- Interim + final pattern and total dividend cash vs profit and free cash flow.
- Payout ratio (dividend / EPS) and cash cover (free cash flow / dividend cash).

## B. Price and trap check
- Latest close and date; 52-week high/low; position in range (%).
- Last 5 trading-day closes and % change (run-up trap if above 8%).
- 1-month and 3-month change; distance from 50-day and 200-day average; RSI (14).
- Average daily traded value (shares x price) and delivery %.

## C. Financial strength
- Last 4 quarters: sales, operating profit, margin, net profit, EPS, YoY growth.
- Last 3-5 years: sales, profit, ROE, ROCE, debt/equity, interest cover, operating cash flow, free cash flow.
- Latest result and one line on management commentary (concall/press release).

## D. Valuation
- P/E vs sector or peer median (name the peers), P/B, EV/EBITDA if relevant, dividend yield (tranche and 12-month).
- Own 5-year P/E range if available.

## E. Sector and market
- Sector 1-month momentum, key drivers (crude, rates, commodity, monsoon, policy, global cues).
- Government/regulatory developments that affect this company.

## F. Ownership and risk
- Promoter holding and pledge; FII/DII change in the last quarter.
- Pending negatives: litigation, regulatory action, concession or licence expiry, management change, rating action.
- Company-specific risk in one paragraph (what could make the price fall more than the dividend).

## G. News and events in the next 30 days
- Results date, board meetings, AGM, policy decisions, index changes.

## H. Verification record
For each key number write: value | source | date | confidence (High/Medium/Low).

---

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

---

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

---

# Tax and Cost Check

Rules and rates change. Verify the current ones on the Income Tax Department website or with a tax professional. This file is a checklist, not tax advice.

## 1. Net yield check (gate)

Estimated net dividend per share = Dividend - tax on dividend.
Estimated round-trip cost = brokerage + STT (delivery) + exchange/DP charges + GST, for buy and sell.

Reject (gate) if: total dividend received - total round-trip costs - tax is zero or negative for the budget used.

Small budgets (Rs 10,000) are hit hardest because many charges are flat per trade (for example DP charges on selling).

## 2. Dividend tax

- Dividend income is taxed in the investor's hands at their income-tax slab rate.
- Companies deduct TDS on dividends above a yearly per-company threshold. Check the current threshold and rate.
- Mention this in every report: "Dividends are taxable."

## 3. Dividend stripping (Section 94(7))

Buy within 3 months before the record date + sell within 3 months after = a loss on the sale is disallowed up to the dividend received.

## 4. Capital gains

Selling after a recovery creates a capital gain or loss. Short-term and long-term rates depend on the holding period. Check the current rates.

## What the AI must do

- Show estimated costs as a range, state the assumptions, and flag that the user's broker charges may differ.
- Never state tax figures as certain. Say "verify current rules".

## Two-slab tax view (required in every report)

Show net dividend after tax at two assumed slab rates (for example 20% and 30%), plus the number if the user is in the lowest slab. State that the user's own slab and any TDS may differ.

## Cost assumptions to state

List the assumptions used: brokerage per trade, STT on delivery (buy and sell), exchange charges, stamp duty on buy, DP charge on sell, and GST. Say that the user's broker rates may differ.

---

# Report Template (always use this format, DEEP mode)

Use headings and tables. Fill every section. If something is not available, write "not verified" and explain in section 12.

```
# Dividend Skill Report
Date: [today] | Window: [from - to] | Budget: [..] | Risk: [..] | Goal: [..] | Mode: DEEP
Assumptions: [one line: defaults used]

## 1. Market and sector context (5-8 lines)
[market trend, rates, key sector drivers, holiday calendar, results season note]

## 2. Dividend universe
Total ex-dates found in window: [N]. Source(s): [..]. Holidays/trading days: [..]
| Company | Ex-Date | Buy-By | Dividend | Price | Tranche Yield |
(list all, or the top 30 by yield + a count of the rest)

## 3. Hard-gate screening (all stocks)
| Stock | Gate result | Reason |
(PASS or REJECT for each stock, with a one-line reason)

## 4. Scored stocks (10+)
| Rank | Stock | Ex-Date | Dividend | Price | Cost/Share | Tranche Yield | Annual Yield | Score | Max if verified | Confidence | Verdict |
Then a filter breakdown table: Stock | F1 | F2 | F3 | F4 | F5 | F6 | Total
Then Dividend per Rs 10,000 ranking.

## 5. Deep dive: top 3-4 picks (one section per stock)
### [Stock] - Score [X] ([verdict]) - Confidence [..]
- Business and why it pays dividends (2 lines)
- Dividend facts: ex-date, record date, type, amount, payment date
- 5-year dividend per share table (mark cuts)
- Financial trend: last 4 quarters and 3-5 years (sales, profit, margin, ROE, ROCE, debt, cash flow)
- Valuation: P/E vs named peers, P/B, 52-week position
- Sector view: tailwind/neutral/headwind and why
- Technicals: 50/200 DMA, RSI, last 5 closes and % move (trap check)
- Ownership: promoter, pledge, FII/DII change
- News and next events (30 days)
- Main risk: what could make the price fall more than the dividend
- Why it ranks above/below the others
- Math for the budget: shares, amount, dividend, costs, net
- Scenarios A / B / C table with rupee results and break-even

## 6. AVOID and watch-list
| Stock | Why rejected / what to watch | Next check date |

## 7. Allocation plan
| Stock | Qty | Amount | % of budget | Gross dividend |
Cash kept, total invested, total dividend, concentration and sector checks.

## 8. Post-dividend Hold/Sell plan
| Stock | Buy By | Hold/Sell | Sell Trigger 1 | Stop Loss | Target 1 | Target 2 | If no recovery in 15 days |

## 9. Costs and tax
Estimated costs (with assumptions), net before tax, net after tax at two slab rates, TDS note, Section 94(7) warning.

## 10. What would change this view
[3-5 events or data points that would improve or worsen the picks]

## 11. Data log
| Item | Value | Source | Date | Confidence |

## 12. Limits of this report
[everything not verified, conflicts between sources, and the effect on scores]

## 13. Disclaimer
Educational purposes only, not investment advice. Not a SEBI-registered adviser. Verify ex-date, dividend and price on NSE/BSE before acting. Dividends are taxable. Markets involve risk of loss.
```

---

# Disclaimer

**Educational purposes only. Not investment advice.**

- This project is a prompt/skill and set of rules for organising information about dividends. It is **not** a recommendation to buy, sell or hold any security.
- The author is **not** a SEBI-registered investment adviser or research analyst.
- Output is generated by an AI and may contain errors, outdated data or wrong dates. **Always verify the ex-date, record date, dividend amount and price on the NSE/BSE websites or the company's filings before acting.**
- Scores, verdicts, targets and stop-losses are rule-based illustrations. They do not predict future prices, and past dividends do not guarantee future dividends.
- Share prices usually fall by about the dividend amount on the ex-date and may not recover. You can lose part or all of your capital.
- Dividend income is taxable and trading has costs (brokerage, STT, DP charges and others). Tax rules change; check the current rules or consult a tax professional.
- Use of this project is entirely at your own risk. The author accepts no liability for any loss or damage.
- Consult a SEBI-registered investment adviser before making investment decisions.
