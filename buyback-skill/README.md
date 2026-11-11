# Share Buyback Arbitrage & Tender/Hold Skill (India: NSE/BSE)

A specialized, reusable AI skill that scans active and upcoming share buybacks on Indian stock exchanges (NSE/BSE), calculates the **15% SEBI Small Shareholder retail quota**, estimates **acceptance ratios**, models **3 post-buyback price scenarios**, computes **Finance Act 2024 deemed dividend taxes**, and generates an actionable **tender-and-exit plan**.

> **Educational and analytical use only. Not SEBI-registered investment advice.** Read [DISCLAIMER.md](DISCLAIMER.md) before using.

---

## Quick Start (30 Seconds)

1. Open your AI assistant (Antigravity, Claude, ChatGPT, Gemini, etc.). Web search should be enabled for live market filings and prices.
2. Load or paste [`SKILL.md`](SKILL.md) into your system prompt or custom instructions. (Or simply upload the `buyback-skill` folder).
3. Run any of these simple prompt triggers:

```text
Run Buyback Skill - Scan all active and upcoming buybacks
Run Buyback Skill for Genus Power, FDC - Budget Rs 200000
Run Buyback Skill - November buybacks, retail quota
```

You receive a complete **Deep Research Report** formatted to institutional standards.

### Simple Words Trigger Full Depth
You do not need to write complex prompts. Even typing `Run Buyback Skill` or `upcoming buybacks budget 100000` automatically triggers the complete deep-dive workflow: full market scan, hard gates, 100-point scoring, retail ratio math, 3-scenario arbitrage matrix, tax calculations, and budget allocations.

### Standalone File for Any AI
If your AI assistant cannot read directory structures, paste the contents of **`buyback-skill-full-prompt.md`** into a single prompt.

---

## What the Skill Does

| Step | Workflow Action | Details |
|---|---|---|
| **1. Collect** | Comprehensive Scan | Pulls all announced, open, and upcoming buybacks from BSE/NSE filings and official PA/LOFs. |
| **2. Gate** | Trap Filtering | Rejects open-market traps near ceiling price, low-spread tender offers (<3%), illiquid stocks, and overleveraged debt. |
| **3. Score** | 100-Point Model | Evaluates premium spread (25 pts), retail acceptance ratio (25 pts), financial health (20 pts), promoter intent (15 pts), and downside valuation (15 pts). |
| **4. Deep Dive** | Top Opportunities | Examines top 2–4 picks: balance sheet cash coverage, debt-to-equity, post-buyback EPS accretion, and promoter participation. |
| **5. Scenario P&L** | 3-Scenario Matrix | Computes exact rupee profit/loss for Bull (0% dip), Base (6% routine dip), and Bear (14% correction) scenarios, including break-even AR%. |
| **6. Tax & Costs** | Finance Act 2024 | Calculates Section 2(22)(f) deemed dividend taxation and capital loss (STCL) tax shield setoff across 10% and 30% tax slabs. |
| **7. Allocation** | SEBI Retail Quota | Sizes exact share counts up to the ₹2,00,000 small shareholder limit, with clear buy-by, tender, and settlement dates. |

---

## Inputs (All Optional)

| Input | Default Value | Description / Options |
|---|---|---|
| **Stock / Window** | Active & upcoming buybacks | Specific NSE/BSE tickers or months |
| **Budget** | ₹50,000 and ₹2,00,000 | Can specify any capital amount |
| **Category** | Retail (< ₹2 Lakhs) | 15% SEBI Small Shareholder quota |
| **Tax Bracket** | 10% and 30% comparisons | 0%, 10%, 20%, 30% slab calculations |

---

## Repository Structure

```
buyback-skill/
├── README.md                     # Skill overview & execution guide
├── SKILL.md                      # Core AI instructions & workflow
├── DISCLAIMER.md                 # Regulatory & risk disclaimer
├── CHANGELOG.md                  # Version release history
├── LICENSE                       # MIT License
├── buyback-skill-full-prompt.md  # Single-file bundled prompt for web AIs
├── references/
│   ├── depth-standard.md         # Minimum depth requirements & self-check
│   ├── research-checklist.md     # Complete data collection checklist
│   ├── scoring-model.md          # 100-point scoring framework & hard gates
│   ├── arbitrage-and-scenarios.md# Retail tender math & 3-scenario P&L formulas
│   ├── tax-and-costs.md          # Finance Act 2024 taxation & transaction charges
│   └── report-template.md        # Standardized markdown report structure
└── examples/
    └── sample-report.md          # End-to-end representative deep-dive report
```

---

## Contributing
Improvements to acceptance ratio prediction models, tax formulas, or SEBI circular updates are welcome. Please ensure the regulatory disclaimer remains intact.

## License
MIT License. See [LICENSE](LICENSE).

