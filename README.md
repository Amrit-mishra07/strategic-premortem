# Strategic Pre-Mortem: a Claude skill

Stress-test an idea, plan, or decision **before** you commit, then simulate what happens **after** you do.

Most pre-mortems give you a generic risk list. This skill makes Claude do the harder work:

- **Challenge the framing.** Steelman the idea, then ask whether the problem, solution, and business model hold, and whether a simpler alternative fits your real goal better.
- **Surface hidden assumptions.** Rank what must be true, label each as fact / assumption / hypothesis / speculation, and find the cheapest test for the ones everything rests on.
- **Check the economics.** Real demand vs. apparent demand, willingness to pay, unit economics, cash and hours runway, with ranges and no invented statistics.
- **Apply game theory to your specific case.** Map every player (customers, competitors, platforms, suppliers, cofounders, regulators), model what each will actually do, when, and how your best response should change as things evolve.
- **Simulate six months, month by month.** Base, upside, downside, and compound-failure scenarios built from a state model (cash, hours, customers, trust), an event library, and player responses, so failures emerge from interacting small problems instead of a single dramatic event.
- **Leave you with decisions.** Risk cards with warning signs, decision gates, kill/pivot/persevere/scale thresholds set in advance, if-then contingency plans, and a 14-day action list.
- **Keep working after launch.** Paste the checkpoint block back in with real results and it compares prediction to reality, updates the forecast, and flags moved goalposts.

## Install

### Claude.ai / Claude Desktop
1. Download `strategic-premortem.skill` from the [latest release](../../releases/latest).
2. In Claude, open **Settings → Capabilities → Skills** (menu names change; see Anthropic's current "Using skills in Claude" guide) and upload the file.

Skills need code execution to be enabled, and availability depends on your plan. Uploaded skills are private to your account unless your organization admin shares them.

### Claude Code
Add this repo as a marketplace, then install:

```
/plugin marketplace add Amrit-mishra07/strategic-premortem
/plugin install strategic-premortem@premortem-skills
```

Or install manually by copying `plugins/strategic-premortem/skills/strategic-premortem/` into `~/.claude/skills/` (all projects) or `.claude/skills/` (one project).

### Claude API
Upload the skill folder through the Skills API. See Anthropic's documentation on custom skills.

## Use it

Just describe your idea, plan, or decision. Examples:

- "Pre-mortem my plan to launch a meal-prep subscription with two friends. We have about 10 hrs a week each and ₹2 lakh."
- "Should I quit my job to freelance? I have 9 months of expenses saved. Walk me through the next six months."
- "Red-team this pitch deck." (attach it)
- "Month 2 update: 7 paying customers vs. target 15, a competitor launched a free tier. Here's my last state block…"

| Mode | When | Output |
|---|---|---|
| Full | A real idea or plan with a consequential commitment | Complete report: verdict, assumptions, economics, players, risks, six-month simulation, decision gates |
| Quick | One-liners or thin information | ~600-word verdict, top risks, cheapest tests, the questions that matter |
| Decision | A specific choice (quit, pivot, sign, launch now vs. later) | Options, irreversibility, regret, flip-conditions |
| Review | A document or deck | Claims audit and strongest outside objections |
| Checkpoint | Mid-project, with actual results | Predicted vs. actual, assumption updates, re-forecast, decisions due |

See [`examples/`](examples/) for an illustrative output.

## How it is built

```
plugins/strategic-premortem/skills/strategic-premortem/
├── SKILL.md                      # stance, modes, pipeline, epistemic rules
└── references/
    ├── intake-and-framing.md     # intake, steelman, goal-fit, assumption ledger, reference classes
    ├── economics.md              # demand evidence, unit economics, cash, type-specific checks
    ├── execution-and-behavior.md # constraints, human behavior, feedback loops, irreversibility
    ├── game-theory.md            # player map, response modeling, strategic structures
    ├── simulation-method.md      # state model, event library, scenarios, month-by-month method
    ├── risk-and-decisions.md     # pre-mortem and pre-parade, risk cards, gates, thresholds
    ├── self-review.md            # pre-delivery checklist, failure modes, adversarial cases
    └── output-templates.md       # report templates, state block, weak-vs-strong examples
```

Design principles: mechanisms over labels, ranges over point estimates, provenance for every number, depth over coverage, tone is negotiable but substance is not, and the user's own behavior is part of the system.

## Limitations

- It forecasts under uncertainty; it does not predict. Scenario weights are judgments, and the report says what would move them.
- It does not invent statistics. When it cannot source a base rate, it says so and asks you to verify. Use web search when available for competitors, prices, and regulation.
- Output quality depends on what you tell it. With thin input it will ask questions or state its assumptions.
- It is not legal, financial, or medical advice.
- Tested by its author on a handful of cases (`evals/evals.json`), not exhaustively. Please report failures.

## Reporting bugs

Please open a [GitHub Issue](https://github.com/Amrit-mishra07/strategic-premortem/issues). Include the prompt you used, what the skill produced, and what you expected instead. Outputs that were generic, overconfident, or arithmetically inconsistent are especially useful.

## Contributing

Issues and pull requests are welcome, especially:
- test cases where the output was generic, overconfident, or wrong (add them to `evals/evals.json`);
- domain references (hardware, biotech, marketplaces, nonprofits, public-sector projects);
- translations and region-specific notes.

## License

MIT. See [LICENSE](LICENSE). Created by [Amritanshu Mishra](https://github.com/Amrit-mishra07).
