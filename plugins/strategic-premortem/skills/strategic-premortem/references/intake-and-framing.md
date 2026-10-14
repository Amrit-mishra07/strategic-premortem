# Intake, Framing, and the Assumption Ledger

Contents: 1 Intake questions · 2 Assumed profile · 3 Challenging the framing · 4 Steelman · 5 Goal-fit check · 6 Assumption ledger · 7 Reference classes and the outside view · 8 Evidence quality

## 1. Intake questions

Ask only what would change the analysis. In priority order (the first five usually decide the verdict):

1. **The commitment.** What exactly will the user spend, give up, or promise, starting when? What is the realistic alternative use of that time and money? Opportunity cost belongs in every pre-mortem; "it might work" is not enough, it must beat the next best use of the same hours.
2. **Success definition.** Outcome, size, and date, in the user's terms. "Make money" is not a target; "₹/$X per month by month 6, or clear evidence a path to it exists" is. If they cannot say, that is the first finding.
3. **Resources.** Cash, and how much of it they can lose without damage; hours per week per person net of job/study/family; skills on the team; what already exists.
4. **Evidence so far.** Who said or did what? Separate compliments from commitments (see `economics.md` §1).
5. **The money path.** Who pays, for what, how much, why now, and by name or channel, where the first 100 customers come from.
6. **Constraints and risk tolerance.** What loss would be ruinous? Non-negotiables? Hard dates (exams, lease, visa, funding, a job offer)?
7. **Why them.** The specific advantage: access, skill, cost, distribution, timing, or insight others lack. "Passion" and "hard work" are not advantages here; everyone claims them.
8. **Landscape.** Known competitors and substitutes, including "do nothing", spreadsheets, and manual workarounds, plus anyone who controls access (platform, distributor, regulator, key supplier).
9. **Team dynamics (if more than one person).** Roles, decision rights, ownership split, and how committed each person really is. Commitment asymmetry among friends is a common silent failure.

Stage-specific additions:
- *Idea stage:* how did they come to believe the problem exists; who have they talked to, and what did those people do next?
- *Pre-launch:* what is the launch plan beyond "post it"; what is the smallest version that tests the riskiest assumption?
- *Early traction:* cohort retention, revenue per customer, source of customers, concentration, and what happened to the ones who left.
- *Scaling:* what breaks first at 3×; CAC trend; cash conversion cycle.
- *Internal project / decision:* who sponsors it, who can veto it, what is the budget cycle, and what happens if the sponsor leaves?

## 2. The assumed profile

When proceeding without answers, write three to six lines the user can correct, for example:

> Assumed profile — Team: 3 people, ~10 hrs/week each, no outside funding, ~$3k of spendable cash. Stage: idea validated only by conversations. Success = first $2k/month recurring by month 6. Correct me where this is wrong; it changes sections X and Y most.

State which sections are most sensitive to each assumption. Silent assumptions are the main source of confident wrong answers.

## 3. Challenging the framing

Do not accept the user's framing as given. Ask, and answer in the analysis:

**Is the problem worth solving?**
- Who has it, how often, how painfully? Is it a *painkiller* (they actively try to fix it today and spend money or effort doing so) or a *vitamin* (they agree it is nice)?
- What do they do today, including doing nothing? The real competitor is usually the status quo, a spreadsheet, a person, or "good enough".
- Is the problem a priority for whoever holds the budget, or only for someone without authority?

**Is the proposed solution viable?**
- Does it solve the problem well enough to beat the cost and effort of switching?
- Is it a *feature* (something a larger product will absorb), a *product*, or a *company*? Features can be real businesses only if distribution or speed is the moat.
- What must be true technically and operationally, and has anyone shown it can be done at the claimed cost?

**Does the business model make sense?**
- Who pays, and is it the same person who benefits? When they differ, the payer's incentives decide.
- Is revenue recurring, repeatable, or one-off? Does the margin survive real costs?
- Where does value get captured: by the user, or by a platform, supplier, or customer with more power?

**Is there a simpler or more defensible alternative?**
- A narrower segment, a service version done by hand first ("concierge"), a paid pilot instead of a build, selling the outcome instead of the software, a partnership instead of a product, or doing the unglamorous adjacent thing that reliably pays.
- What is a 10× cheaper way to learn whether this works?

## 4. Steelman

Before critique, write three to five lines: the strongest honest case for the idea, as its smartest defender would make it. Include the real insight, the conditions under which it wins, and the best version of the plan. If you cannot find a strong case, say so. It is a finding. This protects against rejecting good ideas for fixable flaws, and it makes the later criticism credible.

## 5. Goal-fit check

The user's stated goal can conflict with the vehicle they chose. Test it explicitly:

- Goal "reliable money" vs. vehicle "product with uncertain demand": a services or productized-service route may reach reliability faster, with less variance.
- Goal "learn and build a portfolio" vs. vehicle "venture that needs full-time commitment": learning may be maximized by a smaller, faster project.
- Goal "financial independence" vs. vehicle "a venture that consumes savings and has a long tail of outcomes".
- Goal "build something big" vs. vehicle "a niche tool with a hard ceiling".

If goal and vehicle diverge, say so plainly and show the better-fitting alternatives. This is often the most valuable single insight in the report.

## 6. The assumption ledger

**Extract.** Read the plan and list everything that must be true for it to work: about customers, price, cost, conversion, retention, timing, competitors' behavior, partners, regulation, technology, team capacity, and the user's own follow-through. Include assumptions the user has not noticed they are making. Typical hiding places: "customers will find us", "it will take two weeks", "the platform will keep allowing this", "we will keep working on this at this pace".

**Classify.** Mark each F / A / H / S (see SKILL.md). Most plans are ≥70% assumptions presented as facts.

**Rank.** Score each on:
- *Impact if wrong* — does the plan break, bend, or barely notice?
- *Uncertainty* — how little real evidence supports it?
- *Testability* — can it be tested cheaply and soon?

Load-bearing assumptions are high impact and high uncertainty. Pick five to eight.

**For each load-bearing assumption write:**
- the assumption in one sentence;
- current evidence and its quality (§8);
- the **falsifier**: the observation that would show it is wrong, with a number where possible;
- the **cheapest test**: what, how long, what it costs;
- what the user would do differently if it fails.

**Check the chain.** Plans need several assumptions to hold at once. Multiply roughly: five independent assumptions at 70% give about 17%; at 85% give about 44%. This is not a prediction. It shows why a plan "where each step is reasonable" can still be unlikely, and which assumptions to de-risk first. Where assumptions are correlated (for example, "customers care" drives conversion, retention, and price together), say so; the chain is then less pessimistic than independence implies, but failures also arrive together.

**Find the kill-assumption.** Usually one assumption, if false, makes the rest irrelevant (for example, "customers will pay for this"). Test it first, before building anything that depends on the others.

## 7. Reference classes and the outside view

Planners systematically underestimate time, cost, and difficulty and overestimate their own distinctiveness. Counter this by anchoring on the outside view first:

1. Name two or three reference classes the project belongs to (for example "student-founded B2C apps", "solo-founder SaaS in a niche vertical", "restaurants/cloud kitchens in a first-year", "internal platform migrations").
2. State what usually happens to projects in that class: how often they reach the milestone the user wants, and the common causes of failure. Use sourced figures when you have them; otherwise describe qualitatively and flag for verification.
3. Then adjust for specifics (the inside view): what concrete features of this project and team make it better or worse than the class? Adjust modestly and explain why. "We are different" must be backed by a mechanism.
4. Apply a planning-fallacy correction to schedules and state it ("assume build time is 1.5–2× your estimate unless you have shipped similar work on time before"). Ask for the user's track record: how did past estimates compare with actuals?

If the evidence supports a favorable adjustment, make it. The point is calibration, not pessimism.

## 8. Evidence quality

Weigh each piece of evidence by the cost to produce it and the incentive of its source.

| Evidence | Weight |
|---|---|
| Opinions, compliments, "I'd use that", survey intent | Very low: costless to say, biased toward politeness |
| Time given (follow-up calls, introductions, trial usage) | Low–moderate |
| Reputation staked (agreeing to be a reference, putting their name on a pilot) | Moderate |
| Money paid, especially unprompted, at a real price | High |
| Repeat payment, expansion, or unprompted referral | Very high |
| Observed behavior in the wild (what they did before you asked) | High |
| Secondhand claims (articles, "I heard", vendor reports) | Check source and incentive; vendors and sellers have reasons to inflate |

Also ask: Who is the source and what do they gain? Is the sample the user's friends and network (biased toward agreeable people)? Was the evidence gathered *before* or *after* the user pitched? Does the evidence test the riskiest assumption or a comfortable one?
