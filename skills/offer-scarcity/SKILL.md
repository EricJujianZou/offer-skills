---
name: offer-scarcity
description: "Adds an honest quantity limit to an offer (seats, client spots, units or bonuses) so buyers act before the supply runs out, using the three scarcity types from chapter 12 of \"$100M Offers\". Use when the user says \"should I cap this\", \"how many spots should I open\", \"limited drop\", \"only take X clients\", \"cap the cohort\", \"waitlist for the paid tier\", \"should I say it's limited\", or when an offer has a real capacity limit that buyers do not know about yet. Not for deadlines, cohort start dates or price increases (offer-urgency), designing the bonuses themselves (offer-bonuses), risk reversal (offer-guarantees), building the core offer (offer-build), choosing the market or price (offer-market), or naming the offer (offer-naming)."
---

# Offer scarcity

## What this is

Scarcity is a publicly stated limit on how many units, seats, client spots or bonuses exist, for example "100 boxes this month" or "5 new clients per week". It raises the price a buyer will accept and makes the buyer decide sooner, because the buyer fears losing access that other people get. Scarcity limits quantity; a limit on time belongs to offer-urgency. The supply and demand reasoning behind both (chapter 11 of the book) is explained once in the offer skill.

The book names three scarcity types, used here exactly:

- **limited supply**: a cap on seats, slots, client spots or units, either in total or per period.
- **limited bonuses**: a cap on how many buyers receive a particular bonus.
- **never available again**: an item, edition or term that will not be made or offered again once it is gone.

## When to use it, when not to

Use it when at least one of these holds:

- The service has a real capacity limit, as coaching, freelance work, workshops and one-to-one access do.
- The seller can produce a fixed batch of a physical or digital item and will stop at that number.
- The offer is a higher-priced upsell or a one-off workshop or consulting block.
- A free lead magnet (a free download used to collect contact details) gets too little interest (the weekly download cap in references/examples.md).

Do not use it, or switch to another form, when any of these holds:

- The limit would be invented and the seller would still take buyers past it. A broken cap removes the effect for every later release.
- The product is software with no delivery limit and the proposed cap is on licences. A cap on setup calls or a founding batch with terms that never return is honest.
- The batch is far above current demand, so it will not sell out. A visible failure to sell out removes the scarcity.
- The seller needs mass market reach for a strategic reason.
- The real constraint is a date. Run the offer-urgency skill (it may be namespaced in some installs, for example offer-skills:offer-urgency).

## Procedure

1. **Find the real limit.** Ask the user how many clients, orders or seats they can serve per week, per month and in total without quality dropping, or how many units of an edition they can reliably sell. Produce one number per period that the user would defend if a buyer asked why. If the user does not know, estimate it as the hours available per week divided by the hours one client takes per week, then subtract 20 percent for slack.

2. **Pick the scarcity type.** Choose one of the three types above and confirm its condition.
   - limited supply for a service takes one of three caps: a total business cap (X clients at this level, ongoing, with a waiting list), a growth rate cap (X new clients per week, which needs a known onboarding capacity) or a cohort cap (X people per group that starts together). Cohort start dates go to offer-urgency.
   - limited supply for a product takes a limited release: a fixed batch, about once a month.
   - limited bonuses needs a bonus that is worth something on its own. Design the bonus with the offer-bonuses skill (it may be namespaced in some installs, for example offer-skills:offer-bonuses) and attach the quantity here. When this skill runs inside the offer skill before offer-bonuses has run, do not call offer-bonuses; mark the bonus "to be set after offer-bonuses". This form is a bonus cap: only the first X buyers get the bonus, for example "the first 20 buyers also get the setup call".
   - never available again needs a commitment the user will keep never to remake or reopen the item. For software, this is usually a founding batch: a fixed number of early buyers whose price or terms will not be offered again.

3. **Set the number below demand.** Ask how many people are likely to buy at the planned price. If the user cannot say, use last release's sales, waiting list size or inbound inquiries; with no history, set the cap at half the number of warm leads (people who asked about it or joined a list). Set the cap below expected demand so it sells out with buyers left over.

4. **Write the page copy and the sales line.** Draft the exact sentence the buyer sees on the page (page copy) and the line the seller says on a sales call (sales line). State the cap and, when true, how full it is ("3 of 5 spots taken this week").

5. **Write the sold-out message and waiting list line.** Always draft the sell-out announcement and the signup that puts missed buyers first in line next time.

6. **Plan the next release.** Record how much capacity grows next time (10 to 20 percent for a total business cap) while leaving some demand unmet. For the date of the next opening, run the offer-urgency skill (it may be namespaced in some installs, for example offer-skills:offer-urgency).

7. **Optional: a very small one-to-one tier.** For a seller with an audience, add the one-to-one access tier from references/examples.md, only if the user will deliver it.

## Output

Return this block. Copy the user will paste goes in fenced blocks.

````
SCARCITY
Type: <limited supply | limited bonuses | never available again | none>
Form: <total business cap | growth rate cap | cohort cap | workshop or event seats | weekly download cap | one-to-one access tier | members who leave cannot return | limited release | founding batch | bonus cap | never available again | fill level statement>
The limit and why it is real: <number per period>; <capacity or batch fact that sets the number>
Expected demand: <number and how it was estimated>
Next release: <capacity increase; date handed to offer-urgency>

Page copy:
```
<sentence the buyer sees on the page>
```

Sales line:
```
<line the seller says on a call, or "not used on calls">
```

Sold-out message (extra field, includes the waiting list line):
```
<message>
```

If none: <reason no honest limit exists>
Next: run the offer-urgency skill (it may be namespaced in some installs, for example offer-skills:offer-urgency).
````

## Rules

- The cap is a number the user can actually serve or produce, and the user will not sell past it.
- No copy claims a limit, fill level or sell-out that is not true. Return "none" with the reason rather than invent one.
- "never available again" and "members who leave cannot return" are used only when the user will keep the promise, and the second only for small groups.
- The cap appears where the buying decision happens (checkout page, sales call, cohort page) with a recently updated count.

## References

- `references/examples.md`: a table of caps for services, products and software, picked by the user's situation, with page copy and sales lines for each, and examples for small software and service products.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
