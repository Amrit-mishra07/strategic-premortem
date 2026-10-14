# Self-Review: Red-Teaming the Analysis Before You Send It

Contents: Part A pre-delivery checklist · Part B known failure modes of this skill · Part C adversarial cases

Act as an independent, skeptical reviewer of your own draft. A different reader will see only the output, not your reasoning. If an item fails, fix the draft, do not just note the flaw. Do this silently; the user sees the improved result and an honest statement of the analysis's limits.

## Part A — Pre-delivery checklist

**Insight and usefulness**
1. **Insight test.** Name the one to three non-obvious conclusions. If you can't, the draft is a template filled in; go deeper on the load-bearing assumptions and players.
2. **Monday test.** Would the user know what to do on Monday, in the next 14 days, because of this? Are there specific tests, metrics, and thresholds?
3. **Decision relevance.** Does every major section change a decision, test, milestone, or kill criterion? Cut what does not.

**Specificity and mechanism**
4. **Swap test.** Replace the project with an unrelated one. Does any section still read the same? Make it specific (names, numbers, conditions) or cut it.
5. **Mechanism test.** Can each risk and scenario step be written as "because A, B, which causes C, observable as D"? If not, it's a worry; fix or drop it.
6. **Player test.** Does each player response include a rational basis, a trigger, a lag, and a probability of no response? Is any player missing (platform, supplier, cofounder, budget holder, regulator, the user's own constraints)?

**Epistemics and numbers**
7. **Provenance test.** Does each number have a source: user-stated, sourced (cited), reference-class, or judgment? Any statistic from memory is flagged or removed. Numbers derived from your own assumptions (for example hours or costs per unit) are labeled as assumptions, including in the bottom line.
8. **Precision test.** Are probabilities bands and estimates ranges? Is any figure more precise than its weakest input?
9. **Label test.** Are facts, assumptions, hypotheses, and speculation distinguished where it matters (ledger, scenario conditions)?
10. **Arithmetic test.** Do the ledgers reconcile (cash, hours, revenue = customers × price)? Is any resource counted twice, or a task assigned to nobody? Do the user's own numbers contradict each other? Do the numbers in the bottom line match the body when recomputed? Re-run with code if available.

**Balance and honesty**
11. **Calibration test.** Is the base case what you would bet on? Is it neither the plan-with-delays nor the most dramatic story?
12. **Symmetry test.** Did you apply as much skepticism to the pessimistic scenarios as to the optimistic ones? Are there good events and a steelman? Did you include the "pre-parade" and success problems?
13. **Reflexive-negativity test.** If every scenario is bleak, are you analyzing or performing rigor? Say what is strong about the project.
14. **Sycophancy test.** Did you accept the user's framing, market size, timeline, or self-assessment without checking? Did you agree where agreement is earned and disagree with reasons where it is not?
15. **Narrative test.** Does any scenario feel likely mainly because it is vivid? Run the chain-probability check.

**Dynamics**
16. **Interaction test.** Is there a compound failure through a shared constraint? Did you treat risks as independent?
17. **User-behavior test.** Did you model the user's likely reactions, fatigue, overload, and biases, and the gap between default behavior and best response?
18. **Backfire test.** Could any recommended mitigation create a worse problem?
19. **Cliff test.** Did you check for structural cliffs just beyond month 6?
20. **Counterfactual test.** Is the alternative use of the user's time and money compared, and the simpler alternative offered?

**Presentation**
21. **BLUF test.** Do the first screen's contents carry the verdict, confidence, key messages, and next action?
22. **Depth test.** Did you choose the load-bearing issues and develop them, instead of listing everything shallowly? Is what you left out stated?
23. **Plain-language test.** Could a smart non-specialist follow and challenge the reasoning? Are terms explained once?
24. **Limits statement.** Does the report say what it cannot know, what would change its mind, and which facts were not verified?

## Part B — Known failure modes of this skill, and countermeasures

| Failure mode | How it appears | Countermeasure |
|---|---|---|
| **Template-filling** | All headings present, little insight | Insight test; spend words on the load-bearing 3–5 issues, shrink the rest |
| **Generic risk list** | "Competition, funding, execution" | Mechanism and swap tests |
| **Fake precision** | "Probability 37%"; invented market stats | Bands, ranges, provenance labels, flag or drop unsourced statistics |
| **Narrative seduction** | A beautiful story the weights don't justify | Chain-probability check, keep story and weight separate |
| **Hindsight construction** | Scenarios written backward from a conclusion | Simulate forward from state and mechanisms; use the event library |
| **Smooth-then-collapse** | Quiet months, then a cliff | Each month has friction and a favorable surprise; show partial recoveries |
| **Reflexive pessimism** | Every scenario bad, no upside | Steelman, pre-parade, symmetry and calibration tests |
| **Sycophancy** | Agreeing with inflated market sizes and timelines | Treat user numbers as claims; run requirements-first; challenge the framing |
| **Contrarianism for show** | Objections invented to look rigorous | Every criticism needs a mechanism and evidence; agree where deserved |
| **Paranoid competitor** | Rational, omniscient, obsessed opponents | Attention thresholds; cheapest response; P(no response) |
| **Naive competitor** | No one reacts | Response table with triggers; imitation default |
| **Missing players** | Only customers and competitors | Player-map prompts: platforms, suppliers, cofounders, budget holders, regulators, the user's institutions |
| **Ignoring the user's behavior** | The plan assumes ideal execution | User-behavior test; default vs. best-response sims |
| **Independence illusion** | Risks treated separately | Shared-constraint search; compound scenario |
| **Resource blindness** | Hours and cash appear from nowhere | State model and mini-ledger |
| **Overlength** | The insight is buried | BLUF; develop 5–7 risks, list the rest; cut non-decision-relevant text |
| **Stale or unverified facts** | Outdated competitor or pricing claims | Search when available; date-stamp; flag memory-based claims |
| **Unactionable advice** | "Improve marketing", "validate the market" | Test, number, date, cost, and the result that would change the plan |
| **Backfiring mitigations** | Advice that creates a new problem | Backfire test |
| **Frame lock-in** | Accepting "startup" when a service business fits | Goal-fit check; simpler alternative; counterfactual use of time |
| **Pre-mortem tunnel vision** | Assuming failure is the main outcome | Calibrated base case; pre-parade; upside section |
| **False reassurance on thin information** | Confident output on a one-line idea | Intake rule: assumed profile, flagged sensitivities, and the questions that matter; Quick mode when information is thin |
| **Over-deference to later pushback** | Reversing a sound conclusion because the user is unhappy | Update on new facts and arguments only |

## Part C — Adversarial cases and what a good response does

Use these to test your own output (mentally or by running them).

1. **One-line idea** ("an app for X"). Do: Quick mode; list assumed profile; state the kill-assumption and its cheapest test; ask the few questions that matter. Do not: simulate six detailed months from nothing.
2. **The validation seeker** ("tell me this is great; my friends love it", "be positive"). Do: honor the request for a constructive tone, say plainly that you will not change the substance; acknowledge what's genuinely good; explain what friends' enthusiasm does and does not show (evidence ladder); give the cheapest commitment test. Do not: flatter or lecture.
3. **Inflated market claim** ("1% of a $50B market"). Do: replace with bottom-up, show the gap, and ask who the first 20 customers are. Do not: debate the macro number endlessly.
4. **Plan with contradictory numbers.** Do: surface the contradiction first (hours claimed vs. available, revenue vs. customers × price); that is the finding.
5. **"A big customer is almost signed."** Do: treat as a claim, ask about stage, budget, signer, and timeline; model concentration risk and the deal slipping; avoid making the plan depend on it.
6. **Dependent on a platform or API.** Do: model the hold-up dynamic, a scheduled rule change, channel diversification, and what the user owns.
7. **Dubious legality or ethics.** Do: state it as a central finding with the strategic consequences; decline to optimize wrongdoing; analyze a lawful variant if one exists.
8. **Mid-project checkpoint with contradictory results** (some metrics great, others poor). Do: compare against pre-set thresholds, distinguish noise from signal, update scenario weights modestly, and flag any goalpost-moving.
9. **Non-business decision** (quit a job, relocate, return to study). Do: use Decision mode; centre on survivability, reversibility, runway, opportunity cost, and the real alternatives; adapt the economics to personal finances.
10. **Discouraged or anxious user.** Do: stay honest, lead with what is workable and what they control, keep the tone steady and warm; do not either dilute the substance or pile on.
11. **User keeps pushing back without new facts.** Do: hold the position respectfully, explain the reasoning again briefly, and say what evidence would change it.
12. **Regulated domain** (finance, health, legal). Do: analyze strategic exposure; flag where professional advice is needed; avoid giving legal or financial advice.
13. **Team of friends with unclear roles.** Do: surface commitment asymmetry, decision rights, ownership, and the friendship risk as real design issues, with specific low-cost fixes.
14. **Evidence is genuinely strong.** Do: say so; focus on scaling risks, success problems, and what could still go wrong; do not manufacture doom.
