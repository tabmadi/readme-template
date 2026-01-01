# 🤖 AI Assistant Instructions for README Generation

Use these instructions when working with Cursor, Junie, or similar AI coding assistants that have access to the codebase.

## 📋 Task
Generate or update the `README.md` for this project by inspecting the codebase and following the standardized style.

## 🛠️ Instructions for the AI
1.  **Analyze the Codebase**:
    -   Identify the **Project Name** from the root directory or configuration files (e.g., `package.json`, `go.mod`, `Cargo.toml`).
    -   Determine the **Primary Language** and **Tech Stack**.
    -   Scan for **Key Features** by looking at the source code and documentation.
    -   Identify **Installation** and **Usage** commands from scripts (e.g., `scripts/`, `Makefile`) or task runners (e.g., `mise.toml`, `moon.yml`).
    -   Extract **Available Scripts** and their purposes.
    -   Note any **Configuration** (environment variables, config files).
    -   Generate a `📁 Project Structure` ASCII tree (exclude `node_modules`, `.git`, etc.).

2.  **Follow the Template**:
    -   Strictly adhere to the structure and style defined in `TEMPLATE.md`.
    -   Use the exact emojis for headers as specified in `TEMPLATE.md`.
    -   Use Shields.io badges for License, Language, and key tools.

3.  **Drafting Rules**:
    -   **Tone**: Technical, enthusiastic, and professional.
    -   **Conciseness**: Keep descriptions clear and punchy.
    -   **Consistency**: Ensure the output matches the branding of other projects in this ecosystem (Apache 2.0 license, Lefthook for hooks, etc.).

## 🚀 Execution Command
If you are using a tool like Junie or Cursor, you can simply say:
> "Read `TEMPLATE.md` and the current codebase to generate a complete `README.md` following our standard style."
