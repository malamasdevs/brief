# brief

`brief` is a small skill for getting shorter, clearer AI answers without losing technical accuracy.

It is built for people who already like their model, but want better output discipline:

- fewer words
- less filler
- faster reading
- cleaner day-to-day use

## Why this exists

Most AI output is not wrong.

It is just longer than it needs to be.

That creates three problems:

1. You spend more time reading.
2. You pay for more output tokens.
3. The useful part is harder to find.

`brief` fixes that by changing the default style of the answer, not the model itself.

## What it does

`brief` tells the model to:

- answer first
- keep only the context that changes the answer
- remove filler and repeated points
- state tradeoffs plainly
- stay concise without becoming vague

The result is not "caveman mode."

The goal is simple: professional, high-signal answers that are easy to scan.

## Who it is for

`brief` is useful for:

- developers
- founders
- CTOs
- operators
- product teams
- anyone using AI for real work

Especially for:

- coding help
- architecture tradeoffs
- code review comments
- technical explanations
- product decisions
- executive-style summaries

## What is inside

- [SKILL.md](./SKILL.md): the core skill

## How to use it

If your tool supports skills, install or place the skill where that tool expects it.

If your tool does not support skills directly, copy the rules from `SKILL.md` into:

- your system prompt
- your project rules
- your reusable prompt template

## Core idea

Same model.

Same prompt.

Better default output.

That means:

- less reading time
- fewer output tokens
- cleaner communication
- more useful answers

## Example

Without `brief`:

> In most early-stage SaaS products, a monolith is the better starting point because it reduces operational complexity, simplifies deployment, and allows teams to move faster while the product and organization are still changing rapidly...

With `brief`:

> Start with a monolith. Faster to build, easier to debug, cheaper to run. Move to microservices only when scaling pain makes it worth it.

Same point.
Less noise.

## Positioning

`brief` is not a new model.

It is a better answer style for the model you already use.

## License

MIT
