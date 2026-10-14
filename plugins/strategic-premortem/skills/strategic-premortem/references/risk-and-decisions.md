# Risks, Decisions, Thresholds, and Opportunities

Contents: 1 Failure-first and success-first generation · 2 Risk cards · 3 Probability and severity bands · 4 Prioritizing · 5 Decision points · 6 Value of information and option value · 7 Thresholds and kill criteria · 8 Early-warning indicators · 9 Contingency plans · 10 Setbacks as opportunities · 11 Upside analysis

## 1. Failure-first and success-first generation

**The pre-mortem proper (prospective hindsight).** Imagine, as a fact, that it is month 6 (and separately month 12) and the project has clearly failed. Write the headline and a short obituary. Then ask what happened. People generate more and better causes when they treat failure as already having occurred than when they ask what *might* go wrong.

Procedure:
1. **State the failure concretely:** "By month 6 we have 4 paying customers, no cash, and two of three founders have stopped working on it." A vague failure produces vague causes.
2. **Generate causes independently** before looking at any list. Write ten or more, fast. Do not stop at the first plausible one.
3. **Probe each category** to catch what you missed: demand; economics; execution; team and people; competition and other players; dependencies (platform, supplier, channel); legal/regulatory; timing and macro; self-inflicted decisions (choices the user made); information failures (signals that were available but not noticed or not believed).
4. **Include failures in disguise:** things that look like success but cause failure, such as vanity growth, a large customer that consumes focus, funding that forces the wrong strategy, early praise that hides a retention problem, a "pivot" that restarts the clock too many times.
5. **Cluster to root causes.** Ten causes are usually three root mechanisms. Name the roots; they become the risk cards.
6. **Do the month-12 version briefly:** failure at month 12 often has different roots (slow decay, burnout, failure to scale, market shift).

**The pre-parade (success-first).** Now assume the project succeeded beyond expectations. Ask: Why? What did the user do or luck into? What resources, sequencing, or assumptions mattered? What is being undervalued in the plan today? And what *problems did the success create*? This finds opportunity and "success problems" (strain, concentration, attention from larger players).

Feed both outputs into the simulation (`simulation-method.md`) as events, assumption values, and scenario definitions.

## 2. Risk cards

Develop five to seven risks in full. List others in one line each ("also considered"). Use this card:

```
R# — Name (what, in plain words)
Mechanism: the causal chain: because A, B happens; which causes C; which shows up as D.
Basis: [F/A/H/S] what the chain rests on, and the evidence for it.
Likelihood (in the window): band (see §3) and why. Say how it changes with the user's own actions.
Severity: Minor / Serious / Severe / Ruinous, with reversibility (can it be undone, at what cost?).
Earliest warning signs: observable signals, with numbers or thresholds, and roughly when they would appear.
Prevent: actions that reduce likelihood.
Reduce: actions that cap the damage if it happens.
Respond: what to do when the warning sign fires, and the decision rule.
Interactions: other risks it feeds or is fed by; the shared constraint.
```

**Mechanism-first rule.** If you cannot write the chain, you have a worry, not a risk. Either find the mechanism or drop it (or mark as [S] with a one-line note).

**Specificity test.** Swap the user's project for a different one. If the card still reads the same, it is generic; add names, numbers, and conditions until it would not.

**Beware mitigations that backfire.** Check that the "prevent/reduce" action does not create a worse problem (discounting to improve conversion; hiring to relieve overload; adding features to win one deal).

## 3. Probability and severity bands

Use bands, not point estimates. State the window (default six months).

| Likelihood band | Meaning |
|---|---|
| Unlikely | under ~10% |
| Possible | ~10–30% |
| Plausible | ~30–60% |
| Likely | ~60–85% |
| Near-certain | over ~85% |

| Severity | Meaning |
|---|---|
| Minor | an annoyance; recoverable in days to weeks without lasting cost |
| Serious | costs a month or meaningful money; recoverable |
| Severe | threatens the viability of the venture or the stated goal |
| Ruinous | unrecoverable damage: financial ruin, legal exposure, lost key relationships, serious harm to the user's wider life |

Basis for each estimate: reference-class rate, evidence from the user's situation, or judgment. Say which. Be especially careful with likelihoods for events you can imagine vividly; vividness is not probability.

## 4. Prioritizing

Rank by, in this order:
1. **Ruin and irreversibility.** A small chance of an unrecoverable loss outranks a moderate chance of a recoverable one. Survival comes first, because surviving preserves the option to try again.
2. **Expected loss** (likelihood × severity), including the *time cost* of recovery.
3. **Detectability.** Risks with early, cheap warning signs are easier to handle than silent ones. Silent, severe risks deserve extra attention.
4. **Correlation.** Risks linked through a shared constraint rank higher than their individual scores suggest.
5. **Leverage.** The risks where a small action now changes the outcome the most.

Say explicitly which risks you consider "load-bearing" and why.

## 5. Decision points

A critical decision point is a moment when a small action can substantially change the future, or when a commitment becomes hard to reverse. Find them by looking for:
- **Irreversibility thresholds:** about to spend significant money, sign a contract, announce publicly, give up an alternative, quit something.
- **Information inflections:** a test, pilot, launch, or renewal about to deliver evidence.
- **Cost-of-delay inflections:** a window closing (a season, an application deadline, a competitor's window, a funding cycle).
- **Trigger events:** a competitor response, a platform change, a key customer's decision.
- **Resource cliffs:** cash or energy approaching a level that forces action.

For each, write a **decision gate**:

```
G# — When / what condition (date or trigger)
Question: the decision to be made.
Options: continue / adjust / pivot / pause / scale / stop.
Evidence needed: what you should know by then, and how you'll get it.
Thresholds: the numbers that choose between options (§7).
Default if evidence is missing: which option you take, and why.
Cost of delaying: what waiting costs.
```

Include decisions about **when to stop investing** and **when a setback is actually an opportunity** (§10).

## 6. Value of information and option value

**Wait only when waiting is worth it.** Waiting for more evidence is valuable if (a) the evidence can arrive soon enough, (b) it could change the decision, and (c) the cost of waiting (time, momentum, missed window, money) is less than the expected cost of deciding wrongly. If any of these fail, decide now, or decide the smaller reversible step now.

**Buy information cheaply.** Before committing, find the cheapest test that would change the decision: a paid pilot, a pre-order or deposit, a landing page with a real price, ten structured conversations aimed at commitment, a concierge or manual version, a single-channel experiment with a pre-set budget. State cost, duration, and the result that would change the plan.

**Option value.** Prefer structures that cap the downside and preserve upside: stage-gated spending, month-to-month contracts, a first version that earns before the second version is built, a parallel low-cost experiment. When uncertainty is high and reversibility is low, the right move is usually to buy an option, not to commit to the full plan.

**Asymmetric bets.** When the loss is small and bounded but the upside is large, take the bet even when the probability is low, if it is survivable and informative. Avoid the opposite shape (small gains, catastrophic tail).

## 7. Thresholds and kill criteria

Set these **before** the data arrives, in writing. Afterward, sunk cost, hope, and motivated reasoning distort every judgment.

For each key metric define four zones, derived from the economics rather than invented:

- **Kill / stop:** below this, the business as framed does not work and further investment is not justified. State what else you would do with the time.
- **Pivot:** the data say the plan is wrong in a specific way (for example retention is strong but acquisition is poor, which suggests changing channel; or acquisition is easy but retention is weak, which suggests the product or segment).
- **Persevere:** within the expected range; keep going; do not over-react to noise.
- **Scale / double down:** clearly above range and economics support more investment.

Add:
- **Stop-loss:** a maximum amount of time and money you are willing to spend before a gate, regardless of how it feels.
- **Minimum acceptable evidence** at each gate (for example "at least N paying customers at price P, with retention ≥ R after 8 weeks").
- **Pivot vs. persevere discipline:** pivot on evidence, not boredom. Evidence for pivoting: repeated, consistent signals across multiple customers; a specific mechanism that explains the failure. A sign you are not learning: running experiments without pre-defined success criteria, or changing the criteria after the results.
- **Provisional placeholders.** If a threshold cannot be derived from the economics or a sourced benchmark, label it a *provisional placeholder*, say how it will be calibrated (for example from the first two weeks of real data), and do not present it as an industry standard.
- **Goalpost check:** if the user later wants to move a threshold, require a new argument based on new information, not on discomfort.

## 8. Early-warning indicators

For each major risk and assumption choose indicators that are:
- **Leading** (change before the outcome) rather than lagging;
- **Observable** by the user at low cost;
- **Actionable** (a reading triggers a specific response);
- **Hard to game** (not vanity metrics).

Present as a table:

| Indicator | Why it matters | Green | Amber | Red | Cadence | Response if red |
|---|---|---|---|---|---|---|

Thresholds should come from the economics or reference classes; say where each number comes from. Typical categories: demand (conversion at each step, qualified conversations per week, commitments obtained), economics (CAC, payback, gross margin, cash runway), retention (week-4 and week-8 cohort retention, repeat orders), operations (delivery time, support load per customer, backlog), team (hours actually spent vs. committed, missed commitments), and external (competitor changes, platform notices, regulatory announcements).

## 9. Contingency plans

For the top risks and the critical branch points write **if-then** plans with a trigger and a first action, so the user does not improvise under stress:

- "If the largest customer asks for a discount or signals leaving → [response], and in parallel [diversify]."
- "If the platform changes terms → [switch plan], having already built [direct channel] by month X."
- "If a cofounder's weekly hours fall below N for two weeks → [conversation, role change, reallocation of equity/responsibility]."
- "If cash falls below [level] → [cost cuts in this order], and [decision about stopping]."
- "If an incumbent copies the core feature → [differentiation, lock-in, niche, or exit]."

Include a **graceful scale-down or exit plan**: how to stop with minimal damage (commitments to customers, money owed, relationships, what is salvageable, what you learned). A plan to stop well lowers the fear that keeps people in bad projects too long.

## 10. Setbacks as opportunities

A setback is an opportunity when it:
- reveals pull from an unexpected segment or use case (customers using the product differently than designed);
- shows a competitor's response validates the market, or exposes their weakness;
- fails a cheap test and prevents a much more expensive failure;
- forces a focus the user would not have chosen but which improves economics;
- uncovers a dependency or flaw while it is still cheap to fix;
- produces a customer complaint that points to a premium feature or a pricing change.

Say how to recognize each, and what to do (for example, interview the unexpected users; lean into the segment; renegotiate; document the learning).

## 11. Upside analysis

The user asked to be told where they may be *too pessimistic*. Look for:
- **Where the reference class understates this project:** a real distribution advantage, domain access, cost edge, or timing that most comparable projects lack; what mechanism makes it different?
- **Incumbent blind spots:** segments incumbents cannot or will not serve profitably; incentives that stop them from copying.
- **Adjacent opportunities:** paid pilots, partnerships, services revenue, a narrower niche with stronger economics, selling the outcome rather than the software.
- **Enabling changes:** technology, regulation, behavior shifts, or platform openings that lower cost or raise demand.
- **Asymmetric options:** inexpensive moves that could open large upside if they work.
- **Compounding assets:** reputation, data, relationships, skills, or audience that retain value even if this project stops.

Say what to do to put the user in position to capture it, and which signals would show the upside is real.
