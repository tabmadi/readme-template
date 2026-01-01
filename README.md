# 🚀 README Template

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Language](https://img.shields.io/badge/Language-Markdown-blue.svg)](https://www.markdownguide.org/)
[![Tool](https://img.shields.io/badge/Tool-Mise-green.svg)](https://mise.jdx.dev/)

A standardized template and set of instructions for generating high-quality project READMEs using AI assistants or
manual curation.

## ✨ Features

- ⚡ **Standardized Structure**: Follows a consistent and professional layout.
- 🤖 **AI-Ready**: Includes `AI_INSTRUCTIONS.md` to help AI assistants generate content.
- 🔧 **Modern Tooling**: Integrated with **Mise**, **Lefthook**, and **Cocogitto**.
- 📁 **Organized**: Clean project structure for easy maintenance.

## 🚀 Quick Start

### Prerequisites

- [Mise](https://mise.jdx.dev/) - Tool version manager
- [Git](https://git-scm.com/) - Version control

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/username/readme-template.git
   cd readme-template
   ```
2. **Setup environment**:
   ```bash
   # Installs mise and all defined tools
   ./scripts/install.sh
   ```

## 🏃‍♂️ Usage

To use this template for your own project, copy `TEMPLATE.md` to your project and follow the instructions in
`AI_INSTRUCTIONS.md` with your preferred AI assistant.

```bash
# Copy the template to your project
cp TEMPLATE.md path/to/your/project/README.md
```

## 🛠️ Development

### Available Scripts

| Script   | Description                     |
|----------|---------------------------------|
| `setup`  | Install Git hooks via Lefthook  |
| `lint`   | Run linting checks              |
| `format` | Run formatting                  |
| `act`    | Run local CI checks using `act` |

### 🧹 Code Quality

We use `mise` tasks for linting and formatting:

```bash
# Run linting
mise run lint

# Run formatting
mise run format
```

### 🪝 Git Hooks & Conventional Commits

This project uses **Lefthook** for Git hooks and follows **Conventional Commits**.

- **Pre-commit**: Runs linting tasks.
- **Commit-msg**: Validates commit messages using `cog`.
- **Pre-push**: Checks commit history consistency.

## 📁 Project Structure

```
.
├── .github/             # GitHub templates and workflows
├── scripts/             # Helper scripts
│   └── install.sh       # Project setup script
├── AI_INSTRUCTIONS.md   # AI assistant guide
├── CODE_OF_CONDUCT.md   # Community standards
├── LICENSE              # Apache 2.0
├── PROMPT.md            # LLM prompt context
├── README.md            # You are here! 📍
├── SECURITY.md          # Security policy
├── TEMPLATE.md          # The README template itself
└── mise.toml            # Task runner configuration
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the project
2. Create your feature branch
3. Commit your changes (Conventional Commits)
4. Push to the branch
5. Open a Pull Request

## 🔒 Security

Please see [SECURITY.md](SECURITY.md) for our security policy.

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

---
**Happy coding! 🎉** If you find this project useful, please give it a ⭐️
