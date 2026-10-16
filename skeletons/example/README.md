# {Example Name}

{One paragraph: the one idea this example shows, and for whom. An example teaches one thing and is not a base to fork.}

## What it shows

{The concept, explained for a reader who has not met it. Use a diagram or a worked case when it helps. Split into subsections when the idea has parts.}

## Run it

1. Install [mise](https://mise.jdx.dev/getting-started.html).
2. Install the tools and dependencies, then start it:

   ```bash
   git clone git@github.com:{owner}/{repo}.git
   cd {repo}
   mise install
   mise run setup
   mise run {start task}
   ```

3. {How to see it work: a curl call, a URL to open, or the output to expect.}

## How it works

{Where to start reading the code, file by file, in the order a reader needs it.}

| File | Holds |
| --- | --- |
| `{path}` | {what it does} |

## What is deliberately missing

{What a production system needs that this example leaves out, and why. This stops a reader from adding it back, or from copying the example as production code.}

## Tasks

| Task | Does |
| --- | --- |
| `mise run {task}` | {what it does} |
| `mise run check` | Runs `lint` and `test` |
| `mise run ci` | Runs exactly what CI runs |

## License

Apache License 2.0. See [LICENSE](LICENSE).
