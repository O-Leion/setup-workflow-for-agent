# setup-workflow-4-Cline

🌐 [日本語版 (Japanese)](./README.md)

**AI Agent Workspace Scaffolder for Cline**

An automated workflow for building optimized workspace environments for AI agent development in Cline (VS Code AI extension).
It safely sets up a project structure with rule definitions in `.clinerules/` and AI exclusion settings in `.clineignore` through an interactive process.

## 🚀 Features

* **Interactive Setup**: The AI scans your current environment and guides you through the setup process.
* **Rule Management**: Organizes project rules with numbered files in the `.clinerules/` folder.
* **AI Exclusion Settings**: Uses `.clineignore` to exclude unnecessary files from AI analysis.
* **Structured Directories**: Automatically separates `docs`, `src`, and `tests`.

## 📦 Installation

### 1. Prerequisites

> ⚠️ Cline does not have a built-in Global Workflows mechanism. Place this workflow file in the root of your new project and have Cline's AI read it to use.

### 2. Usage
1. Open a new project (empty folder) in VS Code.
2. Place `setup-assistant.md` in the project root.
3. In Cline's chat, enter the following instruction:

> **"Read `setup-assistant.md` and run the setup"**

4. After setup is complete, you may delete `setup-assistant.md`.

## 📂 Generated Structure

```text
.
├── .clinerules/          <-- [AI Rule Config]
│   ├── 01-coding-standards.md
│   └── 02-project-conventions.md
├── .clineignore          <-- [AI Exclusion Config]
├── docs/                 <-- [Documentation]
│   └── design/
├── src/                  <-- [Source Code]
├── tests/                <-- [Test Code]
├── scratchpad.md         <-- [AI Work Log]
└── .gitignore            <-- [Git Config]
```

## License

MIT License
