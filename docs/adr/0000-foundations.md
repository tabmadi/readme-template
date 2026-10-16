# ADR-0000: Foundations

**Status:** Accepted
**Decides:** What this repo is, the three repo sizes, and the ADR process itself.

## Context

The [blueprints](https://github.com/tabmadi/blueprints) set holds platforms, templates, and examples. One README shape does not fit all three. A short skeleton leaves a platform with no place for its selection guidance. A long skeleton fills a small example with empty sections.

A README written from no skeleton drifts from its siblings. A reader then has to learn each repo's layout before reading it.

## Decision

This repo holds the README and `AGENTS.md` skeletons for every repo in the set, and the instructions to fill them. It ships no application code.

**A repo has one of three sizes.** The size decides the README skeleton and the size of the ADR set.

| Size | Is | README skeleton | ADRs | `AGENTS.md` skeleton |
| --- | --- | --- | --- | --- |
| Platform | A repo that runs a whole system, with many decisions | `skeletons/platform/` | a full set | its own |
| Template | A base to start a new project from | `skeletons/template/` | 0000, 0001, and 0100 | `skeletons/template/` |
| Example | A repo that teaches one idea, not a base to fork | `skeletons/example/` | none | `skeletons/example/` |

**A skeleton holds placeholders only.** A placeholder is in braces, such as `{Project Name}`. A concrete name, URL, or badge target in a skeleton leaks into every README made from it.

**A section with nothing to say is deleted.** It is never kept with a placeholder or a `TBD`.

**Every decision is an ADR.** An ADR states what is true of the repo. It is law, not a plan. Planned work lives in an untracked `*.local.md` file.

## Consequences

A change to a skeleton changes what every repo of that size should look like. The blueprints repo applies the change to each of them in one pass.

The documentation rules live in [ADR-0001](0001-documentation-conventions.md), which is a copy of the one in [github-project-template](https://github.com/tabmadi/github-project-template). A skeleton never restates those rules.

## Rules

- Every README in the set follows the skeleton for its size.
- A skeleton holds only placeholders in braces.
- `skeletons/`, `AI_INSTRUCTIONS.md`, and `PROMPT.md` change together. A section added to a skeleton is a section the instructions tell the writer to fill.
- Every ADR carries a `Status`, a one-sentence `Decides` line, and a flat `Rules` section.
- Planned work lives in an untracked `*.local.md` file. No committed file links to one.
