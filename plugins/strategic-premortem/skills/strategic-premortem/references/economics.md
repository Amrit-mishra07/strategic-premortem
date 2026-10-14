# Economic Reality Checks

Contents: 1 Apparent demand vs. real demand · 2 Willingness to pay · 3 Unit economics · 4 Cash flow and runway · 5 Distribution and customer acquisition · 6 Scalability and switching costs · 7 Value capture · 8 Market sizing · 9 Requirements-first method · 10 Checks by project type · 11 Arithmetic hygiene

The question this file answers: **is there a sustainable business here, or only apparent demand?** Apparent demand is attention, compliments, free usage, and one-off sales. A sustainable business has customers who pay a price above the full cost of serving and acquiring them, repeatedly, through channels that keep working as volume grows.

## 1. Apparent demand vs. real demand

Common traps that look like demand:
- **Friends, family, and network.** They buy to be supportive. Their conversion rate does not transfer to strangers.
- **Waitlists and sign-ups.** Costless. Ask what share converts to payment, and look at who signed up (curious, or in pain?).
- **Free users.** Free usage measures price sensitivity at zero. The step from $0 to any price usually loses most users; test it early.
- **Discount-driven sales.** Demand that disappears at full price is demand for the discount.
- **Novelty and launch spikes.** A first-week surge is not retention. Look at week 4, week 8, month 3.
- **One large or unusual customer.** Concentration hides fragility.
- **Seasonality.** A peak month mistaken for a trend (exams, festivals, fiscal year-ends, holidays).
- **Surveys and "would you pay".** Stated willingness to pay overstates real willingness to pay, often by a lot. A price put in front of someone who must act is far more informative.

Climb the **commitment ladder** (see `intake-and-framing.md` §8): opinion → time → reputation → money → repeat money. Say where the user's evidence sits and what the next rung would be.

## 2. Willingness to pay

Derive it, do not assume it.
- **Anchor on current spend.** What do customers pay now for the alternative, in money and in time? A tool that saves one hour a week is worth the value of that hour *to the person who feels the hour*, which may not be the person who approves the budget.
- **Value of the problem.** What does the problem cost them in money, risk, or stress? Price is usually a fraction of captured value, and customers will not pay more than they can justify to themselves or their boss.
- **Budget path.** Who signs? Is there an existing budget line, or must one be created (which is slow and often fails)? How long from first contact to payment?
- **Who pays vs. who benefits.** If they differ, the payer's incentives decide the sale.
- **Comparables.** What do adjacent products charge? Is the user's price credible next to them, given brand and trust?
- **Price test.** The cheapest strong evidence is a real price in front of real prospects asking for money or a binding commitment.

## 3. Unit economics

Compute the economics of *one unit* (one customer, one order, one project) under realistic costs, then see whether the totals can ever cover fixed costs and the user's time.

**For recurring products (software, subscriptions):**
- Revenue per customer per month; gross margin after hosting, payment fees, support, refunds, and any third-party API costs (these scale with usage and can invert margins).
- **CAC:** all sales and marketing cost, including the founders' time at a stated hourly value, divided by *new paying customers*. Separate organic from paid; organic rarely scales on demand.
- **Payback:** months of gross margin needed to recover CAC. Payback beyond runway means growth consumes cash faster than it returns.
- **Retention:** monthly churn, and cohort curves if available. A leaky bucket makes growth expensive forever.
- **LTV:** use gross margin, a truncated horizon (say 12–24 months), and observed churn. Be skeptical of any LTV that assumes years of retention from a product that has existed for weeks. LTV:CAC is meaningless without payback and cash context.

**For transactional or physical businesses (food, retail, delivery, services):**
- Contribution per order: price − ingredients/COGS − packaging − delivery − payment fees − platform commission − refunds/wastage − variable labor.
- Break-even volume: fixed costs ÷ contribution per order. Compare against realistic demand in the catchment, not hoped-for demand.
- Capacity and utilization: what is the peak vs. average load; what is idle time costing; what happens at 2× demand?
- Time cost: if the founders do the work, what is their effective hourly rate? Many "profitable" side businesses pay below minimum wage once time is counted. That may be acceptable (learning, option value), but say it.

**For services and agencies:**
- Billable utilization, realized price after scope creep, delivery cost, sales time per project, collection time, and client concentration. Revenue is lumpy and capacity-capped; reliability comes from repeat clients and retainer structures.

## 4. Cash flow and runway

Profit is not cash. Check timing:
- **Cash conversion:** do you pay suppliers, contractors, or ad platforms before customers pay you? Enterprise and institutional customers often pay in 30–90 days; platforms may hold payouts; annual contracts help, refunds hurt.
- **Fixed commitments:** subscriptions, rent, salaries, loans, minimum purchase quantities, annual tool licenses, taxes and compliance costs.
- **Runway** = cash ÷ net monthly burn. Compute it under base and downside assumptions. Also compute **hours runway**: how many months can the team sustain current weekly hours given exams, jobs, and fatigue? For many small teams time runs out before money does.
- **Default alive or default dead?** At current growth and costs, does the business reach break-even before cash or energy runs out? If not, what must change, by when?
- **Minimum viable cash buffer** including working capital and a contingency for the plausible shocks in the simulation.

## 5. Distribution and customer acquisition

Distribution is usually the real problem, not the product.
- **First ten, first hundred, first thousand are different problems** with different channels. Founder-led outreach may yield the first ten; the first hundred needs a repeatable channel.
- For each channel (direct outreach, content, communities, partnerships, paid ads, marketplaces, referrals, events): expected volume, cost, time to results, and whether it saturates. Channels decay as they get crowded and as audiences are used up.
- **Name the first 20 customers.** Real people, companies, or places and how you would reach each. If the user cannot, "we'll find them online" is an assumption, not a plan.
- **Channel dependence:** what share of customers arrive through a single channel someone else controls (a search engine, a social algorithm, an app store, a marketplace)? That is a risk and a bargaining weakness (see `game-theory.md`).

## 6. Scalability and switching costs

- **What breaks at 10×?** Manual work, founder time, support load, quality control, infrastructure cost, supplier capacity, compliance. Does cost per unit fall, rise, or hold with volume?
- **Is the early margin an artifact of doing things that don't scale?** If yes, say what automation, hiring, or pricing change closes the gap.
- **Switching costs for customers:** contracts, data lock-in, workflow integration, habit, retraining, network ties. Low switching costs make acquisition easy and retention hard; high switching costs make acquisition hard and retention strong. The same applies to competitors' customers you want to win.
- **Moats that are real vs. claimed:** exclusive supply, regulation, proprietary data that improves with use, integration depth, brand with trust, network effects, cost advantage, distribution control. Speed and "execution" are not moats unless they compound.

## 7. Value capture

Who ends up with the profit? A business can create value and still capture little if:
- a platform, marketplace, or payment provider sets the fee and can raise it;
- one supplier or one customer has more bargaining power than you;
- the product is a commodity complement to someone else's offering;
- customers can capture the value themselves at low cost (build in-house, use a free alternative).
Identify where in the value chain the margin sits and whether the user can reach it.

## 8. Market sizing

Bottom-up beats top-down. "1% of a $50B market" is not a plan.
- Count reachable customers: how many exist in the *segment you can actually serve and reach in six to twelve months*? Multiply by a realistic conversion rate and a defensible price. Show the range.
- Distinguish total market, serviceable market (your product and geography), and obtainable (what you can win given your channels and capacity).
- Check that the first customers can pay enough to support the business: if the reachable segment is small, can it still sustain the user's goal?

## 9. Requirements-first method

Instead of forecasting from the plan, work backwards from the goal:
1. State the success target (for example, a given monthly revenue or margin by month 6).
2. Compute what that requires: customers × price × retention, or orders × contribution, minus costs and the user's time.
3. Convert into weekly activity: conversations, demos, leads, sends. Does the required effort fit in the team's actual hours?
4. Compare to reference-class conversion rates (cold outreach, trial-to-paid, lead-to-meeting). Is the required performance typical, optimistic, or heroic?
5. Report the **break-even conditions** ("this works if CAC stays under X and monthly churn stays under Y; today's evidence supports roughly A–B on each").

The result is often more useful than any forecast: it shows which two or three variables decide everything and how far the evidence is from the required values.

## 10. Checks by project type

- **B2B software or tool:** sales cycle length × burn; budget owner vs. user; pilot-to-paid conversion; integration burden; security/compliance gates; "nobody gets fired for buying the incumbent".
- **Consumer app or content:** retention curves, not downloads; monetization path (ads need huge scale; subscriptions need clear value); platform dependence; seasonality; churn of attention.
- **Marketplace / platform:** cold start on both sides, liquidity (what share of listings or requests get fulfilled), disintermediation (do the parties leave the platform after matching?), take rate sustainability.
- **AI-wrapper or API-based product:** margin sensitivity to model/API pricing and usage, the provider shipping your feature natively, how little of the value is yours, switching ease for customers, quality variance and liability for wrong outputs. Value must come from workflow, data, distribution, or trust, not the model call.
- **Hardware or physical product:** minimum order quantities, lead times, inventory cash, returns, certification, supplier concentration, unit cost at small volume vs. quoted cost at scale.
- **Local / physical business:** location economics, local competition, repeat rates, labor reliability, licensing, wastage, working capital, owner's time.
- **Services / agency / freelance:** pricing power, client concentration, repeat vs. one-off, capacity ceiling, whether the business can run without the founder.
- **Content / creator:** audience growth is slow and nonlinear; monetization lags audience by many months; algorithm and platform dependence; sponsorship volatility.
- **Internal project:** the "customer" is a stakeholder group; adoption is political; benefits are often unmeasured; sponsor changes are an existential risk; budget cycles gate timing.
- **Personal decision (quit, relocate, retrain):** runway in months of personal expenses; reversibility of the move; re-entry cost if it fails; opportunity cost; support network; what the downside looks like at month 6 and month 12.
- **Student or side-project team:** time is the scarcest resource, and it is seasonal (exams, placements, holidays); commitment asymmetry among teammates; ownership and decision rights agreed before money arrives; reputational and academic spillovers in both directions.

## 11. Arithmetic hygiene

- Show formulas and inputs; label which inputs are facts, user claims, or your assumptions.
- Run low / mid / high, and say which input drives the result most (sensitivity).
- Check units and periods (monthly vs. annual; per order vs. per customer).
- Never present derived numbers with more precision than the least certain input. Use code to compute ledgers and sensitivities when available.
- When two of the user's numbers cannot both be true (revenue vs. customer count × price; hours claimed vs. hours available), say so; the contradiction is the finding.
- **Count each resource once.** If a cost line pays for something (a hired cook, a contractor, a tool), do not also count founders' hours for it. Reconcile cash and hours together: every task is done either by paid help or by team hours, never both and never neither.
- **Re-derive headline numbers from the body.** After drafting, recompute every number in the bottom line from the tables below it. Mismatched ranges between summary and body are a common, credibility-destroying error.
- **When the range straddles the decision threshold, say so.** If break-even could be 20 or 160 units a day depending on two inputs, the finding is "this cannot be forecast from here". Name the one or two inputs that dominate (sensitivity) and make *measuring them* the first action, instead of narrowing the range by false precision.
