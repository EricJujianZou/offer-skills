---
name: offer-market
description: "Chooses the market and niche for an offer and sets a premium price, rating the market on four pass or fail tests (pain, purchasing power, easy to target, growing). Use when the user says \"what should I charge\", \"is my price too high\", \"should I lower the price\", \"should I offer a discount\", \"should I give a discount\", \"who should I sell this to\", \"is this a good market\", \"should I niche down\", \"should I switch niches\" or \"how do I stop competing on price\", or when a product is priced by copying competitors. Not for building the offer contents or the value equation (offer-build), and not for scarcity, urgency, bonuses, guarantees or naming (offer-scarcity, offer-urgency, offer-bonuses, offer-guarantees, offer-naming)."
---

# Offer market

## What this is

This skill decides who an offer is sold to and what it costs, before the contents are built. A commodity is a product sold by many sellers, so buyers compare on price and margins shrink. The fix is a market that passes the four market tests (pain, purchasing power, easy to target, growing), narrowed to one type of buyer and charged a premium price well below the value delivered. The price-to-value gap is the distance between what the buyer perceives the offer is worth and what it costs.

## When to use it, when not to

- Use it when the audience is undecided or broad ("small businesses", "anyone").
- Use it when the price was copied from competitors, or the user is considering a discount or price cut.
- Use it when sales are weak and the user is about to change the product or niche. Market outranks offer and persuasion, so it is checked first.
- Do not use it when market and price are settled and the user wants to design the contents. Run the offer-build skill (it may be namespaced in some installs, for example offer-skills:offer-build).
- A shrinking market can sink a strong offer with a strong salesperson. No pricing or offer work fixes it.
- A price cut is valid only when the business delivers at roughly one tenth of competitors' cost.
- A premium price backfires when the product has not yet delivered the result reliably. Raising the price on a product that does not work brings refunds.
- Niching down pays below about $10M a year in revenue. Above that, a small niche may force a move to an adjacent market.

## Procedure

1. **Check for commoditization.** Ask in one message for the competitors a buyer would see as interchangeable and their prices, the user's price, the direct cost of serving one more customer, and how many times an average customer buys. Compute lifetime gross profit as (price minus direct cost) times purchases; indirect costs such as rent and software are excluded. If the purchase count is unknown, use 1 for a one-time product and 6 for a monthly subscription, and say so. Good output: one line on whether the offer is commoditized (the goal is a "category of one" that buyers cannot compare side by side), the competitor price range, and lifetime gross profit per customer.

2. **Run the four market tests.** Ask the user to name the market in one sentence and check that it sits inside health, wealth or relationships, the three markets that always exist. Rate each test pass or fail with one reason:
   - **Pain.** Pass if the buyer badly needs the result and the user can state the pain in the buyer's words.
   - **Purchasing power.** Pass if a typical buyer has or controls a budget that covers the price. A resume service for unemployed people fails.
   - **Easy to target.** Pass if the user can name three specific places (associations, mailing lists, online groups, channels) where hundreds of these buyers can be reached this week.
   - **Growing.** Pass if the number of people searching for or paying for the category rose over the last three years. Sources: Google Trends for the category terms, app store or marketplace listing counts, job postings that name the problem or tool, or the user's own inbound volume. If no source can be checked (for example, no web tool is available), rate it "unverified", not fail, and say which data was missing.

   A fail on pain or purchasing power means pick a different market before any other work. A fail on easy to target or growing means narrow the niche or collect the missing evidence first.

3. **Niche down and commit.** Narrow the buyer until the product reads as "I solve [problem] for [specific type of person]". Build a pricing ladder of at least three levels, each with a narrower title, the buyer, what one more result is worth to that buyer, and the price (method in references/niche-and-price.md). Name who will be turned away. Tell the user to stay in the niche through repeated trial and error, since one failed offer means the offer failed, not the market. Good output: the niche sentence, the ladder, and the excluded buyers.

4. **Set a premium price.** Estimate the value to the buyer in money (extra revenue per year, or hours saved times the buyer's hourly rate). If the user cannot estimate it, ask for one recent customer's before and after numbers and extrapolate. Set the price as a fraction of that value so the buyer still gets a clear deal. For a subscription, compare value and price per year (12 times the monthly price) unless the user says otherwise. Aim far enough above competitors that the buyer assumes something different is going on; the book's case priced at three times the highest competitor. A price that requires the buyer's own work should sting a little, since buyers who pay more follow through more. Good output: price or range, value estimate, value to price ratio, competitor range, and any missing proof of delivery.

5. **Explain the price choice.** Summarize the price cycle from references/niche-and-price.md in two sentences. If the user asked about a discount, recommend a bonus instead and run the offer-bonuses skill (it may be namespaced in some installs, for example offer-skills:offer-bonuses).

## Output

```
MARKET
Niche: <one line, "I solve [problem] for [specific person]">
Market tests:
  Pain: <pass|fail> - <one reason>
  Purchasing power: <pass|fail> - <one reason>
  Easy to target: <pass|fail> - <one reason>
  Growing: <pass|fail|unverified> - <one reason, naming the data source checked>
Price position: premium, <number or range> (competitors <range>)
Why the user can charge it: <one line tying price to value delivered>
```

Next: run the offer-build skill (it may be namespaced in some installs, for example offer-skills:offer-build) to build the core offer stack for this niche and price.

## Rules

- Do not rate the strength of the offer here. That is offer-build's job.
- Serve buyers who can pay what the work is worth.
- Do not average competitors' prices and go slightly lower. That leaves only enough margin to stay open.
- Widen the gap between value and price by raising value first, then price. Price can only fall to zero.
- Measure success by profit, not customer count.
- Flag a premium price that lacks delivery evidence in the reason line.

## References

- references/niche-and-price.md: the niche pricing ladder, the price cycle (what a price cut and a price rise do to buyers and margin), and examples for small software and service products.
- references/book-examples.md: the book's market and pricing cases, arranged by the user's situation, and growth arithmetic.

Based on ideas from Alex Hormozi's book "$100M Offers". Not affiliated with or endorsed by the author.
