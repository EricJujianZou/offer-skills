# Audit checklist for an existing offer

A note "fix with offer-x" means run that skill, which may be namespaced in some installs (for example offer-skills:offer-x).

Run every test. Each test is pass, fail, "not checked" or "not applicable", never a score. A pass needs one line of evidence: a quote from the page, script or listing, or the user's answer to a question. Tests the page does not answer and the user was not asked are marked "not checked", not failed. Each section names the sibling skill that fixes a fail in it. If that sibling is not installed, use its paragraph in `references/fallbacks.md`.

The book ranks the market above offer strength and offer strength above persuasion skill. Report fails in section order, A first.

## A. Market and price -> fix with offer-market

The first four tests are the four market tests, rated the same way offer-market rates them.

| # | Test | Pass when |
|---|---|---|
| A1 | Pain | The buyer has a problem they urgently need solved, not a nice-to-have, and the page states that pain. |
| A2 | Purchasing power | The niche has, or can get, the money for the price. A resume service sold to people with no income fails. |
| A3 | Easy to target | The user can name where the niche gathers: associations, mailing lists, online groups, channels they follow. |
| A4 | Growing | The number of people searching for or paying for the category rose over the last three years (Google Trends, app store or marketplace listing counts, job postings, or the user's own inbound). Unknown counts as fail, with the reason. |
| A5 | One named niche | The offer names one specific buyer group, and the user has not switched niche in the last few months. "Anyone who wants to grow" fails. |
| A6 | Not a commodity | A buyer reading the offer could not call it the same as a named alternative and pick the cheaper one. |
| A7 | Premium price | The price is not set to undercut competitors. |

## B. Core offer -> fix with offer-build

The value equation is dream outcome times perceived likelihood of achievement, divided by time delay times effort and sacrifice (see offer-build).

| # | Test | Pass when |
|---|---|---|
| B1 | Dream outcome, not vehicle | The headline promises the result the buyer wants (a weight loss target, not a gym membership). |
| B2 | Perceived likelihood | The page gives proof the result will happen: past results, numbers, testimonials, a guarantee. |
| B3 | Time delay | The page says how soon the buyer gets the first result. |
| B4 | Effort and sacrifice | The page shows what the seller does so the buyer does less. |
| B5 | Problems listed | The offer covers the obstacles the buyer meets before, during and after using the product, not only the main task. |
| B6 | Each problem has a named solution | Every listed problem maps to a deliverable with its own name. |
| B7 | Delivery method stated | Each deliverable says how it is delivered (one to one, group, one to many, done for the buyer, software, template). |
| B8 | Trimmed | No item remains that costs the seller a lot and gives the buyer little. |
| B9 | Core offer stack with values | Each item shows a stated value, and the total is a large multiple of the price (the book's gym example sold a stated value of $4,351 for $599). For a subscription, use the price per year (12 times the monthly price) unless the user says otherwise. |

## C. Scarcity -> fix with offer-scarcity

| # | Test | Pass when |
|---|---|---|
| C1 | Scarcity present | The offer states one of the three types: limited supply, limited bonuses, or never available again. "None" with a stated reason also passes, as does the user confirming that no real limit exists. |
| C2 | Scarcity is real | The user confirms the limit matches a real capacity or a real decision. A countdown that resets, or an "only 3 left" that never changes, fails. |
| C3 | Supply under demand | The user does not sell to every prospect at once; some demand stays unmet for the next round (chapter 11, in `references/enhancers.md`). Not applicable for a software product with no seat cap. |

When C1 is "none" with a stated reason, or fails, mark C2 and C3 "not applicable".

## D. Urgency -> fix with offer-urgency

| # | Test | Pass when |
|---|---|---|
| D1 | Urgency present | The offer uses one of the four types: rolling cohorts, rolling seasonal, pricing or bonus based, exploding opportunity. "None" with a stated reason also passes, as does the user confirming that no real deadline exists. |
| D2 | Urgency is real | The deadline or start date actually happens, and the stated result of missing it is true. |

When D1 is "none" with a stated reason, or fails, mark D2 "not applicable".

## E. Bonuses -> fix with offer-bonuses

| # | Test | Pass when |
|---|---|---|
| E1 | Bonuses offered | The offer has bonuses at all. |
| E2 | Core versus bonus split | Each bonus passes the wow test in offer-bonuses, and nothing the buyer must not skip is listed as a bonus. |
| E3 | Named with a benefit | Each bonus has a name that states a benefit. |
| E4 | Removes an obstacle | Each bonus removes a specific obstacle or answers a specific objection. |
| E5 | Proof and stated value | Each bonus has proof that it works and a stated value with a reason for the number. |
| E6 | Bonus value exceeds core value | The total bonus value is larger than the core offer stack value. |

When E1 is "none" with a stated reason, or fails, mark E2 to E6 "not applicable".

## F. Guarantee -> fix with offer-guarantees

| # | Test | Pass when |
|---|---|---|
| F1 | Kind chosen | The offer uses one of the four kinds: unconditional, conditional, anti-guarantee, implied. |
| F2 | Visible | The guarantee sits near the price and the call to action, not only in the footer or terms. |
| F3 | Reason why | The guarantee says why the seller can make it. |
| F4 | Exact terms | A buyer can tell what they must do and what they get back. |
| F5 | Cost known | The user knows the expected refund or payout cost, or uses the default in offer-guarantees until real data exists. |

When F1 is "none" with a stated reason, or fails, mark F2 to F5 "not applicable".

## G. Name -> fix with offer-naming

The MAGIC formula builds a name from up to five parts: Magnet (the reason why), Avatar, Goal, Interval, Container (see offer-naming).

| # | Test | Pass when |
|---|---|---|
| G1 | Has a name | The offer has its own name, not a generic one ("Pro plan", "Coaching"). |
| G2 | Three to five MAGIC parts | The name uses at least three of the five parts. |
| G3 | Calls out the buyer | The name or headline tells the right buyer it is for them and turns away the wrong buyer. |

## H. Whole offer -> fix with the sibling of the first failing section above

| # | Test | Pass when |
|---|---|---|
| H1 | No comparison possible | The buyer's choice is between this offer and nothing, because no competitor offers the same bundle, terms and guarantee. |
| H2 | Payment terms stated | The page states the price and how payment is taken. |
| H3 | Easy yes | A target buyer reading only the page sees a stated value far above the price, a reason to act now, and little risk. |

## Reporting

Write the result as the Audit mode table in SKILL.md. List the top three fixes in section order, A first, each with the sibling and the one input it needs from the user. Any fail in section A is fixed first, even if sections C to G fail more often.
