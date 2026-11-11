---
name: buyback-skill
description: Deep-research skill for Indian stock share buybacks (NSE/BSE tender offers & open market via SEBI mechanism). Scans active & upcoming buybacks, checks 15% SEBI small shareholder retail quota (<Rs 2 Lakhs), calculates entitlement & estimated acceptance ratios, models arbitrage profit/loss across 3 post-buyback scenarios, analyzes promoter participation intent, calculates tax impact under Finance Act 2024 (deemed dividend + capital loss setoff), and outputs budget allocation and a tender-or-hold plan. Use when the user says "Run Buyback Skill" or asks about buyback arbitrage, tender offers, retail acceptance ratios, or upcoming buybacks in India. Educational only, not investment advice.
---

# Share Buyback Arbitrage + Tender/Hold Skill (India) - DEEP MODE

Version 1.0 | NSE/BSE only | Educational use, not SEBI-registered advice

## 0. The most important rule: DEPTH IS THE DEFAULT

The user may type something very short, for example "Run Buyback Skill this month" or "upcoming buybacks, budget 100000". **Treat every such message as a request for the full deep report.** Do not give a short answer, a 1-paragraph summary, or a superficial table. The user does not need to say "detailed", "in depth", or "thorough".

Only use QUICK mode if the user explicitly says "quick", "short", or "summary". Quick mode = ranked screening table + retail ratio summary + disclaimer.

Before answering, read and follow all reference guides in `references/`:
1. `references/depth-standard.md` - minimum mandatory content of every report
2. `references/research-checklist.md` - exact data points to collect per buyback
3. `references/scoring-model.md` - exact 100-point scoring model and hard gates
4. `references/arbitrage-and-scenarios.md` - retail math, 3 price scenarios, tender/hold strategy
5. `references/tax-and-costs.md` - Finance Act 2024 tax rules (Section 2(22)(f)) & cost calculations
6. `references/report-template.md` - standard output report template

If you cannot read files in separate folders, read `buyback-skill-full-prompt.md` which contains all references combined.

## Trigger phrases (all of these start the full workflow)

- "Run Buyback Skill ..." (any ending)
- "upcoming buybacks", "buyback this week", "buyback this month", "share buyback", "buyback arbitrage", "tender offer", "retail acceptance ratio", "which stock has buyback"
- Any company symbol, budget, or timeframe after these phrases

## Inputs (use defaults if not provided, never halt to ask)

| Input | Default | Notes |
|---|---|---|
| Window | Active (Ongoing) & Upcoming buybacks: currently open offers, impending record dates, and future announced boards | Can specify month or specific stocks |
| Scope | Both **Ongoing** (active bidding window / cum-buyback trading) and **Upcoming** (board approved, future record dates) |
| Data Priority | **NSE MCP Server (Priority 1)**. If not configured, auto-skip to live web search fallback |
| Budget | Show Rs 50,000 and Rs 2,00,000 (Max SEBI Retail Limit) if not given | If specified, use exact budget |
| Category | Retail (< Rs 2 Lakhs on Record Date) | Max investment allowed under SEBI 15% quota |
| Strategy | Arbitrage Tender (Tender maximum shares, manage unaccepted portion) | Arbitrage / Tender-and-Hold |
| Tax Slab | 10% and 30% slab comparisons | Post-Oct 1, 2024 deemed dividend tax rules |

State the assumptions in one clear line at the top of the report. Do not stop to ask questions.

## Rules for the AI

1. **Data Source Priority (NSE MCP first):**
   - **Priority 1: NSE MCP Server.** If an NSE MCP tool/server is configured in your environment, query it on priority for live buyback announcements, corporate filings, circulars, and market prices.
   - **Fallback:** If NSE MCP is not set up, note in one brief line: *"NSE MCP server not active; using live web search fallback"*, and seamlessly query web sources (NSE/BSE filings, Chittorgarh, SEBI LOF filings). Never abort or halt if MCP is absent.
2. **Scan Both Ongoing & Upcoming Events:**
   - **Ongoing / Active:** Tender offers with active bidding windows open on stock exchange platforms, or stocks currently trading cum-buyback before an upcoming Record Date.
   - **Upcoming:** Buybacks approved by the Board of Directors, buybacks awaiting shareholder/postal ballot clearance, or approved deals awaiting official Record Date announcement.
3. **Use live data and comprehensive searches.** Plan for 15-30 tool calls. Check official exchange circulars (NSE/BSE corporate announcements), Chittorgarh, SEBI Public Announcements (PA), and Letters of Offer (LOF).
4. **Never invent numbers.** Unverified figures must be labeled "not verified" and receive 0 points in the scoring model.
5. **Cross-check critical parameters** (Buyback Price, Record Date, Offer Size, Route) from at least 2 distinct sources.
6. **Distinguish Route strictly**: Tender Offer via Stock Exchange vs. Open Market repurchase. (Tender offers have fixed price and 15% retail reservation; open market does not guarantee retail acceptance).
7. **Always calculate the SEBI Small Shareholder threshold**:
   $$\text{Max Retail Shares} = \left\lfloor \frac{2,00,000}{\text{Closing Price on Record Date}} \right\rfloor$$
8. **Compute both ratios**:
   - **Base Entitlement Ratio (ER)**: Official guaranteed ratio disclosed in the Letter of Offer.
   - **Estimated Acceptance Ratio (AR)**: Expected final acceptance based on retail shareholder participation history (typically 1.5x–4x the base entitlement).
9. **Always model 3 post-buyback scenarios**:
   - Bull (Full recovery to CMP)
   - Base (Normal 5-8% post record-date dip)
   - Bear (12-15% market correction on unaccepted shares)
10. **Factor in the new Finance Act 2024 tax regime**:
   - Buyback proceeds are taxed as **Deemed Dividend** under Section 2(22)(f) at slab rates.
   - Acquisition cost of accepted shares is treated as Capital Loss (STCL) to offset other capital gains.
11. **Score at least 5-10 buybacks** (or all active candidates if fewer) before selecting top picks.
12. **Always end with the standard regulatory disclaimer.**

## Workflow

1. **Collect**: Scan all announced, open, and upcoming buybacks from exchange circulars and market trackers.
2. **Gate**: Apply Step 0 Hard Gates (`references/scoring-model.md`). Reject unviable deals with reasons.
3. **Score**: Score all surviving buybacks across the 5 filters (0–100 total).
4. **Deep-Dive Top Picks**: Analyze the top 2-4 picks using `references/research-checklist.md` (promoter intent, balance sheet cash, debt, EPS accretion).
5. **Model Scenarios**: Run the 3-scenario arbitrage model with exact rupee profit/loss and break-even acceptance ratio.
6. **Budget Allocation**: Allocate capital up to the Rs 2,00,000 retail limit with exact share quantities.
7. **Tax & Net Return**: Show net post-tax return across tax slabs.
8. **Tender Plan**: Clear timeline of Record Date, Bidding Window, and post-buyback exit strategy.
9. **Self-Check**: Verify math, then output using `references/report-template.md`.

## Verdict bands

| Score | Verdict | Recommendation |
|---|---|---|
| 90–100 | STRONG | Prime Arbitrage Candidate (High premium, small retail base, pristine balance sheet) |
| 75–89 | GOOD | Attractive Risk-Reward (Good premium, reasonable acceptance ratio) |
| 60–74 | NEUTRAL / TACTICAL | Selective Play (Low premium or high unaccepted share risk) |
| 40–59 | WEAK | High Risk (Low acceptance expectation, vulnerable CMP) |
| Below 40 | REJECT | Fails safety or profitability gates |

## Capital allocation rules (SEBI Small Shareholder Framework)

- Never exceed Rs 2,00,000 per Demat account per stock (to stay within the 15% retail quota).
- Recommend allocating across multiple family Demat accounts if budget exceeds Rs 2,00,000.
- For budgets below Rs 50,000: Concentrate on the single highest-conviction buyback.
- Show exact share counts, total outlay, expected tendered shares, expected accepted shares, and remaining cash.

## Disclaimer (Mandatory in every report)

*This report is for educational and analytical purposes only and does not constitute SEBI-registered investment advice or a recommendation to tender or trade securities. Buyback acceptance ratios, post-buyback prices, and tax liabilities depend on market participation and individual tax slabs. Verify all dates, prices, and circulars directly from official BSE/NSE filings and the SEBI Letter of Offer before taking any action.*

