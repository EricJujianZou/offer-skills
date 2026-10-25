---
name: offer-guarantees
description: "Chooses and writes the guarantee for an offer by picking one of four kinds (unconditional, conditional, anti-guarantee, implied) and one of fourteen named guarantees, then checks the refund cost. Use when the user says \"add a guarantee\", \"should I offer a refund\", \"money back guarantee\", asks about refunds, wants to \"reverse the risk\", asks whether to make \"all sales final\", weighs \"rev share or performance pricing\", says \"pay me only if it works\", or when an offer is built and the buyer's main objection is that it might not work for them. Not for bonuses (offer-bonuses), scarcity (offer-scarcity), urgency (offer-urgency), naming the whole offer (offer-naming), building the core offer (offer-build) or choosing the market or price (offer-market)."
---

# Offer guarantees

## What this is

A guarantee is a promise of what the seller will do if the buyer does not get the result. Risk, meaning the buyer's fear that the product will not work for them, is treated as the largest single objection to a sale, and the guarantee moves that risk from buyer to seller. Guarantees come in four kinds: unconditional (a refund for any reason), conditional (a promise with terms the buyer must meet, often worth more than a refund), anti-guarantee (all sales are final, with a stated reason) and implied (performance pricing, where the seller is paid only when the result happens).

## When to use it, when not to

- Use it when the core offer exists and delivers, and buyers hesitate because they doubt it will work for them.
- Do not use it to cover a weak product or a weak sales process.
- Narrow it or skip it when the user cannot yet fulfil the promise reliably.
- Avoid an unconditional refund when delivery is expensive. A refunded buyer then costs the price and the delivery already spent.
- Avoid an implied guarantee when results cannot be measured openly or the user cannot collect payment once the result happens.
- Tie the guarantee to the actions that produce success. A loose guarantee draws buyers who buy for the guarantee and do no work.

Pick the kind from the user's situation:

| Situation | Kind |
|---|---|
| Low price, consumer buyer, low cost to fulfil | Unconditional |
| High price, business buyer, or high cost to fulfil | Conditional or anti-guarantee |
| The user knows the actions a buyer must take to succeed | Conditional, with those actions as the conditions |
| High margin, and buyers who do the actions almost always succeed | Conditional, outsized refund (2x, 3x or a fixed large payment) |
| Product is consumable, loses value once delivered, or is easy to copy once seen | Anti-guarantee with a true reason |
| High-price work that needs heavy effort or customization from the buyer | Anti-guarantee that screens for committed buyers |
| Outcome is measurable and the user can see the numbers and collect | Implied (performance, revenue share, profit share) |
| The user is new and afraid of refunds | Service guarantee or performance pricing first, since neither pays cash back. Loosen later to raise volume. |

The fourteen named guarantees, with the condition, risk and cost of each, are in `references/guarantee-catalogue.md`.

**Ethics.** The anti-guarantee reason must be true, so never invent one. Any guarantee must be one the user will honour as written, with a claim process a buyer can complete, and it must not contradict the refund rules of the payment platform or store.

## Procedure

1. **Find the fears.** Ask the user what the buyer is most afraid will happen after paying. List the costs the buyer takes on beyond the price: time, ad spend, travel, effort. Good output is two to four concrete fears in the buyer's terms.
2. **Find the success actions.** Ask which actions buyers who succeed take, for example installing and using it daily, attending the calls, sending 100 emails, or putting the page live. Good output is three or fewer actions a buyer can track. These become the conditions.
3. **Classify the situation.** Batch these into one message: price, consumer or business buyer, delivery cost per customer (low, medium or high), whether the outcome is measurable, and whether the product is easy to copy once seen. Use the table above to pick one or two kinds.
4. **Pick named guarantees.** Find candidates for the chosen kind in the objection and product type tables of `references/guarantee-catalogue.md` and read their entries. Choose two or three candidates and one recommendation.
5. **Run the refund math.** Expected cost per 100 sales = 100 × refund rate × (price + delivery cost already spent per refunded buyer). For delivery cost, use $0 for the low tier and the user's estimate in dollars for medium and high. For a subscription, use the yearly price. The guarantee pays off when the sales lift it causes exceeds the extra refunds. Break-even sales multiple = (1 − old refund rate) / (1 − new refund rate); use 0 for the old refund rate if no guarantee existed. When the user does not know the refund rate, assume 5 percent of buyers for an unconditional refund on a digital product and 10 percent for a service, and tell the user to replace it with real data after thirty sales. If the expected cost is more than the user can pay or the lift needed is implausible, narrow the guarantee or switch kind. A guarantee without a refund is costed as:
   - Pay only on result: the expected revenue not collected from buyers who miss the result.
   - Service until outcome: extra hours per buyer times the hourly cost of delivery.
   - Delayed second payment: the share of second payments expected not to arrive, times that payment.
6. **Consider stacking.** Two guarantees can sit together: an unconditional short-window refund plus a conditional larger promise, or two conditional promises on sequential milestones. See the catalogue's stacking section.
7. **Write it in X, Y, Z form.** "If you do not get X in Y time, we will Z." State the conditions in plain words. Z gives the guarantee its force. Give it a specific name, not "satisfaction guarantee".
8. **Write the claim process.** One action, one address, one response time.
9. **Write how to say it.** The seller states the guarantee plainly and with its reason, an anti-guarantee included, and does not apologise for it.

Next: run the offer-naming skill (it may be namespaced in some installs, for example offer-skills:offer-naming).

## Output

````
GUARANTEE
Kind: <unconditional | conditional | anti-guarantee | implied>
Named guarantee: <catalogue name, plus the user's own name for it>
Condition the buyer must meet: <the actions, or "none">
Wording:
```
<the exact guarantee copy the user pastes: name, X/Y/Z promise, conditions, how to claim>
```
Expected cost: <refund rate used and its source (user data or the 5%/10% default), cost per 100 sales, break-even sales multiple>
Candidates considered: <one line each for the other one or two, with kind and main risk>
Why this kind: <one sentence; when to move to a less restrictive one>
````

## Rules

- The core offer must deliver without the guarantee.
- Every guarantee states X (result), Y (time) and Z (what the seller does).
- Conditions are the actions that produce success, and there are few enough that a buyer can track them. Each condition added to an unconditional guarantee weakens it.
- The user can afford to honour every claim, and the claim is one step.
- The guarantee gets as much attention as the deliverables, not a line added at the end.

## References

- `references/guarantee-catalogue.md`: the fourteen named guarantees by buyer objection and product type, performance pricing minimums, stacking, the refund math example, naming, and examples.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
