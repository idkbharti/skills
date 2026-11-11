---
name: dividend-skill
description: Deep-research skill for upcoming and ongoing dividends on Indian stocks (NSE/BSE). Scans ALL ex-dates in the window, applies hard gates, scores 10+ stocks out of 100 with a fixed model, deep-dives the top picks (dividend history, financials, valuation, technicals, ownership, news), runs price scenarios, and gives budget allocation and a hold/sell plan. Use when the user says "Run Dividend Skill" or asks about dividend capture, upcoming ex-dates, or dividend picks in India, even in very simple words. Educational only, not investment advice.
---

# Dividend Capture + Hold/Sell Skill (India) - DEEP MODE

Version 1.2 | NSE/BSE only | Educational use, not SEBI-registered advice

## 0. The most important rule: DEPTH IS THE DEFAULT

The user may type something very short, for example "Run Dividend Skill this week" or "upcoming dividends, budget 50000". **Treat every such message as a request for the full deep report.** Do not give a short answer, a 3-stock answer, or a summary. The user does not need to say "detailed", "in depth" or "thorough".

Only use QUICK mode if the user clearly says "quick", "short" or "summary". Quick mode = ranked table + allocation + disclaimer.

Before answering, read these files and follow them:
1. `references/depth-standard.md` - minimum content of the report
2. `references/research-checklist.md` - what data to collect for each stock
3. `references/scoring-model.md` - exact scoring
4. `references/hold-sell-plan.md` - plan, triggers, scenarios
5. `references/tax-and-costs.md` - tax and cost checks
6. `references/report-template.md` - the output format

If you cannot read files, ask the user to paste the file "dividend-skill-full-prompt.md" instead, and follow it.

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
