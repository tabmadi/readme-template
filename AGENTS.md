# Agent guide

Tool-agnostic guide for any coding agent (Codex, Cursor, Claude Code, or another) working in this repo. `AGENTS.md` is the one standard: an agent either reads it or it does not — the repo carries no per-tool shim files (`CLAUDE.md`, `.cursor/rules/`, etc.). A tool that ignores `AGENTS.md` is a limitation of that tool, not something the repo works around.

## The one rule that outranks this file

**Humans are the first developers. [README.md](README.md) outranks this file.** It is the human-facing description of what this template provides and how to use it. This file holds only agent-specific operational hints: how to navigate the repo.

## What this repo is

A README authoring kit. It ships no application code — the deliverables are four markdown files, each with a distinct job:

| File | Job |
| --- | --- |
| [TEMPLATE.md](TEMPLATE.md) | The canonical README skeleton: section order, headings, badge row. The structure every generated README follows. |
| [AI_INSTRUCTIONS.md](AI_INSTRUCTIONS.md) | Instructions for an agent that can read the target codebase and fill the template from what it finds. |
| [PROMPT.md](PROMPT.md) | A fill-in-the-blanks prompt for a chat assistant with no repo access. |
| [README.md](README.md) | This repo's own README, and a worked example of the house style. |

**Using this repo means reading it, not running it.** To write a README for another project, load `AI_INSTRUCTIONS.md` and follow it against that project's code; `TEMPLATE.md` is the shape of the answer.

## Changing the kit

- **The three files drift apart easily, so change them together.** A section added to `TEMPLATE.md` is a section `AI_INSTRUCTIONS.md` must tell the agent to fill and `PROMPT.md` must ask the user about. Verify all three after any structural edit.
- **Keep the emoji headings.** They are the recognisable signature of this README style across the template set; consistency with the sibling templates' READMEs is the point.
- `TEMPLATE.md` holds placeholders, never real content. A concrete project name, URL, or badge target committed there leaks into every generated README.
- Prose is the product here. Write for a developer landing on the repo cold: what it does, how to run it, what to configure — in that order, with no marketing.

## Working in the repo

- The task runner is `mise` (root `mise.toml`); commands are `mise run <task>`. `mise run setup` installs the git hooks.
- Tool versions live in [.tool-versions](.tool-versions) here, not in a `[tools]` block — the one deviation from the sibling templates.
- The `format` and `lint` tasks are `echo "Ok"` placeholders — there is no code to check. Keep the task names so the repo matches its siblings.
- `mise run act` replays the pull request workflow locally with [act](https://github.com/nektos/act). It reads secrets from `.env`.

## Commits

- **Conventional Commits, enforced.** `cog verify` runs on `commit-msg` and `cog check` on `pre-push`, so a malformed message is rejected locally before CI sees it.
- Commit messages are a title only — no body, no footer.
- Never push unless asked to.
