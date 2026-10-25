---
name: offer
description: "Builds a complete offer, or audits an existing one, with the method from the book \"$100M Offers\", by running the sibling offer skills in a fixed order and assembling their results into one offer summary. Use when the user says \"make an offer for this\", \"build me an offer\", \"is this offer good\", \"review my pricing page\", \"audit my landing page\", \"why isn't anyone buying\", \"nobody is buying\", \"nobody is converting\", \"100M offers\", \"Hormozi\" or \"grand slam offer\", when the user pastes a landing page, pricing page or sales pitch and asks what is wrong with it, or when the user wants more than one part of an offer done at once. Not for a single part on its own: market and price (offer-market), offer contents (offer-build), scarcity (offer-scarcity), urgency (offer-urgency), bonuses (offer-bonuses), guarantee (offer-guarantees) or name (offer-naming)."
---

# Offer

## What this is

An offer is what a business delivers, how it takes payment and the terms of the deal. The book "$100M Offers" calls it a grand slam offer when buyers cannot compare it with any alternative and weigh it against doing nothing. Build mode runs seven sibling skills in order and assembles one summary. Audit mode tests an existing offer and routes each failure to the sibling that fixes it.

## When to use it, when not to

- Use Build mode when the user has a product or idea but no defined offer, price or sales page, or asks for more than one part of an offer.
- Use Audit mode when the user supplies a sales page, script, store listing or pitch, or asks why sales are low.
- For one part only, run that sibling directly.
- Do not use it for a traffic problem. Under about 300 visitors is too little data to judge conversion (a rule of thumb, not from the book), so say that before auditing.
- The method backfires when enhancers wrap a core offer that does not solve the buyer's problems, or in a market that fails the four market tests.

## Procedure

### Build mode

1. **Take the intake.** Ask in one message for: what the user can deliver, who buys it, any current price, weekly capacity, proof (results, user counts, testimonials), and the sales calendar (cohort starts, seasonal peaks, launches, price changes). Good looks like one confirmed paragraph. If capacity is unknown, estimate it: weekly hours available divided by hours per customer.
2. **Run the offer-market skill** (it may be namespaced in some installs, for example offer-skills:offer-market) with the intake. Wait for the `MARKET` block: niche, four market tests, price position and why the user can charge it. If the growing test cannot be checked because no web tool is available, it is rated "unverified" and noted in the summary. Only a confirmed fail stops the run: say which test and why, and ask whether to switch niche or accept the risk.
3. **Run the offer-build skill** (it may be namespaced in some installs, for example offer-skills:offer-build) with the `MARKET` block. Wait for the `CORE OFFER` block: dream outcome, the core offer stack table, total stated value and a proposed price. Good looks like a total stated value several times the proposed price. For a subscription, compare against 12 times the monthly price.
4. **Run the offer-scarcity skill** (it may be namespaced in some installs, for example offer-skills:offer-scarcity) with `MARKET`, `CORE OFFER` and the capacity from step 1. Wait for the `SCARCITY` block. A limit on a bonus is marked "to be set after offer-bonuses".
5. **Run the offer-urgency skill** (it may be namespaced in some installs, for example offer-skills:offer-urgency) with the blocks so far and the sales calendar from step 1. Wait for one `URGENCY` block per type chosen. A deadline on a bonus is marked "to be set after offer-bonuses".
6. **Run the offer-bonuses skill** (it may be namespaced in some installs, for example offer-skills:offer-bonuses) with the blocks so far. Wait for the `BONUSES` block. Remove the items offer-bonuses moved out of the core offer stack from slot 2 and recompute its total before the bonus-exceeds-core check. If `SCARCITY` chose "limited bonuses", or `SCARCITY` or `URGENCY` has a part marked "to be set after offer-bonuses", run offer-scarcity and offer-urgency again with `BONUSES`; their new blocks replace slots 3 and 4.
7. **Run the offer-guarantees skill** (it may be namespaced in some installs, for example offer-skills:offer-guarantees) with the blocks so far. Wait for the `GUARANTEE` block.
8. **Run the offer-naming skill** (it may be namespaced in some installs, for example offer-skills:offer-naming) with the blocks so far. Wait for the `NAME` block. If offer-naming renamed stack items or bonuses, apply the new names in slots 2 and 5 and carry renamed bonuses into the slot 3 and slot 4 copy.
9. **Fill the summary.** Map each block's fields to the template lines of the same name in `references/offer-summary-template.md`, with extra fields under the slot, then fill price and terms. A block of "none" keeps its stated reason.
10. **Audit the result.** Run `references/audit-checklist.md` on the summary. Send each fail back to the sibling skill named on that test (it may be namespaced in some installs, for example offer-skills:offer-build), then update the slot.

A missing sibling is replaced by its paragraph in `references/fallbacks.md`, and its block is marked "(fallback)".

### Audit mode

1. **Collect the offer.** Get the page text, URL or script and read all of it. For a URL with no fetch tool available, ask the user to paste the page text. Fill the summary template from what the page states, writing "not stated" in any field the page leaves out.
2. **Ask what the page cannot show.** In one message, ask at most five questions, usually the market test facts, the real capacity behind any scarcity claim, and whether stated deadlines happen.
3. **Run every test.** Use `references/audit-checklist.md`. Each test is pass or fail with one line of evidence quoted from the page or from the user's answer, or "not checked" when neither answers it. No scores.
4. **Order the fixes.** Market fails come first, then core offer, then the enhancers in run order, then whole-offer tests.
5. **Route each fail.** Name the sibling skill to run (it may be namespaced in some installs, for example offer-skills:offer-build) and the one input it will need from the user.

## Output

Build mode hands back:

```
MODE: build
<the filled template from references/offer-summary-template.md>

DECISIONS
- <sibling>: <what it decided, and why in one line>   (one line per sibling, in run order)

OPEN QUESTIONS
- <anything that blocks launch, or "none">
```

Audit mode hands back:

```
MODE: audit
| Section | Test | Pass or fail | Evidence | Sibling to run |
|---|---|---|---|---|
| <A to H> | <test id and name> | <pass/fail/not checked/not applicable> | <quote or user answer> | <skill> |

TOP THREE FIXES
1. <test id>: run <sibling>; it needs <one input from the user>
2. <...>
3. <...>

OFFER AS STATED
<the template filled from the page, "not stated" where the page is silent>
```

## Rules

- Accept a sibling block only when every field is filled or the block is "none" with a reason.
- Every scarcity and urgency claim must be true and in the user's power to honour; a countdown that resets fails.
- Never price to undercut competitors.
- The headline sells the buyer's result, not the product that delivers it.
- Run the enhancers only after the core offer exists, and leave some demand unmet for the next round (`references/enhancers.md`).
- Copy the user will paste goes in a fenced code block and uses no em or en dashes.

## References

- `references/offer-summary-template.md`: the summary, one slot per block.
- `references/audit-checklist.md`: the Audit mode tests.
- `references/fallbacks.md`: minimum versions of each sibling.
- `references/enhancers.md`: why enhancers follow the core offer.
- `references/book-examples.md`: the book's definition, cases and recap, and our examples.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
