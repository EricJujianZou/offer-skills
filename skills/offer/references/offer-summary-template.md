# Offer summary template

Fill this at the end of Build mode, and fill it from the page in Audit mode. Each slot takes one sibling block: map each field to the template line of the same name; extra fields go under the slot. A slot holds the block, or "none" with a one line reason, or (Audit mode only) "not stated". Dollar values are the stated value to the buyer, not the cost to deliver.

The slots follow the run order, so a slot is filled only after the one above it.

Fields a sibling returns beyond the required ones are kept below that block's slot, as `<further fields the sibling returned, if any>`; the template does not repeat that placeholder in each slot. Slot 4 repeats once per urgency type when offer-urgency chose more than one.

```
OFFER SUMMARY: <working title>            Date: <yyyy-mm-dd>

1. MARKET                                  (from offer-market)
   Niche:             <one line>
   Pain:              <pass/fail>: <one reason>
   Purchasing power:  <pass/fail>: <one reason>
   Easy to target:    <pass/fail>: <one reason>
   Growing:           <pass/fail/unverified>: <one reason>
   Price position:    premium, <number or range>
   Why the user can charge it: <one line>

2. CORE OFFER                              (from offer-build)
   Dream outcome:     <one line>
   | Item | What problem it solves | Delivery method | Cost tier | Stated value |
   |------|------------------------|-----------------|-----------|--------------|
   |      |                        |                 | low/medium/high | $      |
   Total stated value: $
   Proposed price:     $

3. SCARCITY                                (from offer-scarcity)
   Type:              <limited supply / limited bonuses / never available again / none>
   The limit and why it is real: <one line, or the reason for "none">
   Page copy:
   <fenced block with the exact page copy>
   Sales line:
   <fenced block with the exact line for sales calls or messages>
   Sold-out message (optional): <fenced block, if offer-scarcity returned one>

4. URGENCY (repeat per type)               (from offer-urgency)
   Type:              <rolling cohorts / rolling seasonal / pricing or bonus based / exploding opportunity / none>
   The deadline and why it is real: <one line, or the reason for "none">
   Copy:
   <fenced block with the exact copy>

5. BONUSES                                 (from offer-bonuses)
   | Name | Obstacle it removes | What it is | Proof | Stated value |
   |------|---------------------|------------|-------|--------------|
   |      |                     |            |       | $            |
   Total bonus value: $
   Total bonus value exceeds core offer stack value? <yes/no>

6. GUARANTEE                               (from offer-guarantees)
   Kind:              <unconditional / conditional / anti-guarantee / implied>
   Named guarantee:   <name>
   Condition the buyer must meet: <condition, or "none">
   Wording:
   <fenced block with the exact wording>
   Expected cost:     <refund rate or cost, and the basis for it>

7. NAME                                    (from offer-naming)
   Final name:        <name>
   MAGIC parts used:  <any of Magnet (the reason why), Avatar, Goal, Interval, Container>
   Alternates:        <alternate 1>; <alternate 2>

8. PRICE AND TERMS                         (assembled here from blocks 1, 2 and 5)
   Price:             $<amount>, <one time / monthly / other payment terms>
   Total stated value (core offer stack plus bonuses): $
   Value to price ratio: <x>   (for a subscription, divide by the price per year, 12 times the monthly price, unless the user says otherwise)
   Why a buyer cannot compare it with the cheapest alternative: <one line, taken from "Why the user can charge it" in slot 1>
```

## Slot to skill map

| Slot | Block | Skill that fills or fixes it |
|---|---|---|
| 1 | MARKET | offer-market |
| 2 | CORE OFFER | offer-build |
| 3 | SCARCITY | offer-scarcity |
| 4 | URGENCY | offer-urgency |
| 5 | BONUSES | offer-bonuses |
| 6 | GUARANTEE | offer-guarantees |
| 7 | NAME | offer-naming |
| 8 | (none) | assembled by offer; a fail here goes to offer-market for price and to offer-build for stated value |

A block produced from `references/fallbacks.md` keeps its slot and adds "(fallback)" after the block name.
