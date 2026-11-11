# Indian Capital Markets & Corporate Actions AI Skills

A curated collection of modular, production-grade AI skills designed for analyzing Indian equity markets and corporate actions (NSE/BSE).

Each skill follows the **"Depth by Default"** standard: even a short, 3-word prompt triggers a multi-step research workflow with screening, hard gates, 100-point scoring models, scenario calculations, and post-event execution plans.

---

## Skills Catalog

| Skill | Directory | Description | Quick Trigger |
| :--- | :--- | :--- | :--- |
| **Dividend Capture & Hold/Sell** | [`dividend-skill/`](dividend-skill/) | Scans upcoming dividend ex-dates, checks financial health, scores stocks out of 100 across 6 filters, and provides a post-dividend exit strategy. | `"Run Dividend Skill"` |
| **Share Buyback Arbitrage** | [`buyback-skill/`](buyback-skill/) | Analyzes tender offer buybacks, calculates the 15% SEBI retail quota (<₹2L), estimates acceptance ratios, and models 3-scenario arbitrage P&L. | `"Run Buyback Skill"` |

---

## How to Use These Skills

### Option 1: In Antigravity / Claude / Custom Agent
Copy the respective skill folder (`dividend-skill` or `buyback-skill`) into your agent's skills directory. The agent will automatically detect and load `SKILL.md` when triggered.

### Option 2: In ChatGPT, Claude Web, or Gemini Web (Single File)
Each skill folder contains a bundled `*-full-prompt.md` file:
- For Dividends: Paste [`dividend-skill/dividend-skill-full-prompt.md`](dividend-skill/dividend-skill-full-prompt.md) into any AI chat.
- For Buybacks: Paste [`buyback-skill/buyback-skill-full-prompt.md`](buyback-skill/buyback-skill-full-prompt.md) into any AI chat.

Then simply type:
```text
Run Dividend Skill - this week, budget Rs 50000
Run Buyback Skill - upcoming buybacks, budget Rs 200000
```

---

## Repository Structure

```
skill/
├── README.md                     # Overview & catalog
├── dividend-skill/               # Dividend capture & hold/sell skill
│   ├── SKILL.md                  # Main AI instructions
│   ├── README.md                 # Detailed documentation
│   ├── dividend-skill-full-prompt.md # Single-file bundled prompt
│   ├── references/               # Scoring, checklist, and scenario guides
│   └── examples/                 # Sample research reports
└── buyback-skill/                # Share buyback arbitrage skill
    ├── SKILL.md                  # Main AI instructions
    ├── README.md                 # Detailed documentation
    ├── buyback-skill-full-prompt.md  # Single-file bundled prompt
    ├── references/               # Scoring, checklist, and scenario guides
    └── examples/                 # Sample research reports
```

---

## Disclaimer
*These skills are for educational and analytical research purposes only and do not constitute SEBI-registered investment advice. Always verify corporate filings, ex-dates, and offer terms directly on official NSE/BSE portals before taking financial positions.*
