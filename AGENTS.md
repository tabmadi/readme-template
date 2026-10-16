# Agent guide

This guide is for any coding agent that works in this repo. `AGENTS.md` is the one standard, and the repo has no per-tool files such as `CLAUDE.md`.

**Humans are the first developers. The ADRs and `README.md` rank above this file.** This file holds only operational hints.

## Read first

- [ADR-0000](docs/adr/0000-foundations.md): the three repo sizes and what each skeleton is for.
- [docs/adr/README.md](docs/adr/README.md): the ADR index.

## Write in Simple English

Every text follows the Simple English profile in [ADR-0001](docs/adr/0001-documentation-conventions.md#simple-english). Here the text is the product, so this matters most.

- Use common words. One idea per sentence, at most 25 words.
- In prose, use only period, comma, colon, and the possessive apostrophe. No em dash, semicolon, parentheses, or `?`.
- No emoji, no contractions, and no `e.g.` or `etc.`

## Changing the kit

- `skeletons/`, `AI_INSTRUCTIONS.md`, and `PROMPT.md` drift apart easily. Change them together, and check all three after a structural edit.
- A skeleton holds placeholders in braces only. A real name or URL there leaks into every README made from it.
- A skeleton change applies to every repo of that size. The [blueprints](https://github.com/tabmadi/blueprints) repo rolls it out.
- Run every command as `mise run <task>`. Before you finish a change, run `mise run check`.
- Commit messages are a Conventional Commits title only, with no body. Never push unless asked to.
