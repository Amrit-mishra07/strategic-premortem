# Game Theory for Real Projects

Contents: 1 What goes wrong · 2 The player map · 3 Response modeling · 4 Calibrating rationality · 5 Strategic structures library · 6 Collective bad outcomes · 7 Your best response over time · 8 What to put in the report

Game theory here is a discipline for answering one question: **given what each player wants, knows, and can do, what will they actually do when this idea enters the world, and what should I do in return?** It is not vocabulary. If you name a concept (Prisoner's Dilemma, hold-up) without deriving what a specific player does and why, the analysis has failed.

## 1. What goes wrong

- **"Competitors may respond"**: no player, no trigger, no response, no probability. Useless.
- **Paranoid model:** every player is rational, informed, and obsessed with you. In reality most players are busy, slow, and unaware until you are visible.
- **Naive model:** nobody reacts. Large players *do* react once you matter, and cheaply.
- **Missing players:** the model includes customers and competitors but forgets platforms, payment processors, suppliers, employees, cofounders, regulators, the customer's boss, and the user's own family and school.
- **Static thinking:** treating others' strategies as fixed rather than responses to your moves and to what they can observe.

## 2. The player map

List every player whose decisions affect the outcome. Prompt categories:

- **Demand side:** end users, buyers/budget holders, champions, blockers, gatekeepers (IT, legal, procurement), resellers.
- **Supply side:** suppliers, contractors, talent, infrastructure and API providers.
- **Competition:** direct competitors, indirect competitors, substitutes (including the manual way and doing nothing), potential entrants, incumbents in adjacent markets, open-source or free alternatives.
- **Platforms and gatekeepers:** app stores, marketplaces, search/social algorithms, payment processors, cloud providers, data providers.
- **Capital and partners:** investors, lenders, accelerators, strategic partners, distributors, complementors.
- **Authority:** regulators, standards bodies, tax and licensing, institutions (university, employer).
- **Internal:** cofounders, employees, early hires, advisors, family who depend on the user's income or time.

Keep the **three to eight** players who matter most and mention the rest in one line.

## 3. Response modeling

For each key player complete this record (a table works well in the report):

| Field | Question |
|---|---|
| **Objective** | What do they maximize? Profit, growth, career safety, a metric, avoiding blame, time? Individuals inside organizations differ from the organization. |
| **Information** | What can they see about the user, when, and from where (public metrics, customer complaints, app rankings, sales calls)? They respond to what they *observe*, not to the user's private truth, and with a lag. |
| **Options** | The cheap-to-costly menu available to them. |
| **Constraints** | Contracts, margins, cannibalization, organizational speed, reputation, regulation, capital. |
| **Attention trigger** | What would make them notice? (Losing accounts, a press mention, crossing a share or growth threshold, a customer asking "why can't you do this?") |
| **Likely response** | The cheapest action that serves their objective, conditional on the trigger. |
| **Lag** | Days, weeks, quarters? |
| **P(no response)** | Explicit probability band; at early stage it is often high. |
| **User's best reply** | How the user should respond to each plausible response. |

**Six questions that generate the response:**
1. *What would I do in their position, with their incentives, margins, and org chart?* Not what would hurt the user most.
2. *Is responding in their interest?* Fighting costs money and cannibalizes; if the user's segment is small or low-margin, ignoring may be rational.
3. *Do they see the user, and what do they see?*
4. *What is the cheapest response that works?* Typical menu, cheap to costly: ignore → copy or bundle a "good enough" feature → targeted discount or free offer to the user's accounts → exclusive contracts, loyalty terms, or partner pressure → FUD (fear, uncertainty, doubt) and legal threats → hire away people or acquire → block access (platform/API rules).
5. *Is their threat credible?* A threat is credible only if carrying it out is rational for them when the time comes, or they have committed in a way that makes backing down costly.
6. *What do their reactions reveal?* A strong response signals the market matters; silence may be an unexploited window or hidden preparation. Say which and why.

## 4. Calibrating rationality

- **Attention thresholds are real.** Large players often ignore challengers below a visibility level. Staying under it while building defensible assets is a legitimate strategy; so is the opposite (making noise early to attract partners or capital). Choose deliberately.
- **Organizations are slow and political.** Product roadmaps, quarterly goals, and cannibalization fears delay responses for quarters. Incumbents can be rationally unwilling to serve the segment you are attacking (low margin, awkward for their model).
- **Targeted responses are cheap.** An incumbent can offer a discount only to the accounts you approach; it costs them little and you much.
- **Imitation is the default competitive response** when a feature is visible and copyable; it is usually the first thing that happens when a product shows traction.
- **Bounded rationality cuts both ways.** Players make mistakes, but do not build your plan on them making mistakes.
- **Sanity check against history:** how did this player respond to previous entrants or similar moves? Past behavior is stronger evidence than theory.

## 5. Strategic structures library

Use the ones that apply. For each: *signs it applies → the logic → what to do*.

**Entry against an incumbent (accommodate or fight).**
Signs: you target customers or profits an established player currently serves. Logic: fighting is costly, so incumbents fight when the entrant threatens core profit or could grow into it; entrants that look small, non-overlapping, or complementary ("puppy dog") are often tolerated, while those attacking the core invite a response. Move: pick positioning against visibility; win a segment the incumbent profitably ignores; accumulate assets that survive a response (contracts, integrations, data, community, reputation) before becoming visible; consider whether an acquisition is the realistic upside.

**Price competition and commoditization.**
Signs: similar products, easy comparison, low switching costs. Logic: price drifts toward marginal cost; price wars are won by the party with lower costs, deeper cash, or ability to cross-subsidize; targeted price cuts are cheap for incumbents. Move: compete on dimensions that are hard to compare by price, raise switching costs through workflow integration, avoid direct price comparison, and compute **war arithmetic** (how long can you survive at their price; how long can they).

**Network effects, tipping, and cold start.**
Signs: value depends on other users, or two sides must both show up. Logic: early value is near zero, people wait for others (a coordination problem), participants multi-home, and whoever reaches critical mass first may win. Move: start with a small, dense network (one campus, one city, one niche), subsidize the scarcer side, create single-player value (useful even with no network), and sequence the sides.

**Platform dependence and hold-up.**
Signs: your product, distribution, or traffic depends on someone else's API, store, marketplace, or algorithm. Logic: once dependent, you cannot credibly threaten to leave; the platform's best response over time is to raise fees, change rules, copy successful complements, or reduce your visibility. Move: measure dependence (share of revenue/traffic/ functionality via the platform), diversify channels, own the customer relationship (direct contact, contracts), avoid being "feature-sized", and plan for the rule change as a scheduled event.

**Principal–agent and incentive misalignment.**
Signs: someone acts on your behalf and you cannot fully observe effort or intent (cofounders with unequal stakes, employees, contractors, agencies, sales partners, suppliers). Logic: agents optimize their own payoffs; effort that is unobservable tends to shrink; misalignment shows up under stress. Move: align payoffs (vesting, milestone pay, commissions on outcomes), make progress observable, keep skin in the game, and verify rather than hope.

**Information asymmetry: adverse selection, moral hazard, signaling.**
Signs: buyers cannot judge quality before purchase, or counterparties know more than you. Logic: if buyers cannot tell good from bad, they discount everything, driving out the good (the "lemons" problem); parties behave worse when shielded from consequences (moral hazard). Claims are cheap; costly signals (guarantees, trials, escrow, third-party validation, track record) are credible. Move: design for verifiability and trust; offer risk-reversal; build reputation deliberately.

**Bargaining power and hold-up (customers, suppliers, investors, partners).**
Signs: concentration (one big customer or supplier), time pressure, or no alternatives. Logic: the party with better outside options and less urgency captures the surplus; early concessions become anchors; needing money *now* produces worse terms. Move: preserve alternatives, avoid single-customer dependence, negotiate before you are desperate, sequence deals so each strengthens the next.

**Prisoner's dilemma, race to the bottom, and commons problems.**
Signs: everyone would be better off with restraint, yet each gains by cutting price, bidding up ads or talent, or over-promising. Logic: individually rational moves yield a collectively bad outcome; the user can trigger one by entering aggressively or be caught in someone else's. Inside teams, the same structure appears as free-riding. Move: avoid starting wars you cannot outlast, compete on non-price dimensions, signal restraint, and exit contested spaces early.

**Coordination games and focal points.**
Signs: adoption needs others to act at the same time ("we'll buy once others do"; "we'll use it once everyone's on it"). Logic: multiple stable outcomes exist (everyone waits vs. everyone adopts); the market settles on whichever is focal. Move: create a focal point (an anchor customer, a respected endorser, a standard), reduce the cost of moving first, and seed a cluster rather than spreading thin.

**War of attrition.**
Signs: both sides lose each period and the one who outlasts wins. Logic: staying power (cash, patience, cost structure, alternatives) decides; announcing intent to stay can change the other side's calculation. Move: estimate staying-power asymmetry honestly; avoid wars you cannot outlast; change the game rather than endure it.

**Winner's curse and auctions.**
Signs: you bid for scarce inputs (ad slots, talent, deals, inventory, locations). Logic: the winner is often the one who overestimated value; competitive bidding erodes margin. Move: bid below your estimated value, find non-auction channels, and skip contested inventory.

**Signaling vs. cheap talk.**
Signs: judging evidence from customers, investors, or partners. Logic: statements that cost nothing to make carry little information; actions that are costly to fake are informative. "Sounds great, let's talk" costs nothing; a signed pilot or payment does. Move: weight evidence by the cost to the sayer; design asks that force costly signals.

**Repeated games and reputation.**
Signs: you will deal with the same players again (a campus, a city, a niche industry, a community). Logic: reputation makes cooperation rational; one burned relationship spreads. Move: protect early reputation, over-deliver to the first customers, and keep promises you can keep.

**Preemption and mover advantages.**
Signs: scarce assets (exclusive distribution, locations, key talent, data, a regulatory window). Logic: early movers lock them up; fast followers with deeper resources can overtake once the market is proven. Move: decide whether the advantage lies in being first (lock-in available) or second (learn from others' errors), and act accordingly.

## 6. Collective bad outcomes

The user asked specifically for situations where *individually rational choices produce a bad result for everyone*. Check for:
- **Discount spirals:** everyone cuts price to win share; margins vanish.
- **Customers all waiting:** each prefers to adopt after others, so nobody adopts.
- **Platform squeeze:** the platform extracts so much from complementors that the ecosystem weakens.
- **Free-riding in teams:** each member shirks because the cost is shared.
- **Funding herd behavior:** investors follow each other in and out; funding climates change independent of your merit.
- **Ad and talent bidding wars:** costs rise until acquisition economics break.
- **Mutually destructive exclusivity or standards fights.**
Ask: does the user's entry *create or trigger* one of these? Is the user likely to be collateral damage in someone else's? What would a restraint signal or a different positioning change?

## 7. Your best response over time

The user's best move is a function of the *state of the game*. Write a state-contingent playbook rather than a single strategy:

> *While below the attention threshold* (rough marker): build assets that survive a response; avoid features that make you look like a direct threat; get paid customers. *When you cross it:* expect a cheap response (copy, targeted discount). Prepare the counter in advance (lock-in, annual contracts, depth of integration). *If the incumbent responds with R1:* do X. *If with R2:* do Y. *If no response by [time]:* treat as an open window and accelerate in segment Z, or suspect hidden preparation and check for signals A, B.

Include:
- **Two or three branch points** (for example "platform changes API terms", "incumbent bundles a feature", "largest customer asks for a discount") with the user's best reply on each branch and what it costs.
- **No-regret moves:** actions that are good in all branches (earn real revenue, build direct relationships with customers, reduce a single dependency, extend runway). Do these first.
- **Bets:** actions good only in some branches; sequence them after information arrives (see option value in `risk-and-decisions.md` §6).
- **Commitment and credibility:** public commitments (prices, roadmaps, guarantees) change others' behavior. Sometimes you want credible commitment (to deter, to reassure customers); sometimes you want to preserve flexibility.
- **Minimax regret check** for irreversible choices: which option has the least bad worst plausible outcome, and does that matter more than the expected outcome given the user's survivability?

## 8. What to put in the report

- A **player-response table** with four to eight rows, specific and conditional.
- **One to three named games** that matter most, each in a short paragraph: why this structure applies, the likely equilibrium or pattern, and the conditions under which the outcome changes.
- A **state-contingent playbook** with branch points.
- A line on **no-response probabilities** and what silence would mean.
- Explicit mention of **collective bad outcomes** if relevant, including the user's role.
