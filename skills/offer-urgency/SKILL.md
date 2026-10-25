---
name: offer-urgency
description: "Adds an honest deadline to an offer with one of four urgency types (rolling cohorts, rolling seasonal, pricing or bonus based, exploding opportunity) and writes the deadline copy and sales scripts for it. Use when the user says \"add urgency\", \"give people a reason to buy now\", \"they'll think about it\", \"should I put a countdown on the page\", \"run a launch or promo\", \"when should the next cohort start\", \"I'm raising my price\" or \"how do I close fence sitters\", or is planning start dates, promotion windows or a price change. Not for limits on how many people can buy (offer-scarcity), designing bonuses (offer-bonuses), guarantees (offer-guarantees), naming a promotion (offer-naming), building the core offer (offer-build) or choosing a market and price (offer-market)."
---

# Offer urgency

## What this is

Urgency is a real deadline on a purchase. It limits when a buyer can get the offer; scarcity, which limits how many can get it, belongs to the offer-scarcity skill. This skill picks the urgency types the user can enforce and writes the deadline copy and close scripts.

1. **Rolling cohorts**: new customers start together on a fixed, repeating date, in groups of any size.
2. **Rolling seasonal**: the same core offer runs as a dated promotion with a new seasonal name and end date each period.
3. **Pricing or bonus based**: a discount, price level or bonus expires on a date, and the core product stays for sale.
4. **Exploding opportunity**: the opportunity the buyer is acting on loses value over time by its own nature.

## When to use it, when not to

- Use it when buyers agree the offer fits them but put off the decision. In a week-long launch, up to 50 to 60 percent of sales arrive in the last 4 hours, because most buyers act only when a deadline is close. Without a deadline, many of them never act at all.
- Use rolling cohorts when the business can start customers in groups on a cadence. Skip it for instant-access products where a start date means nothing to the buyer.
- Use rolling seasonal when the promotion really ends on its date and the next one gets a new name. Recommend it first for a local business, because a new dated promotion on the same service adds novelty as well as a deadline.
- Use pricing or bonus based when the business sells year round with no natural start date, or a price raise is planned.
- Use exploding opportunity only when the opportunity decays: a market gap that will close, a channel before competitors arrive, terms that get worse each day.
- Do not use any type when the deadline will not be enforced. A countdown that resets costs the seller credibility.
- Do not attach the deadline to the core service when the business will keep selling it afterward. A roofer who says he will not serve late buyers is lying; he can say the promotion ends.

## Procedure

1. **Ask how the product is sold and delivered.** In one message, ask: do customers start at a set time or anytime, does the business sell year round, is a price change planned, does the opportunity itself get worse with time, and is there a seasonal or calendar moment the product ties to. Treat an unknown price change as not planned.

2. **Pick the type or types the facts support.** Test each type against the conditions in "When to use it, when not to". Types can be combined. Name each rejected type and the condition it failed.

3. **Rolling cohorts.** Ask what start cadence the user can run. Default to every other week if the user has no preference; fewer start dates give more urgency, and twice a year is the strongest the method describes. Write the close line: sign today and start with the group on the next date, or wait for the kickoff after it. Use the variant about a client who dropped out only if that happened. Write the reply for a buyer who arrives just after a start, using one of the two options in the references (the preferred one is waiting for the next group with a longer payment plan). Good output names a real date, a cadence and the late-arrival reply.

4. **Rolling seasonal.** Keep the core promotion the same and give each period a seasonal name and a hard end date, shown on the landing page and in every email and ad. When the period ends, swap in the next name and dates. Use real calendar dates. Hand the promotion name to the offer-naming skill (it may be namespaced in some installs, for example offer-skills:offer-naming) if the user wants help with it.

5. **Pricing or bonus based.** Choose what expires: a discount, a price level or a bonus. Hand bonus design to the offer-bonuses skill (it may be namespaced in some installs, for example offer-skills:offer-bonuses). When this skill runs inside the offer skill before offer-bonuses has run, do not call offer-bonuses; mark the expiring bonus "to be set after offer-bonuses" and give only its expiry date. Write the close so the buyer risks missing the promotion, never the service. If a price raise is planned, write an announcement that goes to everyone in the pipeline before the new price takes effect, with the date and both prices.

6. **Exploding opportunity.** State in one sentence why the opportunity shrinks with time. Write copy that names the decay and the cost of each week of delay.

7. **Answer the fear of lost sales** if the user raises it. Give the last-4-hours figure and the point that buyers who miss a real deadline mostly would not have bought without one.

8. **Return the URGENCY block.** Next, run the offer-bonuses skill (it may be namespaced in some installs, for example offer-skills:offer-bonuses).

## Output

Return one block per chosen type. If no type fits, return the block with type "none" and the reason.

````
URGENCY
Type: <rolling cohorts | rolling seasonal | pricing or bonus based | exploding opportunity | none>
The deadline and why it is real: <date or cadence>; <what happens on that date and how it is enforced>
After the deadline the buyer misses: <start date, price, bonus or opportunity>
Copy:
```
<close script>
<landing page or email deadline line>
<for cohorts: reply for a buyer who arrives just after a start>
<for a price raise: pipeline announcement>
```
Rejected types: <type: condition that failed>
````

Copy the user will paste goes in the fenced block, never in a blockquote.

## Rules

- Every deadline is a real date that will be enforced, and nothing resets it.
- A "client dropped out" or "best promotion in a while" line appears only if it is true.
- A planned price raise is announced to the pipeline before it happens. Raising a price without notice wastes the buyers who were waiting.
- One undated campaign running for months gets replaced by dated promotions.
- Quantity limits go to the offer-scarcity skill (it may be namespaced in some installs, for example offer-skills:offer-scarcity) and stay out of this output.

## References

- `references/scripts-and-examples.md`: a table keyed on the user's situation, close scripts, the price raise announcement, a seasonal promotion sequence, decaying opportunity examples, the launch sales figure, and examples for small software and service products.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
