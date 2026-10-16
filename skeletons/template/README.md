# {Project Name}

{One paragraph: what this template is, who it is for, and what a repo made from it starts with.}

## Stack

| Tool | Owns |
| --- | --- |
| [{tool}]({url}) | {the one job this tool does in the repo} |

## Getting started

1. Install [mise](https://mise.jdx.dev/getting-started.html).
2. Clone the repo and install the tools, dependencies, and hooks:

   ```bash
   git clone git@github.com:{owner}/{repo}.git
   cd {repo}
   mise install
   mise run setup
   ```

3. {The first useful command, such as `mise run dev`.}

## Tasks

| Task | Does |
| --- | --- |
| `mise run setup` | {Installs the dependencies and the git hooks} |
| `mise run format` | {Applies every formatter} |
| `mise run lint` | {Runs every linter} |
| `mise run test` | {Runs the tests} |
| `mise run check` | Runs `lint` and `test`. Run it before you finish a change |
| `mise run ci` | Runs exactly what CI runs. The `pre-push` hook runs it too |

## Layout

```text
.
├── {dir}/    {what it holds}
└── {file}    {what it holds}
```

## Configuration

{Delete this section when the repo reads no configuration.}

| Variable | Description | Default |
| --- | --- | --- |
| `{NAME}` | {what it controls} | `{value}` |

## Using this template

1. Create a repository from this template on GitHub.
2. {Each change a new project makes: names, module path, package name.}
3. Update the contacts in `SECURITY.md` and the copyright line in `LICENSE`.

## Decisions

The ADRs in [docs/adr](docs/adr/README.md) record every decision and the reason for it. [ADR-0001](docs/adr/0001-documentation-conventions.md) is the house style for all text.

## Contributing

Follow the [Code of Conduct](CODE_OF_CONDUCT.md). Commit messages follow [Conventional Commits](https://www.conventionalcommits.org), and the `commit-msg` hook checks them. Run `mise run check` before you open a pull request.

## Security

To report a vulnerability, follow [SECURITY.md](SECURITY.md).

## License

Apache License 2.0. See [LICENSE](LICENSE).
