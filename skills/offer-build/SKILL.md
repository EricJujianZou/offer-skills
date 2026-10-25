---
name: offer-build
description: "Builds the core of an offer (what a product or service delivers to the buyer) with the book's five steps, expanded to nine, from \"$100M Offers\" and scores each part against the value equation (dream outcome times likelihood of achievement, divided by time delay times effort and sacrifice). Use when the user says \"what should my offer be\", \"make this offer better\", \"why would anyone pay for this\", \"how do I compete with free\", \"what should I include\", \"list the problems my users have\" or \"what can I deliver at scale\", or wants to design or strengthen what a product delivers, or asks why one product is worth more than another with the same promise. Not for choosing a market or price (offer-market), the whole offer at once (offer), or scarcity, urgency, bonuses, guarantees or naming (offer-scarcity, offer-urgency, offer-bonuses, offer-guarantees, offer-naming)."
---

# Offer build

## What this is

This skill produces the core offer stack: the trimmed and stacked list of deliverables, each with a stated value, and a total far above the price. It scores every deliverable against the value equation: the dream outcome (the result the buyer wants) times the perceived likelihood of achievement, divided by the perceived time delay times the perceived effort and sacrifice. Read the full explanation in `references/value-equation.md` before step 2.

## When to use it, when not to

Use it when any of these is true:

- Prospects compare the product on price with a cheaper or free alternative.
- Prospects refuse even a free trial because they doubt they will keep going.
- The user describes the vehicle ("a membership", "an extension", "a course") instead of the result the buyer wants.
- Lost sales trace back to one unsolved objection, such as "but I eat out every day".
- The user asks why a rival offer with the same promise sells for more.

Do not use it, or adjust it, when:

- Choosing the buyer or the price belongs to the offer-market skill (it may be namespaced in some installs, for example offer-skills:offer-market).
- Scarcity, urgency, bonuses, a guarantee or a name for a finished core offer belong to the enhancer skills listed in step 9.
- The method backfires when stated values are inflated past what the buyer would believe, or the price exceeds what the product is worth.
- The method backfires when the offer is trimmed before anyone is buying. The first version over-delivers, and cutbacks come once demand exists.

## Procedure

1. **Collect the inputs.** Ask for the product, the buyer and the `MARKET` block if offer-market has run. Without a `MARKET` block, take a one-line niche from the user (who buys and what they get today) and continue.

2. **Write the dream outcome.** Ask what the buyer wants to have or experience once they arrive, and how fast. Write it as a result plus a time frame, for example "Lose 20lbs in 6 weeks". It names the destination, not the vehicle. Good looks like one concrete sentence with a shorter time frame than the buyer expects.

3. **List every problem.** Ask the user to walk through what the buyer does, in order, including the step before and after using the product. No idea is judged until step 6. For each activity, list why the buyer would fail to start or continue, using one prompt per driver: not worth the money; will not work for me or I will not stick with it; too hard or unpleasant; takes too long or does not fit my schedule. Good looks like dozens of problems; the cohort course in `references/worked-example.md` reaches about 40.

4. **Turn each problem into a solution.** For each problem, ask what the buyer would need to be shown to solve it, then write the answer as a "how to" line ("Healthy food is expensive" becomes "How to buy healthy food for less than the current grocery bill"). Every problem gets a solution, because one unanswered problem can be the reason a buyer says no. Repeated solutions are normal.

5. **List delivery options.** For each solution, list every way it could be delivered, including ways the user would never choose, by varying the six delivery variables in `references/delivery-options.md`. Good looks like several options per solution across at least two levels of attention (one-to-one, small group, one-to-many).

6. **Rate cost and trim.** Rate each option on a three-tier cost scale instead of asking the user for dollar figures:
   - low: automated, or a one-time asset such as a template, calculator, recording or software feature
   - medium: group or batch effort, such as a weekly group call or a monthly batch review
   - high: one-to-one time or money spent per customer

   Rate value to the buyer as high or low against the four drivers. Cut low value options, high cost ones first. Step a high cost, high value option back one version at a time (one-to-one, small group, recorded) until its cost is acceptable, or raise the price to cover it. Good looks like at least one low-tier one-to-many asset and an early win the buyer gets within days of purchase.

7. **Stack and value.** Group the surviving options under each problem and give each group a plain name and a one-line benefit. Give each group a stated value from what it saves or earns the buyer: money saved, hours saved times what the buyer's hour is worth, or the price of the nearest standalone alternative. Keep in the core everything the buyer must not skip. Items that pass the wow test in the offer-bonuses skill may move to bonuses later. Sum the stated values.

8. **Propose a price.** Use the price from the `MARKET` block when there is one. Otherwise propose a price at or below one fifth of the total stated value (the gym example: $4,351 of stated value sold for $599) that still covers the high-tier items with a wide margin. For a subscription, compare yearly figures. Then run the offer-market skill (it may be namespaced in some installs, for example offer-skills:offer-market) to confirm it; skip this when run inside offer.

9. **Hand off.** Return the Output block, then run the offer-scarcity, offer-urgency, offer-bonuses, offer-guarantees and offer-naming skills in order (each may be namespaced in some installs, for example offer-skills:offer-scarcity). Skip this when run inside offer.

## Output

```
CORE OFFER
Dream outcome: <result plus time frame, one line>

Core offer stack:
| Item | What problem it solves | Delivery method | Cost tier | Stated value |
|------|------------------------|-----------------|-----------|--------------|
| <name> | <problem from step 3> | <one-to-one / small group / one-to-many, and, for live delivery, the channel> | <low / medium / high> | $<amount> |
| ... | ... | ... | ... | ... |

Total stated value: $<sum>
Proposed price: $<price> (<from MARKET block / estimate; run the offer-market skill to confirm it>)

Fast win: <what the buyer gets within days of purchase>
Problems left unsolved: <list, or none>
```

## Rules

- Lower time delay and effort before making bigger claims, because that usually raises value more than a larger promise.
- Prefer a cheap change in how something feels to the buyer over an expensive logical fix.
- An improvement the buyer cannot see adds no value until the offer states it.
- Do not force the buyer to solve a problem the user's preferred way. Offer a route that fits the buyer's actual habit.
- The total stated value exceeds the price by a wide margin, and the price exceeds delivery cost by a wide margin.

## References

- `references/value-equation.md`: the full value equation, rules per driver, and comparisons of offers with the same dream outcome.
- `references/delivery-options.md`: the six delivery variables, cost tiers, trim rules, and examples for small software and service products.
- `references/worked-example.md`: the book's gym offer in summary ($4,351 of stated value sold for $599) and a cohort course worked through steps 2 to 7.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
