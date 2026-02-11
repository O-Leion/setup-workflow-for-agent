# setup-workflow-4-RooCode

🌐 [日本語版 (Japanese)](./README.md)

**AI Agent Workspace Scaffolder for Roo Code**

An automated workflow for building optimized workspace environments for AI agent development in Roo Code (VS Code AI extension).
It safely sets up an advanced structure with workspace-wide rules and mode-specific rules (Code, Architect, Ask, Debug) consolidated in the `.roo/` folder through an interactive process.

## 🚀 Features

* **Interactive Setup**: The AI scans your current environment and guides you through the setup process.
* **Mode-Specific Rules**: Set dedicated rules for each of Roo Code's 4 modes (Code, Architect, Ask, Debug).
* **Rule Hierarchy**:
    * `.roo/rules/`: Workspace-wide rules (applied to all modes)
    * `.roo/rules-code/`: Code mode specific rules
    * `.roo/rules-architect/`: Architect mode specific rules
    * `.roo/rules-ask/`: Ask mode specific rules
    * `.roo/rules-debug/`: Debug mode specific rules
* **Custom Modes**: Define project-specific custom modes via `.roomodes`.
* **Structured Directories**: Automatically separates `docs`, `src`, and `tests`.

## 📦 Installation

### 1. Prerequisites

> ⚠️ Roo Code does not have a built-in Global Workflows mechanism. Place this workflow file in the root of your new project and have Roo Code's AI read it to use.

### 2. Steps
1. Open a new project (empty folder) in VS Code.
2. Place `setup-assistant.md` in the project root.
3. In Roo Code's chat, enter the following instruction:

> **"Read `setup-assistant.md` and run the setup"**

4. After setup is complete, you may delete `setup-assistant.md`.

## 📂 Generated Structure

```text
.
├── .roo/                     <-- [AI Config] (Hidden folder)
│   ├── rules/                <-- Workspace-wide rules
│   │   ├── 01-coding-standards.md
│   │   └── 02-project-conventions.md
│   ├── rules-code/           <-- Code mode rules
│   ├── rules-architect/      <-- Architect mode rules
│   ├── rules-ask/            <-- Ask mode rules
│   └── rules-debug/          <-- Debug mode rules
├── .roomodes                 <-- [Custom Mode Definitions]
├── docs/                     <-- [Documentation]
│   └── design/
├── src/                      <-- [Source Code]
├── tests/                    <-- [Test Code]
├── scratchpad.md             <-- [AI Work Log]
└── .gitignore                <-- [Git Config]
```

## ⚠️ If the Hidden Folder (.roo) Is Not Visible

This workflow stores configuration files in a hidden folder called `.roo`. Follow the instructions below to make it visible.

### macOS (Finder)
* Press **`Command` + `Shift` + `.` (dot)** to toggle visibility.

### Windows (File Explorer)
1. Click **[View]** tab → Enable **[Hidden items]**.

### VS Code
```json
"files.exclude": {
    "**/.roo": false
}
```

## License

MIT License
