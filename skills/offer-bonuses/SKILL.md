---
name: offer-bonuses
description: "Designs the bonuses attached to an offer by splitting deliverables into named bonuses, writing each one up with the obstacle it removes, proof and a stated value, adding products from partner businesses, and deciding when each bonus is shown during a sale. Use when the user says \"add bonuses\", \"what can I throw in\", \"they said it's too expensive\", \"make the offer feel like more\", \"stack the offer\", \"what extras should I include\", \"partner with another business for perks\", \"affiliate deal with another tool\", or when a prospect has objected and the core price should stay fixed. Not for building the core offer stack (offer-build), choosing the market or the price (offer-market), scarcity or urgency on the whole offer (offer-scarcity, offer-urgency), guarantees (offer-guarantees) or naming (offer-naming)."
---

# Offer bonuses

## What this is

A bonus is a deliverable presented apart from the core offer, with its own name and its own stated value. Buyers value an offer more when it is broken into parts and shown one item at a time, so each bonus raises perceived value while the price stays tied to the core offer. Perceived value follows the value equation, which is dream outcome times perceived likelihood of achievement, divided by time delay times effort and sacrifice (see offer-build), and the growing gap between price and perceived value is the price-to-value gap (see offer-market).

## When to use it, when not to

- Use it when the core offer stack exists. Bonuses are drawn from that list and from the user's spare assets, so run the offer-build skill first if there is no list (it may be namespaced in some installs, for example offer-skills:offer-build).
- Use it when a prospect says the price is too high or asks for a discount. The core price is never cut, because a discount teaches buyers that prices are negotiable; a bonus raises value instead and keeps the seller in a position of strength.
- Use it when a prospect names a specific obstacle, such as no time or no idea how to set it up.
- Use it when the user owns assets that cost effort to make once and nothing to give again, or when buyers will next need something a non-competing business sells.
- Do not partner with a direct competitor, and do not turn an item the buyer must not skip into a bonus (see the wow test in step 2).
- Do not attach scarcity or urgency to a bonus unless the limit or deadline is real. Invented limits cost trust.
- The tactic backfires when bonuses are piled on with no link to an objection. The buyer reads a long list of unrelated extras as filler and the price starts to look inflated.

## Procedure

1. **Collect the core offer and the user's assets.** Ask for the core offer stack (items, stated values, total, price) and, in the same message, a list of assets the user already owns: recordings, templates, documents, past workshops. Produce one flat list that names each item concretely ("onboarding checklist PDF", not "support materials").

2. **Split core from bonus with the wow test.** Mark an item as a bonus when it is distinct, short, high in value and could almost be sold on its own, such as a checklist, a launch map or a template pack. Everything the buyer must not skip stays in the core.

3. **Map bonuses to obstacles and next problems.** Ask for the reasons prospects give for not buying and what buyers need right after the core offer works. Tie each bonus to one obstacle or one next problem. Drop any bonus that maps to neither.

4. **Turn training into tools.** Convert each training bonus into a checklist, template, script, calculator or swipe file where possible, because a tool takes less of the buyer's time and effort.

5. **Write up each bonus against the eleven bonus rules.**
   1. Every offer gets bonuses. The source is the list of deliverables from the core offer stack.
   2. Each bonus gets its own name, and the name states a benefit.
   3. The write-up tells the buyer four things: (a) how the bonus connects to their problem, (b) what it is, (c) how the seller found it or what it took to make, and (d) how it makes the result faster, easier or less work.
   4. The write-up shows proof that the bonus is valuable: a number, a past customer or the seller's own experience.
   5. The write-up describes the buyer's life after the bonus is already working for them.
   6. Each bonus carries a stated value, and the write-up says why it is worth that.
   7. Tools and checklists beat more training, since they cost the buyer less time and effort.
   8. A bonus can target one specific doubt the prospect has about why they will fail, and show that doubt is wrong.
   9. A bonus can solve the problem the buyer will meet next, before they meet it.
   10. The bonuses together are worth more than the core offer.
   11. A bonus can carry its own scarcity (limited in number, or only available through this offer) or urgency (lost after a deadline). Script patterns are in references/scripts-and-examples.md.

6. **State a value for every bonus and total them.** Justify each value by what the item would cost to buy elsewhere, what it cost to make, or what it saves the buyer. If the user has no figure, use the market price of the closest paid equivalent (an hour of setup help, a template sold on a marketplace). Check that total bonus value exceeds the core offer stack value.

7. **Add partner products (optional).** Ask what buyers will want next from another business. For each non-competing business that sells it, the user can ask for free units as a bonus in exchange for exposure, negotiate a group discount that individual buyers could not get alone, and negotiate a referral commission per customer sent. Record the buyer's value and the user's commission (worked example in references/partner-examples.md).

8. **Set the order of presentation.** In a one-on-one sale, the seller asks first; a yes hears the bonuses after signup, and a no hears the one bonus that answers the objection, then a second ask ending with "fair enough?" (full sequence in references/scripts-and-examples.md). On a written page, the core offer and price come first and bonuses follow one at a time in rising value.

9. **List vault assets to build.** Give the user a short list of reusable assets to make over time so later offers have bonuses ready. The asset types are in references/scripts-and-examples.md.

10. **Next.** Run the offer-guarantees skill (it may be namespaced in some installs, for example offer-skills:offer-guarantees).

## Output

```
BONUSES
| Name | Obstacle it removes | What it is | Proof | Stated value |
|------|---------------------|------------|-------|--------------|
| ...  | ...                 | ...        | ...   | $...         |

Moved from core: <items, or "none">
Total bonus value: $...
Core offer stack value: $... (after the moved items are removed)
Check: total bonus value exceeds core offer stack value: yes / no (if no, what to add)
```

After the block, give each bonus's page copy (rules 2 to 6) in one fenced code block, the one-on-one order of bonuses matched to objections, and the partner table if step 7 was used.

## Rules

- The core price never changes to close a deal.
- No bonus is mentioned before the first ask in a one-on-one sale.
- Bonus copy that uses scarcity or urgency says which one it is.
- The offer is never shown as one block, which hides deliverables.

## References

- references/scripts-and-examples.md: a table of situations, the presentation sequence, the wow test, bonus scarcity and urgency scripts, vault assets and our own examples.
- references/partner-examples.md: partner and commission tables and a group discount deal.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
