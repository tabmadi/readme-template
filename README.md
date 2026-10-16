# README Template

The README and `AGENTS.md` skeletons for every repo in the [blueprints](https://github.com/tabmadi/blueprints) set, and the instructions to fill them with a coding agent or a chat assistant.

A repo has one of three sizes: platform, template, or example. Each size has its own skeleton, because one shape does not fit a whole platform and a small example.

## What it holds

| File | Use it to |
| --- | --- |
| [skeletons/template/](skeletons/template/README.md) | Write the README and `AGENTS.md` of a template: a base to start a new project from |
| [skeletons/example/](skeletons/example/README.md) | Write the README and `AGENTS.md` of an example: a repo that teaches one idea |
| [skeletons/platform/](skeletons/platform/README.md) | Write the README of a platform: a repo that runs a whole system |
| [AI_INSTRUCTIONS.md](AI_INSTRUCTIONS.md) | Let a coding agent read a repo and fill the right skeleton |
| [PROMPT.md](PROMPT.md) | Let a chat assistant with no repo access fill a skeleton from facts you give it |

The house style for all text is [ADR-0001](docs/adr/0001-documentation-conventions.md): Simple English, no emoji, compact tables, and no hard-wrapped paragraphs.

## Using it

1. Choose the size of your repo. [ADR-0000](docs/adr/0000-foundations.md) defines the three sizes.
2. Give your coding agent this prompt from the root of your repo:

   > Read `AI_INSTRUCTIONS.md` in <https://github.com/tabmadi/readme-template> and follow it to write `README.md` for this repo.

3. With no coding agent, fill in [PROMPT.md](PROMPT.md) and paste it into a chat assistant.
4. Check the result with `rumdl check README.md`.

## Getting started

To change the skeletons, set up this repo:

1. Install [mise](https://mise.jdx.dev/getting-started.html).
2. Clone the repo and install the tools and hooks:

   ```bash
   git clone git@github.com:tabmadi/readme-template.git
   cd readme-template
   mise install
   mise run setup
   ```

## Tasks

| Task | Does |
| --- | --- |
| `mise run setup` | Installs the git hooks |
| `mise run format` | Applies the Markdown fixes |
| `mise run lint` | Runs `lint:md` and `lint:secrets` |
| `mise run check` | Runs `lint` and `test`. Run it before you finish a change |
| `mise run ci` | Runs exactly what CI runs. The `pre-push` hook runs it too |

## Layout

```text
.
├── skeletons/
│   ├── template/       README.md and AGENTS.md for a template
│   ├── example/        README.md and AGENTS.md for an example
│   └── platform/       README.md for a platform
├── docs/adr/           The decisions: sizes, doc conventions, toolchain
├── AI_INSTRUCTIONS.md  Instructions for a coding agent
├── PROMPT.md           A prompt for a chat assistant
└── AGENTS.md           Hints for coding agents that change this repo
```

## Decisions

The ADRs in [docs/adr](docs/adr/README.md) record every decision and the reason for it.

## Contributing

Follow the [Code of Conduct](CODE_OF_CONDUCT.md). Commit messages follow [Conventional Commits](https://www.conventionalcommits.org), and the `commit-msg` hook checks them. Run `mise run check` before you open a pull request.

## Security

To report a vulnerability, follow [SECURITY.md](SECURITY.md).

## License

Apache License 2.0. See [LICENSE](LICENSE).
