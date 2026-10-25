<h1 align="center">offer-skills</h1>

<p align="center"><b>Build or audit a product offer with the method from the book $100M Offers, inside your coding agent</b></p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-24292f?style=flat" alt="MIT License" /></a>
  &nbsp;
  <a href="https://agentskills.io"><img src="https://img.shields.io/badge/Agent_Skills-compatible-24292f?style=flat" alt="Agent Skills compatible" /></a>
  &nbsp;
  <a href="#install"><img src="https://img.shields.io/badge/works_in-Claude_Code%2C_Codex%2C_Cursor_%2B_22_more-24292f?style=flat" alt="Works in Claude Code, Codex, Cursor and 22 more agents" /></a>
</p>

<p align="center"><sub><a href="#install">Install</a> · <a href="#a-session">A session</a> · <a href="#the-eight-skills">The eight skills</a> · <a href="#credit">Credit</a> · <a href="#license">License</a></sub></p>

**offer-skills** is a set of eight skills for coding agents that turn the method from Alex Hormozi's book *$100M Offers* into a procedure the agent can run on your product. Tell it what you can deliver and who buys it, and it works through market, price, offer contents, scarcity, urgency, bonuses, guarantee and name in the order the book uses, then hands back one offer summary. Paste in a landing page or pricing page instead and it audits the offer against the same tests, with a pass or fail and one line of evidence for each, then names the skill that fixes each fail.

## Install

```
npx skills add EricJujianZou/offer-skills
```

The same command installs the skills in Claude Code, Codex, Cursor, Gemini CLI, GitHub Copilot, opencode, Windsurf, Amp, Goose and about 15 other agents. It puts them in every agent folder it finds in your project. Add `-g` to install for your user instead.

Nothing else is needed. The skills are plain text and run inside the agent.

<details>
<summary>Other ways to install</summary>

As a Claude Code plugin:

```
/plugin marketplace add EricJujianZou/offer-skills
/plugin install offer-skills@offer-skills
```

By hand, clone the repo and copy the folders under `skills/` into your agent's skills folder, such as `~/.claude/skills/` or `~/.agents/skills/`:

```
git clone https://github.com/EricJujianZou/offer-skills
cp -r offer-skills/skills/* ~/.agents/skills/
```

</details>

## A session

A build session, shortened. The agent is running the umbrella skill, which calls the other seven in turn.

```
> build me an offer for my resume review service. $40 a review, I can do about 10 a week.

Before I start I need six things in one reply: who buys it today, any proof it
works (results, counts, testimonials), your weekly capacity, your current price,
and anything on your sales calendar (term starts, application deadlines, price
changes).

> students applying to internships. 60 reviews so far, 11 told me they got
> interviews after. 10 a week. $40. co-op applications open Jan 6 and May 5.

MARKET
  Niche: engineering students applying to their first paid internship
  Pain: pass.  Purchasing power: pass (parents pay, cost of a missed term is
  high).  Easy to target: pass (program subreddits, co-op portals).
  Growing: pass.
  Price position: premium. Competitors charge $20 to $60 for one pass over the
  document and none of them promises a result.

CORE OFFER
  Dream outcome: an interview from the first batch of applications
  ...
  Total stated value: $1,140.  Proposed price: $197.

SCARCITY   10 students a week, stated on the page and held to.
URGENCY    Rolling seasonal: price rises after Jan 6 and May 5.
BONUSES    Three, worth $390 stated: application tracker, reply templates,
           one re-review after the first rejection.
GUARANTEE  Conditional: no interview within 30 days of sending 20
           applications gets a second full review free.
NAME       First Interview Resume Rebuild for Engineering Students
```

Then the summary, with every number traced back to the step that produced it, and an audit of the whole thing against the book's tests.

## Use

Say what you want in plain words. These are the phrases each skill listens for, so you never have to remember a command.

```
build me an offer for this                 # whole offer, build mode
audit my landing page                      # whole offer, audit mode
what should I charge                       # market and price only
what should I include                      # offer contents only
should I cap this                          # scarcity only
give people a reason to buy now            # urgency only
they said it's too expensive               # bonuses only
should I offer a refund                    # guarantee only
what should I call this                    # name only
```

Each part skill returns a fixed block (`MARKET`, `CORE OFFER`, `SCARCITY`, `URGENCY`, `BONUSES`, `GUARANTEE`, `NAME`). The umbrella skill assembles them, so you can also run one part on its own and paste its block into a later run.

## The eight skills

| Skill | What it does | Run order |
|---|---|---|
| `offer` | Runs the seven part skills in order and assembles one offer summary, or audits an existing page against the book's tests | umbrella |
| `offer-market` | Picks the niche with four pass or fail tests (pain, purchasing power, easy to target, growing) and sets a premium price | 1 |
| `offer-build` | Lists the buyer's problems, turns each into a deliverable, scores each against the value equation and trims to what can be delivered at scale | 2 |
| `offer-scarcity` | Adds an honest limit on seats, spots, units or bonuses | 3 |
| `offer-urgency` | Adds an honest deadline with one of four urgency types, plus the copy and scripts for it | 4 |
| `offer-bonuses` | Splits deliverables into named bonuses with a stated value, adds partner perks, decides when each is shown | 5 |
| `offer-guarantees` | Picks one of four kinds and fourteen named guarantees, then checks what refunds would cost | 6 |
| `offer-naming` | Names the offer with the five-part formula from the book and plans a rename when response drops | 7 |

The run order matters. The book sets price from the market rather than from costs, so price is decided before contents. A limit or deadline on a bonus needs the bonus to exist first, so bonuses come after scarcity and urgency, and the name is written last because it draws on every earlier block.

Every skill carries its own reference files: the book's worked examples organised by the situation you are in, the full guarantee catalogue, the value equation, scripts for the sales conversation, and fallbacks for when a sibling skill is not installed. The skills paraphrase the method and contain no passages from the book.

## Credit

The method is Alex Hormozi's, from *$100M Offers: How to Make Offers So Good People Feel Stupid Saying No* (Acquisition.com Publishing, 2021). This project is not affiliated with, endorsed by or sponsored by Alex Hormozi or Acquisition.com. The skills restate the procedure in their own words and cite the book at the end of each skill file. The book has the reasoning and the stories these skills leave out, so buy it.

## License

MIT
