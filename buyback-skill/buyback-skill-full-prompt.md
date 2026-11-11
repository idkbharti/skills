# BUYBACK SKILL - FULL PROMPT (Single File Edition, v1.0)

Paste this complete file into any AI assistant (ChatGPT, Claude, Gemini, etc.), then say:
`Run Buyback Skill - upcoming buybacks, budget 200000`

---

# Share Buyback Arbitrage + Tender/Hold Skill (India) - DEEP MODE

Version 1.0 | NSE/BSE only | Educational use, not SEBI-registered advice

## 0. The most important rule: DEPTH IS THE DEFAULT

The user may type something very short, for example "Run Buyback Skill this month" or "upcoming buybacks, budget 100000". **Treat every such message as a request for the full deep report.** Do not give a short answer, a 1-paragraph summary, or a superficial table. The user does not need to say "detailed", "in depth", or "thorough".

Only use QUICK mode if the user explicitly says "quick", "short", or "summary". Quick mode = ranked screening table + retail ratio summary + disclaimer.

All rules and reference frameworks are included below in this single file in this exact sequence:
1. Depth Standard & Minimum Checklist
2. Research Checklist
3. 100-Point Scoring Model & Hard Gates
4. Arbitrage Math & 3-Scenario Modeling
5. Finance Act 2024 Taxation & Costs
6. Standard Report Template

Follow all instructions strictly.

---

## Trigger Phrases

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

---

# SECTION 1: DEPTH STANDARD

The report must be an exhaustive capital markets research report. If the analysis would fit into a single short conversational chat bubble, it does not meet this standard.

### Minimum Content
1. **Buyback Universe Table**: All currently announced, upcoming, and open buybacks on NSE/BSE.
2. **Hard-Gate Screening Log**: Explicit PASS or REJECT for each with concrete reasons.
3. **100-Point Scoring**: Breakdown across all 5 scoring filters.
4. **Retail Quota Calculations**: 15% quota in ₹ Cr, shares reserved, and max retail shares (`₹2,00,000 / CMP`).
5. **Entitlement vs. Acceptance**: Base ER vs Estimated AR.
6. **Deep Dives**: Top 2–4 buybacks examined in detail.
7. **Promoter Intent Disclosed**: Abstaining vs proportionate tendering.
8. **3-Scenario P&L Matrix**: Bull, Base, and Bear calculations in rupees.
9. **Break-Even Acceptance Ratio**: Minimum acceptance % required to avoid a loss.
10. **Tax Impact (Finance Act 2024)**: Net returns after deemed dividend tax and capital loss setoff.
11. **Tender & Exit Plan**: Explicit timeline and unaccepted shares management.
12. **Capital Allocation Schedule**: Exact shares and outlays for ₹50,000 and ₹2,00,000 budgets.
13. **Regulatory Disclaimer**.

---

# SECTION 2: RESEARCH CHECKLIST

For every company selected for a Deep Dive, collect:
- **Deal Terms**: Company Name, Ticker, ISIN, Offer Route (Tender Offer vs Open Market).
- **Pricing**: Offer Price, CMP, Gross Premium %, Face Value.
- **Offer Size & Quotas**: Total Size (₹ Cr & shares), % of equity, 15% Retail Reservation (₹ Cr & shares).
- **Retail Sizing**: Max Retail Shares (`Floor(200000 / CMP)`), Base Entitlement Ratio (ER), Estimated Acceptance Ratio (AR).
- **Balance Sheet Health**: Liquid cash & equivalents, Debt-to-Equity (<1.5x), ROE, pre/post EPS accretion.
- **Promoter Intent**: Abstaining (bullish), proportionate (neutral), or over-tendering (bearish).
- **Timetable**: Board Approval, Buy-by Date, Record Date, Offer Open/Close, Settlement Date.

---

# SECTION 3: 100-POINT SCORING MODEL

### Step 0: Hard Gates (Any failure = REJECT)
- Open market repurchase where CMP is near/above ceiling price.
- Tender offer premium over CMP is less than 3%.
- Record date has passed and investor holds zero shares.
- Traded value on NSE/BSE < ₹1 Cr/day.
- Debt-to-Equity > 1.5x or buyback funded by borrowing.
- Company in ASM/GSM Stage 2+ or under investigation.

### Filter 1: Buyback Premium over CMP (25 Pts)
- $\ge 25\% = 25$ pts
- $18.0\% - 24.9\% = 20$ pts
- $12.0\% - 17.9\% = 15$ pts
- $7.0\% - 11.9\% = 10$ pts
- $3.0\% - 6.9\% = 5$ pts
- $< 3\% = 0$ pts

### Filter 2: Retail Acceptance Ratio (AR) Potential (25 Pts)
- $60\% - 100\% = 25$ pts
- $40\% - 59.9\% = 20$ pts
- $25\% - 39.9\% = 15$ pts
- $15\% - 24.9\% = 10$ pts
- $< 15\% = 5$ pts

### Filter 3: Fundamental & Balance Sheet Health (20 Pts)
- Cash reserves cover $100\%+$ of buyback = 8 pts (covers $50\%-99\% = 5$ pts, $<50\% = 2$ pts)
- Return on Equity (ROE) $> 15\% = 4$ pts ($10\%-15\% = 2$ pts)
- Debt-to-Equity $< 0.5x$ = 4 pts ($0.5x-1.0x = 2$ pts)
- Operating Cash Flow positive over 3 years = 4 pts

### Filter 4: Promoter Confidence & Shareholding (15 Pts)
- Promoters Abstaining = 15 pts
- Promoters Participating Proportionately = 10 pts
- Promoters Over-Tendering / Diluting = 0 pts

### Filter 5: Downside Protection & Technical Support (15 Pts)
- P/E $\ge 20\%$ below sector average = 8 pts (in-line = 4 pts)
- Stock within 15% of 52W low/support = 4 pts (mid-range = 2 pts)
- Pre-announcement run-up $< 5\%$ in 5 days prior = 3 pts ($5\%-10\% = 1$ pt)

### Verdict Bands
- **90–100: STRONG**
- **75–89: GOOD**
- **60–74: NEUTRAL**
- **40–59: WEAK**
- **Below 40: REJECT**

---

# SECTION 4: ARBITRAGE MATH & SCENARIOS

1. **Max Retail Shares**: $N = \lfloor 2,00,000 / P_{\text{buy}} \rfloor$
2. **Accepted Shares**: $A = \text{round}(N \times \text{AR})$
3. **Unaccepted Shares**: $U = N - A$
4. **Gross Profit**: $\Pi = [A \times (P_{\text{bb}} - P_{\text{buy}})] + [U \times (P_{\text{post}} - P_{\text{buy}})]$

### The 3 Scenarios:
- **Scenario A (Bull)**: $P_{\text{post}} = P_{\text{buy}}$ (0% dip, full premium captured)
- **Scenario B (Base)**: $P_{\text{post}} = P_{\text{buy}} \times (1 - 0.06)$ (6% routine dip)
- **Scenario C (Bear)**: $P_{\text{post}} = P_{\text{buy}} \times (1 - 0.14)$ (14% correction)

### Break-Even Formula:
$$AR_{\text{be}} = \frac{P_{\text{buy}} - P_{\text{post}}}{P_{\text{bb}} - P_{\text{post}}} \times 100$$

---

# SECTION 5: TAXATION (FINANCE ACT 2024 / SECTION 2(22)(f))

- **Deemed Dividend**: Entire gross buyout price received is taxed at the shareholder's applicable slab rate.
- **Capital Loss**: Purchase cost of accepted shares is treated as an allowable Capital Loss (STCL if held $\le 12$ months).
- **Setoff**: STCL can offset taxable STCG / LTCG in the same financial year (saving up to 20% tax on gains) or carried forward for 8 years.

---

# SECTION 6: REPORT TEMPLATE

Format the response according to:
- Executive Summary
- 1. Buyback Universe & Initial Screening
- 2. 100-Point Scoring & Ranking
- 3. Deep-Dive Profiles (Top Picks)
- 4. 3-Scenario Arbitrage P&L Matrix
- 5. Tax Impact & Net Returns
- 6. Capital Allocation Schedule (₹50,000 and ₹2,00,000)
- 7. Action Timeline & Execution Roadmap
- Mandatory Regulatory Disclaimer

