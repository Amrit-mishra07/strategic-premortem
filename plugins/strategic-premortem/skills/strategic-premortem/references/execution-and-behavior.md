# Execution, Human Behavior, and Dynamics

Contents: 1 Execution constraints · 2 Team and organizational friction · 3 Customer behavior · 4 The user's own behavior · 5 Feedback loops and delays · 6 Second- and third-order effects · 7 Irreversibility and path dependence · 8 Risk interactions

This file covers why a promising plan degrades on contact with reality, and how small effects compound. Use it to enrich the state model and the simulation, and to spot failure mechanisms the economics alone will not show.

## 1. Execution constraints

**Find the binding constraint.** At any stage one resource or step limits throughput: founder hours, a single skill, cash, a supplier, an approval, a sales cycle, a platform review. Name it for the current stage and predict how it *shifts* (early: building time; then: distribution; then: support load or cash). Optimizing anything other than the binding constraint is waste, and many plans do exactly that.

**Planning fallacy and the long tail.** Estimates assume the plan goes well. Real schedules include rework, waiting, and things nobody listed. Apply an explicit multiplier (state it), and treat the last 20% of any build (edge cases, polish, deployment, documentation, onboarding) as a large separate piece of work.

**Dependencies and critical path.** List what must happen before what, and who or what each step waits on: approvals, third-party integrations, payment setup, legal/compliance, app-store review, supplier lead times, other people's availability. Delays on the critical path move everything; delays elsewhere do not.

**Demo vs. production.** What works for ten friendly users in a demo often fails under real data, real edge cases, real load, and real misuse. Ask what happens with messy inputs, failure, support requests, and customers who behave unexpectedly.

**Technical debt and shortcuts.** Early shortcuts are often rational. Say which ones will hurt, and *when*: debt usually bites at the first scaling moment, the first security or reliability incident, or when a second person has to work in the code.

**Single points of failure.** One person who knows everything, one supplier, one channel, one customer, one cloud account, one API. For each, ask what happens if it vanishes for two weeks.

**Operational load.** Support, refunds, onboarding, reporting, compliance, invoicing, and chasing payment all grow with customers and rarely appear in plans. Estimate hours per customer per month and see when this consumes the team.

**Build vs. sell time.** Technical founders tend to over-invest in building and under-invest in selling; the reverse also occurs. Compare the planned split of hours to what the evidence says is the bottleneck.

## 2. Team and organizational friction

**For founding teams (especially friends):**
- *Commitment asymmetry:* one person does most of the work while ownership is equal, or one person drifts as other demands (exams, a job offer) grow. Resentment compounds quietly.
- *Decision rights:* who decides pricing, priorities, hiring, pivots, and when to stop? Deadlock between equals is a classic failure.
- *Ownership and exit:* unwritten equity splits, no vesting, and no plan for a member leaving create conflict exactly when stress is highest. Raise early; it is cheapest before money exists.
- *Skill gaps:* the missing skill (selling, operations, design, finance) is often the actual bottleneck.
- *Friendship risk:* what happens to the friendship if this goes badly? This is an honest cost to price in.
- *Motivation curve:* novelty carries the first weeks. When results lag effort, motivation tends to dip, often in the second to fourth month. Plan for it rather than assume it will not happen.

**For organizations (internal projects, corporate programs):**
- Sponsor dependence, competing priorities, reorganizations, budget cycles, and stakeholder vetoes (security, legal, procurement, IT).
- Adoption is a change-management problem: who loses status, time, or control if this succeeds? They will resist in passive ways (delays, "more requirements", low priority).
- Incentives: are the people whose cooperation you need rewarded for helping?

**Hiring and contractors:** onboarding lag, management overhead, quality variance, misaligned incentives (see principal-agent in `game-theory.md`).

## 3. Customer behavior

Customers are not rational optimizers of your value proposition. They are busy, risk-averse, habitual, and politically embedded. Common patterns:

- **Status quo bias and inertia.** Switching has a cost even when the new thing is better. Your product must beat the old way by a margin large enough to cover effort, risk, and doubt. Rule of thumb for planning: the gain must feel several times the pain of switching.
- **The four forces on a purchase.** Push of the current pain; pull of the new solution; anxiety about the new (risk, learning, trust); habit and inertia of the old. A weak push or strong anxiety kills sales regardless of product quality.
- **Loss aversion and risk avoidance, especially in B2B.** The buyer rarely gains much personally from success but may be blamed for failure. "Nobody gets fired for buying the incumbent." Reduce perceived risk (pilots, guarantees, references).
- **Champion vs. economic buyer vs. blocker.** Enthusiasm from a user without budget authority means little. Map who must say yes, and who can say no.
- **Present bias and low follow-through.** People intend to use the product, then do not. Activation and habit formation decide retention more than features.
- **Stated vs. revealed preference.** What they say they want, what they ask for, and what they pay for are three different things. Trust the last.
- **Trust as a gate.** New, small vendors face a trust deficit. Early customers may need social proof, a known name, or low-risk entry. Costly-to-fake signals (guarantees, public commitments, references) work better than claims.
- **Free expectations and discount conditioning.** Customers who got a discount, or free, learn to wait for it. Early promotions can set the price anchor for good.
- **Social proof cold start.** Many customers wait for others to adopt first (see the coordination structure in `game-theory.md`).

## 4. The user's own behavior

Model what the user will probably do, not only what they should do:
- **Optimism and confirmation bias.** Early positive signals are overweighted; negative signals are rationalized as "not the real customers".
- **Sunk cost and escalation.** The more spent, the harder it is to stop. This is why kill criteria must be set in advance.
- **Shiny-object pivoting vs. premature quitting.** Both errors are common. Pivots driven by boredom are different from pivots driven by evidence; the signals in `risk-and-decisions.md` §5 help tell them apart.
- **Reaction to bad news.** After a bad month, will the user work harder on the wrong thing, add features instead of selling, cut price, or go quiet? Predict the likely reaction and design a better default.
- **Overload.** Studies, jobs, and family compete for the same hours. A project that needs 15 hours a week from people with 6 spare is already failing in the plan.
- **Groupthink among friends.** Agreeable teams avoid conflict and challenge. Add an explicit devil's-advocate role or an outside reviewer.

## 5. Feedback loops and delays

Look for loops, not just chains.
- **Reinforcing loops** amplify: more customers → more references → more customers (virtuous); late delivery → churn → cash stress → shortcuts → worse quality → more churn (vicious). Ask which loop is most likely to dominate, and where the user can intervene early.
- **Balancing loops** resist: growth → support load → slower response → slower growth. Strong balancing loops explain why growth "stalls for no reason".
- **Delays** hide causes and effects: a quality problem today shows up as churn two months later; a hiring decision pays off in a quarter. Delays lead people to over-correct. Make delays explicit in the simulation.
- **Thresholds and tipping points:** a platform's attention, a competitor's reaction, a cash level below which suppliers change terms, a team size at which communication breaks. The system behaves linearly until it does not.

## 6. Second- and third-order effects

For each major action and each major event, ask "and then what?" at least twice, including how *other players* respond to the *consequences*.

Patterns:
- **Fixes that backfire.** A discount to lift conversion trains customers to wait for discounts. Hiring to relieve overload adds management load and cash burn. Adding features to win a deal increases maintenance and slows everything else.
- **Success problems.** Rapid growth overloads support and operations, concentrates revenue in a few customers, attracts competitors, triggers platform attention, and raises expectations for the next quarter. Include at least one in the upside scenario.
- **Metric gaming (Goodhart).** When a number becomes a target (signups, downloads, demos booked), behavior shifts to move the number rather than the underlying outcome.
- **Visibility effects.** Traction makes you visible to competitors and platforms; secrecy has costs too. Visibility is a choice with consequences either way.
- **Substitution and workarounds.** Customers, competitors, and regulators adapt. A rule or advantage is rarely stable.

## 7. Irreversibility and path dependence

Maintain an **irreversibility ledger**: decisions that are expensive or impossible to undo.
- Public commitments and promises; prices (anchors persist); positioning and brand story.
- Contracts, exclusivity, minimum purchases, personal guarantees, debt.
- Equity splits and early investor terms.
- Architecture choices and data models that constrain later change.
- Hiring and firing; relationship damage with early customers or partners.
- Time spent in a direction that forecloses another opportunity (a semester, a job offer, a window).

For each, ask: how reversible, at what cost, and what evidence should exist before committing? Prefer reversible moves while uncertainty is high; commit when evidence arrives or when the window is closing.

**Path dependence:** early choices (first customers, first channel, first price) shape later options. The first ten customers define what the product becomes. Choose them deliberately.

## 8. Risk interactions

Risks are rarely independent. Identify the **shared constraint** that links them: time, cash, attention, trust, a single dependency, or a single person. Risks that draw on the same constraint compound each other: a delay (time) plus a cash squeeze plus a cofounder's reduced hours can turn three manageable problems into one unrecoverable one. When building scenarios, look for these interlocks first (see "compound failure" in `simulation-method.md`).
