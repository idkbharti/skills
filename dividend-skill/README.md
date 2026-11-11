# Dividend Capture + Hold/Sell Skill (India: NSE/BSE)

A reusable AI skill that scans upcoming dividends on Indian stocks, scores each one out of 100 using a fixed 7-filter model, and returns a standard report with a **post-dividend hold/sell plan**.

> **Educational use only. Not SEBI-registered investment advice.** Read [DISCLAIMER.md](DISCLAIMER.md) before using.

---

## Quick start (30 seconds)

1. Open your AI assistant (Claude, ChatGPT, Gemini, etc.). Web search should be ON, because the skill needs live ex-dates and prices.
2. Paste the contents of [`SKILL.md`](SKILL.md) as a system prompt, custom instruction, or the first message. (In Claude you can upload it as a skill.)
3. Run one of these commands:

```
Run Dividend Skill - Scan all upcoming dividends this week
Run Dividend Skill for ONGC, PFC - Budget Rs 50000, Risk Low
Run Dividend Skill - Scan December dividends
```

You get a **deep report** in the fixed format shown in [`examples/sample-report.md`](examples/sample-report.md).

### Simple words are enough
You do not need to write long prompts. Even `Run Dividend Skill this week` or `upcoming dividends, budget 50000` triggers the full deep workflow: all ex-dates, hard gates, 10+ stocks scored, deep dives on the top picks, scenarios, allocation and a data log. Add the word `quick` only if you want a short answer.

### Works with any AI
If your AI cannot read several files, paste **`dividend-skill-full-prompt.md`** (all rules in one file).

---

## What it does

| Step | What happens |
|------|--------------|
| 1. Collect | Lists every ex-date in the window from 2+ sources and checks market holidays |
| 2. Gates | Rejects traps: special dividends, loss-making companies, thin liquidity, missed buy dates, 8%+ run-ups, dividends that don't cover costs |
| 3. Score | 0-100 score for 10+ stocks from 6 filters, with a score range and data-confidence label |
| 4. Deep dive | Top 3-4 picks: 5-year dividend history, financial trend, valuation vs peers, technicals, ownership, news, risks |
| 5. Scenarios | Fast recovery / slow recovery / no recovery, with rupee results and break-even |
| 6. Plan | Buy-by date, sell triggers, stop loss, targets for every pick |
| 7. Allocate | Exact share counts with concentration limits, costs and tax at two slab rates |

## Inputs (all optional)

| Input | Default | Notes |
|-------|---------|-------|
| Stock / "this week" / "December" | upcoming dividends | Any NSE/BSE stock name |
| Budget | Rs 10,000 and Rs 50,000 both shown | |
| Risk | Moderate | Low / Moderate / High |
| Goal | Dividend + Value | |
| Holding | 3-12 months | "Only for dividend" = Capture-Only |

## Repo structure

```
dividend-skill/
├── README.md
├── SKILL.md                      # main instructions (paste this into your AI)
├── DISCLAIMER.md
├── CHANGELOG.md
├── LICENSE
├── references/
│   ├── depth-standard.md         # minimum depth + self-check (why simple prompts give deep reports)
│   ├── research-checklist.md     # data to collect for every stock
│   ├── scoring-model.md          # exact points for every filter
│   ├── hold-sell-plan.md         # decision tree, triggers, targets
│   ├── report-template.md        # fixed output format
│   └── tax-and-costs.md          # tax and cost checks
├── dividend-skill-full-prompt.md # everything in ONE file, for AIs that can't read folders
└── examples/
    └── sample-report.md          # hypothetical example, not real data
```

## Known limitations

- A deep report needs an AI with web search or live data. Without it, the AI should ask you to paste the dividend list and will say the report is limited.
- The AI can make data mistakes. **Always verify ex-date, dividend amount and price on NSE/BSE** before buying.
- Scores depend on the data the AI finds. If data is missing, the skill must say "not verified" and not guess.
- Ex-date price drops are an average pattern, not a guarantee. Prices may not recover.
- Small budgets lose a large part of the dividend to costs and tax.

## Contributing

Issues and pull requests are welcome: better filters, data-source suggestions, bug fixes in the scoring math. Please keep the disclaimer intact.

## License

MIT, see [LICENSE](LICENSE). The license covers the text of this skill, not the accuracy of any output.
