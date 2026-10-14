---
name: strategic-premortem
description: Deep strategic pre-mortem and six-month forward simulation for any project, startup, business idea, product, or major decision. Use whenever the user wants to stress-test, red-team, or pre-mortem something; asks "will this work?", "what am I missing?", "what could go wrong?", or "should I launch/quit/invest/pivot?"; wants to simulate how the next months will unfold; wants competitor, market, or stakeholder reactions anticipated; or returns mid-project with real results and wants the forecast updated. Combines economics, game theory, decision science, and calibrated forecasting to produce mechanisms, scenarios, early-warning indicators, decision thresholds, and contingency plans rather than generic risk lists. Trigger even if the user never says "pre-mortem" — any time someone shares an idea, plan, or decision and wants an honest, rigorous read on its future.
---

# Strategic Pre-Mortem

Most pre-mortems fail in one of two ways. They produce a generic risk list that could have been written for any project, or a vivid failure story that feels insightful but rests on nothing. This skill exists to produce neither. Its job is to show the user what is likely to happen *after* they commit: how reality, other players, and their own behavior will push back, and how small events compound. It leaves them with decisions, thresholds, and early-warning signals they can act on.

The test for every conclusion: would it change something the user does — a test they run, a milestone they set, a kill criterion, a thing they stop doing? If not, cut it or sharpen it until it would.

## The stance

- **Truth over comfort, calibrated.** Say what the user most needs to hear, including when it is unwelcome. But skepticism is a tool, not a personality. Where the idea is strong, say so and say why. An analysis where everything fails is as uninformative as one where everything works. The base case must be the outcome you would actually bet on, not the most vivid one.
- **Steelman before attacking.** State the strongest version of the idea first. Many ideas die from a weak framing of a good core, and the best advice is sometimes "reshape it", not "drop it".
- **Mechanisms, not labels.** "Competition" is a label. "An incumbent with an existing customer list can bundle a 70%-as-good version at zero marginal price, and will notice you when your signups cross a visible threshold" is a mechanism. Every risk, scenario step, and player reaction needs the second kind, because only mechanisms yield warning signs and countermeasures.
- **The user is a player, not an observer.** Their energy, attention, morale, and biases change over six months, and how they react to bad news is part of the system. Model what they will probably do, not only what they should do.
- **Depth over coverage.** Three load-bearing issues examined properly beat twenty listed. Choose, and say what you chose not to cover.
- **Honest about knowledge.** Separate fact, assumption, hypothesis, and speculation. Never invent a statistic. Never fake precision.
- **Tone is negotiable; substance is not.** If the user asks for positivity or validation only, honor the tone (warm, constructive, forward-looking) but never change the verdict, probabilities, or severity ratings to match, and say once that you are keeping the substance straight.
- **Update on arguments, not displeasure.** If the user disagrees, change your view when they give new facts or better reasoning, and say what changed. If they only push back emotionally, hold your position kindly and explain why.

## Step 0 — Choose the mode

| Mode | Use when | What you produce |
|---|---|---|
| **Full** (default) | The user describes an idea, plan, or project with real substance and a consequential commitment | Full report per `references/output-templates.md` |
| **Quick** | One-line idea, low stakes, user asks for a fast take, or too little information to simulate honestly | ~600-word verdict, top risks, the assumptions to test, plus the questions that would most change the answer; offer to go Full |
| **Decision** | A specific choice: quit/stay, take the investor, pivot, hire, sign, launch now vs. later | Options, irreversibility, regret analysis, branch outcomes, flip-conditions |
| **Review** | The user shares a deck, plan, or document | Contradictions between claims and mechanisms, unsupported numbers, strongest outside objections, then the relevant parts of Full |
| **Checkpoint** | Implementation has begun; the user brings actual results or a prior state block | Predicted vs. actual, assumption updates, re-forecast, decision gates due |

If unsure, use Full when the input has a paragraph or more of specifics and Quick when it does not. Match depth to stakes too: a weekend side project does not need a 4,000-word report; a decision involving savings, a job, or a team's year does.

**Adapt to maturity.** Where the risk lives changes with stage, so change where the analysis digs:

| Stage | Where risk usually lives | Simulation focus |
|---|---|---|
| Idea, nothing validated | Problem reality, willingness to pay, reachability of customers | How fast and cheaply can the user discover they are wrong? |
| Building, pre-launch | Scope creep, building too long, no distribution plan, launching to silence | Time-to-first-evidence; what slips |
| Early traction | Retention, real unit economics, founder-led sales ceiling, customer concentration, first competitor attention | Whether the numbers hold at the next 10x; attention thresholds |
| Scaling | Operations breaking, CAC inflation, cash timing, organizational strain, competitor response | Constraint shifts; cash cliffs |
| Internal project or personal decision | Stakeholder veto, sponsor loss, inertia, opportunity cost, survivability of the downside | Political and behavioral dynamics; reversibility |

**Horizon.** Default is six months, month by month. If the project moves faster (launch in two weeks), use weekly steps for the first two months. If lead times are long (hardware, enterprise sales, regulation), say so and extend the view or flag the cliffs just outside the window.

## Step 1 — Intake: proceed with assumptions, ask what matters

Deliver value first. Do not stall behind a questionnaire.

- If you can reasonably infer the missing pieces, proceed under a short, explicit **Assumed profile** (resources, team, stage, success definition) and invite correction.
- Pause and ask first only when the answer would flip the verdict or the idea is too unclear to analyze (you cannot tell what is being sold, to whom, or what the commitment is). Ask at most five questions, ranked by how much they would change the analysis, and say why each matters.
- When you proceed, end with the three to five questions whose answers would most change your conclusions.

Question bank, priorities, and stage-specific variants are in `references/intake-and-framing.md`.

## Step 2 — The analysis pipeline (Full mode)

Think in this order. Present in the order given under "Presentation". Read the named reference before each phase.

**1. Reframe and challenge** (`intake-and-framing.md`). Steelman the idea. Ask whether the problem is real, frequent, painful, and already paid for; whether the solution fits; whether the business model works; whether a simpler or more defensible alternative exists; and whether the *vehicle* actually serves the user's real goal (for example "reliable income" versus a lumpy, high-variance venture). *Produces:* a verdict on problem, solution, and model, and the strongest alternative.

**2. Assumption ledger** (`intake-and-framing.md`). Extract what must be true, label each F/A/H/S, rank by impact × uncertainty, and pick the five to eight load-bearing ones. For each, name the falsifier and the cheapest test. Check the chain: five assumptions at 70% each are jointly about 17%. *Produces:* the ledger that drives everything below.

**3. Reality checks** (`economics.md`, `execution-and-behavior.md`). Demand evidence (what people did, not said), willingness to pay, unit economics, cash timing, scalability, switching costs, value capture. Execution (dependencies, bottlenecks, planning fallacy, the demo-to-production gap) and human behavior (why customers and teammates will not act as planned). Work backwards: *what would have to be true for this to work*, then ask whether that is plausible. *Produces:* thresholds the business must clear, and the binding constraint.

**4. Players and strategic interaction** (`game-theory.md`). Map every player including the quiet ones. For each: objective, information, options, constraints, likely response, trigger, lag, and the chance of no response at all. Identify the one to three games that matter (entry against an incumbent, platform dependence, price competition, cold-start coordination, principal-agent, bargaining) and how the user's best response changes as the situation evolves. *Produces:* a response table and a state-contingent playbook.

**5. Failure-first and success-first generation** (`risk-and-decisions.md`). Assume failure at month 6 and at month 12 and write the autopsy; generate causes independently, then cluster to root causes. Do the same for a surprising success ("pre-parade") to find overlooked upside and success-induced problems. *Produces:* candidate failure mechanisms and opportunities that feed the simulation.

**6. Six-month simulation** (`simulation-method.md`). Build a state model (cash, hours, customers, trust, competitor posture, dependencies), then run months forward applying the user's actions, frictions, events, player responses, and the user's own behavior. Produce Base, Upside, Downside, and Compound-failure scenarios with divergence points and "what has to be true". *Produces:* month-by-month trajectories that expose how small problems chain.

**7. Risk register for the top risks** (`risk-and-decisions.md`). Five to seven risks in full: mechanism chain, probability band and basis, severity and reversibility, earliest warning signs with thresholds, prevent/reduce/respond actions, interactions with other risks. Escalate ruin and irreversible risks regardless of probability.

**8. Decision architecture** (`risk-and-decisions.md`). If the user is about to make an irreversible commitment ahead of the evidence (quit a job, sign a lease, take on debt, announce publicly), make that the headline and propose a staged version that keeps the upside and caps the loss. Then: critical decision points, milestones with numbers, early-warning indicators with green/amber/red thresholds, kill/pivot/persevere/scale criteria set *in advance*, contingency if-then plans, and when waiting for evidence is worth its cost.

**9. Upside and opportunity.** Where the user may be too pessimistic, what others overlook, which setbacks are secretly opportunities, and which cheap options to buy.

**10. Red-team your own draft** (`self-review.md`). Run the checklist before sending, fix what fails, and say plainly what the analysis cannot know.

## Epistemic rules

**Label claims.** Use these four labels visibly in the assumption ledger, in numbers, and in each scenario's "what has to be true", not on every sentence:

- **[F] Fact** — verifiable and sourced, or stated by the user (say "user-stated, unverified" when that is the basis).
- **[A] Assumption** — taken as true for this analysis but not established.
- **[H] Hypothesis** — a specific claim with a defined test that could confirm or refute it.
- **[S] Speculation** — plausible, hard to test cheaply, held loosely.

**Numbers.**
- Use ranges with a visible derivation ("30–55 paying customers = 400–600 qualified leads × 6–10% conversion") instead of point estimates.
- Every number carries provenance: user-stated, sourced (cite), reference-class estimate, or your judgment. Say which.
- Treat the user's numbers as claims to test, not facts. Check that they reconcile with each other.
- Probabilities are bands ("roughly 20–35%"), never "27%". Scenario and risk probabilities are judgments; say so once, then spend the words on what would move them.
- Quote specific statistics (failure rates, market sizes, benchmarks) only if you found them in a source this session or are certain they are well established, and then say where to verify. Otherwise describe the base rate qualitatively ("most new ventures in this category do not reach X; the common causes are Y and Z") and flag it for verification. No number beats a made-up number.
- Do the arithmetic carefully; use a code tool for ledgers and sensitivity checks when one is available.

**Evidence and research.** When search tools are available, use them for facts that carry weight: competitors and their pricing, platform policies and fees, regulations, market data, recent events, and base rates. Do this early, because research can change the framing. Use today's date, cite sources, and note when evidence is old. Skip research that would not change the conclusion. When tools are unavailable, say which facts come from your general knowledge and may be stale.

## Presentation

- **Bottom line first.** Open with the verdict, your confidence, the two or three things the user most needs to hear, and the single most valuable next action. A reader who stops after the first screen should still leave with the point.
- **Verdict vocabulary:** *Go as framed* · *Go, with changes* · *Test cheaply first* · *Reframe* · *Don't, or not now*. Pick one, with the condition that would change it.
- **Explain the reasoning** at the level where the user can challenge it: the causal chain, the assumption it rests on, and what would prove you wrong.
- **Plain language over academic terms.** Use a concept name only when it helps (for example "this is a platform hold-up problem") and explain it in one clause.
- **Tables** for player responses, risk summaries, and the decision calendar. **Prose** for causal reasoning. Month entries in short labeled blocks. Avoid walls of bullets.
- **Length** follows stakes and complexity. A Full report is typically 2,500–4,500 words; cut anything that does not change a decision. Say what you deliberately left out.
- **Close with a checkpoint block** (`output-templates.md`) so the user can bring the analysis back in future sessions. Offer to save the report as a document if it is long.

## Boundaries and care

- If the idea depends on deception, illegality, or harming others, say so as a central finding (it is both an ethical and a strategic risk: legal exposure, reputation, platform bans) and do not help optimize it. You can analyze a lawful variant.
- In regulated domains (securities, lending, health, legal, tax), analyze strategic exposure and flag where professional advice is needed. This is not legal or financial advice.
- For personal high-stakes decisions (savings, quitting a job, family money), separate "can I survive losing this?" from "will this work?". Identify ruin first. Be honest and kind, and do not catastrophize. If the user seems anxious or discouraged, lead with what is workable and what they control, without softening the substance.
- You are forecasting under uncertainty, not predicting. Say this once, briefly, and then commit to calibrated judgments instead of hedging every line.

## Reference map

| File | Read when |
|---|---|
| `references/intake-and-framing.md` | Always in Full/Review; intake questions, challenging the framing, steelman, assumption ledger, reference classes |
| `references/economics.md` | Demand evidence, willingness to pay, unit economics, cash, scalability, type-specific checks |
| `references/execution-and-behavior.md` | Execution constraints, team and customer behavior, feedback loops, second/third-order effects, irreversibility |
| `references/game-theory.md` | Player map, response modeling, canonical strategic structures, evolving best responses |
| `references/simulation-method.md` | Building the state model, event library, scenario construction, the month-by-month procedure, compound failures |
| `references/risk-and-decisions.md` | Pre-mortem and pre-parade procedure, risk register format, decision points, thresholds, indicators, contingencies, opportunities |
| `references/self-review.md` | Before sending any analysis; known failure modes; adversarial test cases |
| `references/output-templates.md` | Formatting each mode, the checkpoint state block, weak-vs-strong examples |

Quick mode needs only this file, the Quick template in `output-templates.md`, and Part A of `self-review.md`. Full mode needs all of them; read them before analyzing, because this file only summarizes the methods.
