---
name: offer-naming
description: "Names an offer, promotion, bonus or product with the MAGIC formula from chapter 16 of \"$100M Offers\" (a name built from three to five parts: Magnet (the reason why), Avatar, Goal, Interval, Container) and plans renames when an offer stops drawing a response. Use when the user says \"name this offer\", \"what should I call this\", \"headline for this promo\", \"name the bonuses\", \"this offer has stopped working\", \"ads are fatigued\", \"refresh this offer\", or asks for a title for a store listing or a waitlist page, or when a finished offer has no name or a generic one such as \"Pro plan\". Not for building the offer itself (offer-build), choosing the market or price (offer-market), designing bonuses (offer-bonuses), guarantees (offer-guarantees), or scarcity and urgency (offer-scarcity, offer-urgency)."
---

# Offer naming

## What this is

Chapter 16 of "$100M Offers" argues that the same offer draws a larger response when its name tells the right buyer why the offer exists, that it is for them, what they get and how fast. The MAGIC formula builds a name from three to five parts: Magnet (the reason why), Avatar (the specific buyer), Goal (the dream outcome), Interval (how long it takes) and Container (a word marking the offer as a bundle or system). It also covers renaming a fatigued offer, one the audience has seen so often that response has dropped, while the deliverables and price stay the same.

## When to use it, when not to

Use it when:
- An offer exists (a defined deliverable and price) and needs a name, headline, store listing title or promotion title.
- Items in a core offer stack or bonus list have plain names such as "Template pack".
- An offer that used to convert has run to the same audience for a long time, and response stayed low after the ad images, videos and body copy were changed.

Do not use it, or hold back, when:
- No offer exists yet. A name does not fix a weak offer. Run the offer-build skill first (it may be namespaced in some installs, for example offer-skills:offer-build).
- The audience has seen the offer once or a few times. Most people miss an offer the first time, so one pass is not fatigue; the fix is new creative and copy.
- The offer is making money and converting. Changing it out of boredom adds operational cost.
- The name pairs a quantified claim (income, weight, followers) with an interval and will run on an ad platform. Most platforms reject that pairing because it implies a guarantee. Use the interval only with a goal that is not a quantified claim ("Ship Your First Feature in 7 Days", not "$5,000 in 7 Days"), or drop it.

## Procedure

1. **Collect the inputs.** Ask in one message for: what the offer delivers, the ideal buyer (as narrow as the user can state it, with a neighbourhood or town for a local offer), the dream outcome, how long the result takes, anything free or discounted, any season or event that gives a reason to run it now, and where the name will appear. If a `CORE OFFER` block from offer-build exists, take the dream outcome and stack items from it and ask only for what is missing.

2. **Write candidates for each part.** Produce three to six options per part, using the word lists in `references/examples.md`.
   - **Magnet (the reason why).** Goes at the front and says why the offer is being made or why the buyer should respond. Examples: Free, Launch Week, Anniversary.
   - **Avatar.** Names who the offer is for, and so who it is not for. Match the real buyer; a local offer names the neighbourhood, not the city. Example: "Etsy Candle Sellers".
   - **Goal.** The dream outcome as an event, feeling, experience or result, as concrete as possible. Example: "Inbox Zero".
   - **Interval.** Minutes, hours, days, weeks or months ("14 Day"). Apply the ad platform rule above.
   - **Container.** A word marking a bundle or system that cannot be price compared with a commodity item. Examples: Sprint, Blueprint, Reset.

3. **Combine into names.** Build at least eight candidates from three to five parts each. Any order is allowed. Rhyme or alliteration is optional and should never be forced. A store listing title or ad headline has a length limit, which favours three parts. Good: "Free 14 Day Invoice Cleanup Sprint". Weak: "Bookkeeping Package".

4. **Pick two or three to test.** Nobody can predict which name wins, so do not argue on taste. Recommend two or three for a side by side test in ads or on the page, keep the winner as control, and test later names against it.

5. **Name the stack items and bonuses.** Apply the formula to each core offer stack item and each bonus. If offer-bonuses already named the bonuses, change only the weak ones.

6. **For a fatigued offer, walk the change order before renaming.** The order, lightest first, is: creative, ad body copy, headline (the name), duration, the free or discount component, then the monetization structure as a last resort. Most fatigue is fixed by repeating the first three. State the user's current step and the next change (details in the "Renames and fatigue examples" section of `references/examples.md`).

7. **Answer how often to rename.** No fixed calendar exists. Rename when response stays down after creative and copy changes stop helping. Estimate reach first: about $20 reaches 1,000 people, so a 200,000 person area costs about $4,000 to reach once (the book prints a different figure, but 200 times $20 is $4,000), and one full pass is still not fatigue.

8. **Hand back the NAME block.** Fill the Output block below. Next: naming is the last step in the run order (offer-market, offer-build, offer-scarcity, offer-urgency, offer-bonuses, offer-guarantees, offer-naming), so return to the offer skill (it may be namespaced in some installs, for example offer-skills:offer) for the summary.

## Output

````
NAME
Final name: <name>
MAGIC parts used: <for example Magnet, Interval, Goal, Container>
Alternates:
1. <name> (parts: <parts>)
2. <name> (parts: <parts>)

Stack and bonus names (if any): <item: name>
Fatigue step (if asked): <step and next change>

Copy to paste:
```
<final name as it will appear on the page, listing or ad>
```
````

## Rules

- Every candidate uses three to five MAGIC parts, and the agent can label which ones.
- The goal is a concrete outcome, event or feeling, not a feature list.
- No candidate for an ad platform pairs a quantified claim with an interval.
- The container word describes a bundle or system, not a commodity item.
- Do not skip to duration, discount or pricing changes before creative, copy and headline have been tried.
- Do not ship a generic placeholder name. The book reports that a better name on the same offer can raise response two to ten times.

## References

- `references/examples.md`: word lists for each MAGIC part, rhyme and alliteration patterns, a part by part breakdown of sample names, the fatigue change order with rename examples, and worked examples for small software and service products.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
