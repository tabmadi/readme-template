# {Platform Name}

{Two sentences: the scope this repo serves, and the profile it implements.}

**The stance, in three lines:**

- **{Principle}.** {One sentence.}
- **{Principle}.** {One sentence.}
- **{Principle}.** {One sentence.}

## Find your profile

{A table of the profiles this repo and its neighbours serve, with a test for each. Name the one this repo implements and link the others.}

## What forces decomposition

{The forces that justify a boundary, each with a test. If no force applies, say which smaller profile fits.}

## When not to use this

{The cases where a smaller or different repo is the correct choice. This is selection guidance, so it lives here and never in an ADR.}

## Stack at a glance

| Layer | Tool | ADR |
| --- | --- | --- |
| {layer} | {tool} | [{NNNN}](docs/adr/{file}.md) |

## Getting started

```bash
mise install
mise run setup
{the commands that bring up the local environment}
```

## Layout

```text
.
└── {dir}/    {what it holds}
```

## How decisions are recorded

The ADRs in [docs/adr](docs/adr/README.md) are law: each states what is true and ends with a flat `Rules` section. [docs/README.md](docs/README.md) indexes the guides and references.

## Using this repo

{How a new project is made from this repo, and what it then owns.}

## License

Apache License 2.0. See [LICENSE](LICENSE).
