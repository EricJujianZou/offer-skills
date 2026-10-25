# Fallbacks for missing sibling skills

Use a paragraph below when the sibling skill it names is not installed (check both the plain name and a namespaced name such as offer-skills:offer-market). Each fallback produces the same block with the same fields, marked "(fallback)", so the Build procedure and the summary template still complete. A fallback is the minimum version of the step. Tell the user once which steps ran as fallbacks and that installing the sibling gives a fuller result.

## offer-market

Ask the user for one specific buyer group and write it as a one line niche. Rate the four market tests pass or fail with one reason each: pain (the buyer urgently needs the problem solved), purchasing power (the buyer has or can get the money), easy to target (the user can name where these buyers gather), and growing (searches for or spending on the category rose over the last three years, judged from Google Trends, marketplace listing counts, job postings or the user's inbound; unknown is fail). Set the price position as premium: list the two or three closest alternatives with their prices and propose a price at or above the highest one, then give one line on why the user can charge it. Return the `MARKET` block.

## offer-build

Write the dream outcome as one line in the buyer's words, naming the result and not the product. List every obstacle the buyer meets before, during and after using the product. Give each obstacle one named deliverable, its delivery method, and a cost tier (low: automated or one-time asset; medium: group or batch effort; high: one to one time or money per customer). Drop items that are high cost and low value to the buyer. Give each remaining item a stated value based on what the buyer would pay for it alone, total the values, and propose a price well below the total. For a subscription, compare the total with the price per year (12 times the monthly price) unless the user says otherwise. Return the `CORE OFFER` block with the core offer stack table.

## offer-scarcity

Ask the user what actually limits supply: hours, seats, units or bonuses. If a real limit exists, pick one type (limited supply, limited bonuses, never available again), state the number and why it is real on one line, and write two fenced blocks: page copy that states the limit and the reason, and a one-line sales line for calls or messages. If no real limit exists, return "none" with that reason; never invent a limit. Return the `SCARCITY` block.

## offer-urgency

Ask the user for real dates: cohort starts, seasonal peaks, planned price increases, or a bonus that ends. Pick one type (rolling cohorts, rolling seasonal, pricing or bonus based, exploding opportunity), state the deadline and why it is real on one line, and write one or two lines of copy in a fenced block. If no real date exists, return "none" with that reason; never invent a deadline. Return the `URGENCY` block.

## offer-bonuses

Take the core offer stack and move out any item that is distinct, short, high value and could almost sell on its own; keep in the core every item the buyer must not skip. Add a checklist, template or tool for each remaining buyer objection. Give each bonus a name that states a benefit, the obstacle it removes, what it is, one line of proof, and a stated value. Total the bonus values and check that the total exceeds the core offer stack value; if it does not, add or re-value bonuses until it does or say why it cannot. Remove the moved items from the core offer stack and update the CORE OFFER total. Return the `BONUSES` block.

## offer-guarantees

Ask what the buyer fears most will go wrong. Pick one kind (unconditional, conditional, anti-guarantee, implied). Use conditional when the result depends on the buyer doing work, and name the actions the buyer must complete. Pick one named guarantee for the block from these five, which use the names in the offer-guarantees catalogue:

- No Questions Asked Refund [unconditional]: full money back within a stated number of days, no questions asked.
- Outsized Refund [conditional]: the price back, or a multiple of it, if the buyer completes the named actions and still does not get the stated result.
- Implied (performance or revenue share) [implied]: the buyer pays nothing, or pays a share of the gain, until the stated result happens.
- Service [conditional]: the seller keeps working at no extra charge until the buyer reaches the stated result.
- All Sales Are Final [anti-guarantee]: no refunds, with the stated reason (for example, the buyer gets immediate access to everything, or the seller reserves limited capacity for each buyer).

Write the exact wording in a fenced block, naming what the buyer gets back and by when. Estimate the cost by the guarantee chosen, and tell the user to replace each estimate with real figures after the first thirty sales:

- No Questions Asked Refund: a refund rate of 5 percent of buyers on a digital product or 10 percent on a service, times the price.
- Outsized Refund: the expected share of buyers who meet the conditions and still fail, times the payout.
- Implied (performance or revenue share): the expected revenue not collected, which is the share of buyers expected to miss the result times the price.
- Service: the extra hours per buyer who misses the result, times the user's cost per hour, times the share of buyers expected to need them.
- All Sales Are Final: no refund cost; note the sales lost to buyers who want reassurance.

For a subscription, use the price per year (12 times the monthly price) in these figures unless the user says otherwise. Return the `GUARANTEE` block.

## offer-naming

Write five candidate names, each with at least three of the MAGIC parts: Magnet (the reason why, such as a season or launch), Avatar (the buyer group), Goal (the dream outcome), Interval (a time frame), Container (a word such as program, kit, challenge or system). Pick the one that names the buyer and the result most plainly, record which parts it uses, and keep two others as alternates. Return the `NAME` block.
