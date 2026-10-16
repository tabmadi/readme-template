# Instructions for a coding agent

Use these instructions with a coding agent that can read the target repo. The agent writes or rewrites the target repo's `README.md`.

## Steps

1. Read the target repo: its config files, task runner, source layout, and existing docs.
2. Choose the size of the repo:
   - **Platform**: it runs a whole system and has a full ADR set.
   - **Template**: it is a base to start a new project from.
   - **Example**: it teaches one idea and is not a base to fork.
3. Read the skeleton for that size: [template](skeletons/template/README.md), [example](skeletons/example/README.md), or [platform](skeletons/platform/README.md).
4. Read the house style in [ADR-0001](docs/adr/0001-documentation-conventions.md).
5. Fill every section from what the repo contains. Take each command from the task runner, and run it if you can.
6. Delete a section that has nothing to say. Never leave a placeholder.
7. Check the result with `rumdl check README.md`.

## Rules for the text

- Keep the section order and the headings of the skeleton.
- Write in Simple English: common words, one idea per sentence, at most 25 words.
- Use only period, comma, colon, and the possessive apostrophe in prose.
- Use no emoji and no marketing. State what the repo does.
- Write a table compact, and do not hard-wrap a paragraph.
- Every claim is true of the code. Do not describe a feature the repo does not have.

## A prompt to start

> Read `AI_INSTRUCTIONS.md` in <https://github.com/tabmadi/readme-template> and follow it to write `README.md` for this repo.
