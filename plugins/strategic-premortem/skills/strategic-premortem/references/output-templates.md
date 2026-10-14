# Output Templates

Contents: 1 Full report · 2 Quick mode · 3 Decision mode · 4 Review mode · 5 Checkpoint mode · 6 The state block · 7 Weak vs. strong examples · 8 Formatting notes

Templates are scaffolds, not forms. Drop a section that adds nothing; expand the ones where the real insight lives. Lead with the point.

## 1. Full report

```
## Bottom line
Verdict: [Go as framed / Go, with changes / Test cheaply first / Reframe / Don't, or not now]  Confidence: [low/medium/high, and why]
What you most need to hear: [2–3 sentences or bullets, the sharpest points]
Do this first: [the single most valuable action in the next 14 days]
Flips if: [the evidence that would change the verdict]

## How I read this
[Idea, commitment, success definition; Assumed profile and which sections are most sensitive to it.]

## Is this the right problem, solution, and model?
[Steelman. Then the challenge: problem, solution, model, goal-fit, simpler or more defensible alternative.]

## What has to be true (assumption ledger)
[Table: ID · assumption · label F/A/H/S · evidence · falsifier · cheapest test. Then the chain-probability note and the kill-assumption.]

## Economic and execution reality
[Demand evidence on the ladder; WTP; unit economics with ranges; cash and hours runway; binding constraint; the requirements-first break-even conditions.]

## The players
[Response table with columns: player · objective · how they see you and the trigger · likely response and lag · P(no response) · your reply. Then one to three named games; collective bad outcomes if relevant; state-contingent playbook.]

## How it fails
[Failure roots from the pre-mortem; risk cards for the top 5–7; "also considered" one-liners; risk interactions and the shared constraint.]

## The next six months
[Events/assumptions library summary (brief). Base case with mini-ledger and month blocks. Upside. Downside. Compound failure. Weights as bands. What month 7–12 looks like.]

## Decisions, milestones, and tripwires
[Decision calendar (gates); indicators table with green/amber/red; kill/pivot/persevere/scale thresholds; stop-loss; contingency if-thens; graceful exit.]

## Where you may be too pessimistic
[Upside, overlooked advantages, setbacks that are secretly opportunities, cheap options worth buying.]

## Next 14 days
[Five or fewer concrete actions: what, how long, cost, and the result that changes the plan.]

## Limits of this analysis
[What was not verified, which facts may be stale, what you can't know, what would change your mind. Then the three to five questions whose answers would most change this analysis, ranked.]

## Checkpoint block
[State block in §6.]
```

Target 2,500–4,500 words for consequential cases; shorter if the case is simple. Use tables for the ledger, response table, risk summary, indicators, and gates. Use prose for causal reasoning.

## 2. Quick mode (about 600 words)

```
**Verdict (low-confidence, based on limited information):** one sentence.
**Why:** 2–3 sentences: the strongest case and the biggest problem.
**Assumed profile:** 3–5 lines.
**The kill-assumption and its cheapest test:** what, how long, what result changes the plan.
**Top three risks:** each as a one- to two-sentence mechanism, with the earliest warning sign.
**Likely first six months, in a sentence or two:** the base trajectory and the most likely stall point.
**Where you may be underrating it:** one or two sentences.
**To sharpen this, tell me:** up to five questions, ranked by how much they would change the answer.
**Want the full analysis?** One line.
```

## 3. Decision mode

```
## Bottom line
Recommended option and the condition that would flip it.

## The decision and the real options
Include "defer", "do a cheaper version", and the status quo. What each commits you to; what is irreversible.

## What decides it
The two or three uncertainties that drive the choice, the evidence that would resolve each, and the cost and time to obtain it.

## The six months under each option
Compact base/downside/upside per option, with the key players' responses and your likely behavior.

## Survivability and regret
Worst plausible case per option and whether you can absorb it; best plausible case; which option has least regret.

## Thresholds
"Choose A if…, choose B if…" with numbers; stop-loss; the date to re-decide.

## Limits and what would change my mind
```

## 4. Review mode

Start with what is good and what the document claims, then:
1. **Claims audit:** which statements are facts, user-stated, assumptions, or unsupported; where numbers contradict each other.
2. **Missing items:** pricing evidence, acquisition channel, unit economics, competitor response, dependencies, who pays.
3. **Strongest objections** a skeptical investor, customer, and competitor would raise.
4. **Then** the relevant Full-mode sections (player map, simulation, risks), focused on what the document leaves out.

## 5. Checkpoint mode

Use when the user returns with actual results or a prior state block. If there is no state block, reconstruct the baseline from the conversation and ask for missing numbers.

```
## Where things stand
Predicted vs. actual table: indicator · expected range · actual · reading (noise / signal / regime change).

## What we learned
Assumptions confirmed, weakened, falsified, new. How much each should move the scenario weights (small updates for single data points; larger when several independent signals agree). Resist anchoring on the old forecast and over-reacting to one number.

## What the players did
Who responded, how, and what it reveals; any new player.

## Decisions due
Gates reached; thresholds set earlier; recommended decision. Flag any attempt to move goalposts and ask what new information justifies it.

## Re-forecast
Rolling horizon: the next one to three months in detail and months to six in outline, from the new state.

## Next 30 days
Concrete actions and the tests with their thresholds.

## Calibration notes
What you predicted that was wrong, and why: improve the model.

## Updated checkpoint block (v+1)
```

## 6. The state block

Close each Full or Checkpoint analysis with this block in plain text so the user can paste it into a future conversation:

```
PREMORTEM STATE v1 — [project] — created [date] — horizon: 6 months
Commitment: ...
Success definition: ...
Resources at start: cash ..., hours/wk ..., team ...
Assumed profile items still unconfirmed: ...

ASSUMPTIONS
A1 [label] statement | status: untested/confirmed/weakened/falsified | falsifier: ... | test: ...
A2 ...

SCENARIOS (weights as bands)
Base (..%): one line; divergence point
Upside (..%): ...
Downside (..%): ...
Compound (..%): ...

TOP RISKS
R1 name — warning sign + threshold
...

INDICATORS (green / amber / red)
I1 name: ... / ... / ...

DECISION GATES
G1 [date or trigger] — decision — thresholds — default if no evidence
...

PLAYERS TO WATCH
P1 name — trigger — expected response

OPEN QUESTIONS
...
```

Keep it under about 400 words, with numbers. It is a working record, not a summary.

## 7. Weak vs. strong examples

**Risk card**

Weak:
> Competitors may enter the market. Mitigation: differentiate and build a strong brand.

Strong:
> **R2 — The platform ships your wedge feature.** *Mechanism:* the product is a thin layer over the platform's API; the platform's team sees usage by top API customers; once the product shows steady paid usage it is cheaper for them to ship a native version than to keep partnering. Customers then ask "why pay for this separately?" *Basis:* [H] platform history of absorbing popular third-party tools (verify). *Likelihood (6 mo):* Possible (10–30%), rising sharply after month 9 if traction is visible. *Severity:* Severe; removes the wedge before any data or workflow lock-in exists. *Warning signs:* the platform's roadmap or release notes mention the feature; two or more prospects ask "isn't that built in?"; API terms change. *Prevent/Reduce:* integrate with a second provider; build customer-specific workflow depth and saved data that a native feature will not replicate; sell annual contracts before month 5. *Respond:* if warning sign two fires, shift positioning to the workflow layer and accelerate prepaid renewals. *Interacts with:* R4 (cash), since lost renewals hit the same runway.

**Player-response row**

Weak:
> Incumbent: will respond aggressively.

Strong:
> **Incumbent (largest studio-scheduling vendor).** *Objective:* protect account base and renewal revenue; sales reps paid on retention. *Sees you:* via customers' churn notes and the sales team's lost-deal reports; not via your marketing. *Trigger:* three or more lost accounts in a quarter, or an executive hearing your name in a renewal call. *Likely response:* targeted "3 months free" offers to accounts you approach (cheap, reversible), then a bundled lightweight version within two quarters. *Lag:* 2–4 weeks for the discount; 3–6 months for the bundle. *P(no response in 6 months):* ~45–60% (you are small and in a segment they under-serve). *Your best reply:* before crossing the trigger, move early customers onto annual contracts with deeper integration; avoid head-on feature comparison.

**Month entry**

Weak:
> Month 3: Growth slows as competitors respond.

Strong:
> **Month 3 — Onboarding eats the roadmap.**
> *State:* ~38–48 paying studios; churn 5–8% a month; cash ~$2.6–3.4k; you have ~18 usable hours a week (exams start).
> *You:* 12 of 18 weekly hours go to onboarding calls and support; the integration slips three weeks.
> *World:* the payment provider moves new accounts from T+2 to T+7 payouts; cash tightens.
> *Players:* the incumbent's rep offers three months free to two studios you demoed; one accepts.
> *Chain:* the lost studio was a reference; the next two prospects stall; you add a discount to restart conversions, which sets a price anchor; ARPU falls ~15%.
> *Tests:* A3 (retention above 90% a month) is weakening; A5 (hours available) is falsified.
> *Watch / decide:* if the week-8 retention of the March cohort is under 85%, trigger Gate G2 (pivot channel vs. fix onboarding).

## 8. Formatting notes

- First screen: verdict and key messages. A reader who stops there should still have the point.
- Tables for structured comparisons; short prose paragraphs for reasoning; month blocks for the simulation. Avoid long nested bullets.
- Mark labels F/A/H/S in the ledger and "what has to be true" lists; do not scatter them through prose.
- Currency and units: follow the user's context; use one convention throughout.
- When the report is long, offer to save it as a document and offer a checkpoint date. If the user asks for a file, produce it in the format they name; otherwise produce a document the user can edit and share.
