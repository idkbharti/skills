# Changelog

## v1.2
- **DEEP mode is now the default.** Short prompts like "Run Dividend Skill this week" produce the full report; "quick" gives a short one.
- New `depth-standard.md` (minimum content, banned shortcuts, 11-point self-check) and `research-checklist.md` (data to collect per stock).
- Must scan all ex-dates, gate every stock, and score 10+ stocks (v1.1 allowed 3).
- Deep dive now needs 5-year dividend per share, 4-quarter and multi-year financials, technicals, ownership, news.
- Run-up trap check uses the last 5 closes; unverified items now show a "score X (up to Y)" range and a data-confidence label.
- Added price scenarios (fast / slow / no recovery) with rupee results and break-even.
- Report template expanded to 13 sections incl. data log and limits.
- Tax view at two slab rates; cost assumptions must be stated.
- Added `dividend-skill-full-prompt.md` (single-file version for any AI).

## v1.1
- Split the single file into `SKILL.md` plus reference files.
- Scoring model now has exact points per sub-rule; total is capped at 100 and bonuses were folded into fixed points.
- Risk/Trap filter split into hard gates (auto-reject) and a graded 10-point score.
- Added net-yield gate (dividend after costs and tax) and a dividend-stripping warning (Section 94(7), Income Tax Act).
- Added a data policy: never invent numbers, mark unverified items.
- Fixed the hold/sell decision-tree gap (score 75+ without sector tailwind).
- Hold Target 2 now defers to Target 1 when it would be lower.
- Verdict labels changed from BUY/SELL wording to score bands.
- Added a sample report (hypothetical data) and a disclaimer file.

## v1.0
- Initial single-file version.
