# 03 · Adoption metrics

The goal is to learn whether AI makes the team better. Measure outcomes against a baseline and watch for side effects.

## 1. What to measure

| Dimension | Metric (examples) | How | Watch out for |
|---|---|---|---|
| **Adoption** | Share of the team using approved tools weekly, by use case | Tool usage reports, short survey | Usage is not value. Report it only next to outcomes |
| **Quality** | Rework on AI-assisted changes; review comments per PR; test coverage; incident count | PR labels, CI data, incident log | Compare against the baseline period, not against zero |
| **Speed** | Cycle time for a defined task type (e.g. new model with tests) | Ticket timestamps | Time saved on drafting can be lost in review. Measure end to end |
| **Cost** | AI spend; warehouse bytes scanned from agent queries; cost per answered question | Billing, dry-run and query logs | Cheap drafts that trigger expensive queries |
| **Trust and risk** | Wrong-answer reports; access violations; near-misses | Incident log, query logs | Zero incidents may mean zero reporting. Encourage reports |
| **People** | Skills coverage (who can use the tools well); champions active; satisfaction | Short survey every quarter | Do not use it to rank individuals |

## 2. How to start
1. **Pick 3-5 metrics**, one or two per dimension that matter most to your pilots.
2. **Capture a baseline** for 4-6 weeks before you push adoption. Starting values and period are suggestions: calibrate them to your workload.
3. **Review monthly** with the team and **quarterly** with leadership.
4. **Change one thing at a time** where you can, so you know what moved the result.

## 3. Metrics to avoid
- **Lines or percentage of code written by AI.** It rewards volume.
- **Number of prompts.** Measures activity.
- **Time saved estimated by individuals.** Self-reported savings are hard to trust. Use observed cycle time instead.
- **Rankings of people by AI usage.** It kills honest reporting.

## 4. Reporting to leadership
One page, three parts: what changed against baseline (quality, speed, cost), what went wrong and what you changed, and what you will try next. Include the uncertainty. "We think this saved time on X, but the data covers 6 weeks" is stronger than a confident but fragile number.

## 5. Scorecard
Use `scorecard-template.csv`. Fill it monthly and keep the history.
