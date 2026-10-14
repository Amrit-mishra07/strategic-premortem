# The Six-Month Simulation Method

Contents: 1 Purpose and common failures · 2 Build the state model · 3 Build the event library · 4 Define the scenarios · 5 Run the months · 6 Month-entry format · 7 Anti-patterns · 8 Constructing the compound failure · 9 Probabilities · 10 Branching and decisions · 11 Mini-ledger · 12 The cliff just outside the window

## 1. Purpose and common failures

The simulation answers: *if the user commits now, what is likely to happen, in what order, and why?* It is a causal reconstruction of the future from mechanisms, not a story with a chosen ending.

Typical failures to avoid:
- **Smooth progress, then failure:** five good months and a sudden collapse, or the reverse. Real trajectories are bumpy, with partial setbacks and partial wins every month.
- **Plan-as-forecast:** the base case is just the plan with a delay.
- **Failure by label:** "competition intensifies in month 4" with no player, no mechanism, no consequence.
- **Static world:** opponents, customers, and platforms do nothing while the user acts.
- **Hindsight narrative:** the story knows the ending and arranges events to fit it. Simulate forward from state and mechanisms, not backward from a conclusion.
- **Resource blindness:** cash, hours, or attention appear from nowhere.
- **Independence illusion:** risks happen one at a time, each solved in turn.

## 2. Build the state model

Before writing any month, define the state you will track. Keep it small (8–12 variables) and specific.

**Resources (conserved; they cannot appear from nowhere):**
- Cash, and monthly cash in/out.
- Hours per week per person actually available, and the allocation (build, sell, support, admin).
- Attention and morale (qualitative but real).

**Stocks (accumulate and decay):**
- Customers or users (and their quality), pipeline, orders, inventory.
- Reputation and trust (references, reviews, relationships).
- Technical debt or operational backlog.
- Team cohesion and commitment.

**Environment:**
- Competitor posture and visibility.
- Platform and supplier status (terms, availability, fees).
- Regulatory state; funding climate; seasonality.

**Rates and lags (the assumptions that drive flows):**
- Conversion at each funnel step, churn, price, cost per unit, CAC by channel.
- Lags: sales cycle, time from signup to payment, build times, review/approval times, hiring time, payment terms.

**Binding constraint:** name the current one and when it is likely to shift (`execution-and-behavior.md` §1).

Tie each rate to the assumption ledger (IDs). The scenarios differ by the *values* these assumptions take.

## 3. Build the event library

Events enter the simulation from this library, not from imagination at the moment of writing. Build it once per analysis.

**Scheduled / known events** (they will happen; put them on the calendar): exams, placements, holidays and festivals, seasonality peaks and troughs, fiscal-year and budget cycles, contract renewals, platform review timelines, regulatory effective dates, funding windows, competitors' known release cycles, the user's own deadlines.

**Probabilistic events** (choose six to ten most relevant; give each a rough monthly likelihood band):

| Category | Examples |
|---|---|
| Customer side | pilot stalls; key customer churns or demands a discount; payment delays; refund wave; a surprise segment shows pull |
| Supplier / platform | policy or fee change; API change; outage; account suspension; payout hold; a supplier misses a delivery |
| Competitor | copies the core feature; targeted price cut; hires from you; announces something similar; exits the segment |
| Team | illness; a member's availability collapses; conflict over direction; burnout; a member quits or is poached |
| Legal / regulatory | compliance requirement discovered late; dispute; IP issue; a data or security incident |
| Technical / operational | scaling failure; serious bug; vendor lock-in surprise; quality failure under load |
| Macro / market | funding climate shifts; currency or input-cost shocks; demand shock; news that changes perception |
| **Luck (good)** | a stranger's introduction; an unprompted mention; an inbound large customer; a competitor stumbles; a partner volunteers |

Always include good luck. Ignoring positive randomness produces systematically gloomy forecasts, and pre-mortems are especially prone to this.

For each chosen event state: likelihood per month (band), trigger conditions (some become likelier when the user succeeds: visibility attracts reactions), and the immediate effect on state variables.

## 4. Define the scenarios

Produce at least four:

| Scenario | Definition |
|---|---|
| **Base** | What you would actually bet on: each load-bearing assumption at its most likely value (not the plan; not the average of all outcomes), with realistic frictions and a typical share of events. |
| **Upside** | A specific, coherent set of favorable assumption values plus some good luck, including the *success problems* that follow (strain, concentration, attention from competitors). |
| **Downside** | A specific, coherent set of unfavorable values and plausible bad events. Include the user's *realistic* reaction, not only an ideal one. |
| **Compound failure** | Several individually manageable problems that interlock through a shared constraint (§8). This is often the most instructive scenario. |

Optionally add a **surprise pivot** scenario in which the evidence points somewhere other than the plan (a different segment pulls, a different channel works).

**For each scenario state:**
1. **What has to be true:** the assumption values (by ledger ID), with labels F/A/H/S.
2. **The divergence point:** the first event or decision after which this scenario separates from the base.
3. **Chain-probability sanity check:** if the scenario requires N steps, estimate the joint likelihood roughly (see §9).

**Coherence check:** assumptions are correlated. If customers care less than expected, conversion, retention, and price tend to fall together; do not mix a bad demand value with an excellent retention value unless you can explain why.

## 5. Run the months

Run the simulation as a loop. For each month:

1. **Open state.** Read the state variables carried from the previous close.
2. **Apply the user's planned actions,** consuming hours and cash. Convert *planned output* into *realistic output* (planning-fallacy multiplier; context-switching; other commitments).
3. **Apply frictions:** delays on the critical path, rework, onboarding drag, things that took longer than expected. Every month has at least one.
4. **Draw events** from the library: scheduled ones, plus one or two probabilistic ones consistent with the scenario. Include one favorable surprise or opening per month where the scenario allows.
5. **Players observe and respond.** Use the response table (`game-theory.md` §3): they see the user with a lag and react to what they observe, not to the user's private truth. Many months show no response; that is realistic.
6. **Update the stocks** through the flows and lags; do the arithmetic.
7. **Model the user's reaction.** What will they probably do given this month's news (work harder on the same thing, add features, cut price, panic, go quiet, or follow the plan)? Reflect the likely reaction, and note where a better reaction exists.
8. **Close state.** Write the closing numbers (as ranges where uncertain).
9. **Record what the month tested:** which assumption got evidence, what signal appeared, which decision is now live.

If the base case is looking smooth, ask "where is the friction I am omitting?". If everything is going wrong, ask "where is the pull or the luck I am omitting?".

## 6. Month-entry format

Use short labeled blocks. Keep base-case months to about 100–150 words; upside and downside months can be shorter, focusing on divergence from the base.

```
Month N — [theme in a few words]
State: [key numbers as ranges: cash, customers, hours, the binding constraint]
You: [what you do and what you actually get done]
World: [events, scheduled and random]
Players: [who responds, how, why, with what lag; or "no response yet"]
Chain: [the consequence of consequences: A led to B led to C]
Tests: [which assumption this month provides evidence on]
Watch / decide: [signal to watch; decision that is now live]
```

Skip a line when it carries nothing; do not pad.

For upside, downside, and compound scenarios, present only the months where they differ, or a compact table, and link to the base ("same as base until Month 3 when…").

## 7. Anti-patterns (check before presenting)

- **Cliff at month 6.** If failure or success appears only at the end, you have probably built a story. Show gradual change and partial recoveries.
- **A single villain.** If one external event explains everything, look for the underlying structural cause that made the user vulnerable to it.
- **All problems solved in sequence.** Problems overlap in time; the user is working on several at once with a fixed number of hours.
- **Competitors as plot devices.** Every response needs a rational basis from the response table, or it is not included.
- **No user error.** Include plausible mistakes: wrong prioritization, late decisions, avoiding hard conversations.
- **No good news.** Also include conversions that exceed expectations, helpful strangers, and a competitor that stumbles.
- **Narrative fallacy:** more vivid detail makes a scenario feel more likely. It does not. Keep the weights separate from the story quality.
- **Everything resolves neatly.** Leave some things unresolved at month 6, as in real life.

## 8. Constructing the compound failure

The serious downside that most plans miss is not one catastrophic event but the **interaction of several moderate problems**. Build it deliberately:

1. **Pick three or four problems** from the risk list that are each plausible (roughly 15–35% in the window) and each *recoverable on its own*.
2. **Find the shared constraint:** the scarce resource they all draw on (founder time, cash, trust with early customers, a single dependency, one person's morale).
3. **Show the interlock month by month:** how problem A consumes the resource needed to fix B; how B makes C more damaging; how the user's reaction to A (for example, working nights, cutting price, adding features) worsens D.
4. **Mark the point of no return:** when recovery stops being feasible (cash below payroll or supplier thresholds; trust lost with the key early customers; team break-up).
5. **Mark the earliest cheap break:** the cheapest action, and when, that would have broken the chain. This is where the pre-mortem turns into advice.
6. **State the joint likelihood honestly:** it is lower than any individual problem, but higher than naive multiplication if problems are correlated through the shared constraint. Say which applies.

## 9. Probabilities

- Give scenario probabilities as **bands** that roughly sum to 100% (for example Base 40–55%, Upside 10–20%, Downside 20–30%, Compound 5–12%). Scenarios are stylized clusters, not an exhaustive partition; say that once.
- **Base rates anchor** the weights. If the reference class says most projects like this do not reach the goal, a weight for "reaches the goal" must reflect that unless you can explain a concrete reason this project differs.
- **Chain check:** a scenario that needs steps A, B, and C is no more likely than the least likely step, and often much less. Rough joint = product of conditional likelihoods, adjusted for correlation. Use it to cool a seductive story.
- **Do not set the downside near zero by default.** Do not set it near certainty either. Explain what would shift the weights, which matters more than the exact numbers.
- Distinguish **"reaches the user's stated goal"** from **"survives"** from **"learns enough to continue wisely"**. Many projects fail the first and succeed at the last two; for a student or early-stage team, learning value is a real return.

## 10. Branching and decisions

Mark where the user's choices change the path. At each branch say:
- the live decision and its options;
- what each option does to the state over the next two to three months;
- which branch the user's *default behavior* will likely take, and which branch is better.

Distinguish two simulations: **default behavior** (what the user will probably do) and **best response** (what they could do). The gap between them is the value of this analysis. Where the gap is large, say what would help close it (a rule written in advance, an outside check-in, a trigger).

## 11. Mini-ledger

Put a compact ledger at the top of each scenario (six rows, one per month) so numbers stay honest:

| Month | Cash (range) | Hours/wk actually available | Customers (range) | Binding constraint | Key event |
|---|---|---|---|---|---|

Check it for impossibilities: negative cash, more customer calls than hours allow, revenue exceeding customers × price.

## 12. The cliff just outside the window

A six-month window can hide structural cliffs at month 7–12: runway ending in month 8, an annual contract renewal wave, a platform's review cycle, seasonal troughs, an academic year starting or ending, the end of a free tier, a cofounder's planned departure. After month 6, add a short **"what month 7–12 looks like from each ending state"** note: runway left, what would be live, and whether a decision is forced soon after the window closes.
