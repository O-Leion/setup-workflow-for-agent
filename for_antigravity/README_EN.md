# setup-workflow-4-Antigravity

🌐 [日本語版 (Japanese)](./README.md)

**AI Agent Workspace Scaffolder for Google Antigravity**

An automated workflow for building optimized workspace environments for AI agent development in Google Antigravity (AI-first IDE).
It safely sets up an advanced directory structure called "Expert Configuration," which consolidates all configuration files into an `.agent` folder, through an interactive process.

## 🚀 Features

* **Interactive Setup**: Instead of generating files immediately, the AI scans your current environment and guides you through the setup process.
* **Expert Configuration**: Consolidates rules and skill definitions into `.agent/` (hidden folder), keeping the root directory clean.
* **Best Practices Built-in**:
    * `GEMINI.md`: Project context definition
    * `.gitignore` & `.geminiignore`: Separate exclusion settings for Git and AI
    * `scratchpad.md`: AI's thought process and task log
* **Structured Directories**: Automatically separates `docs` (specifications), `src` (implementation), and `tests` (testing).

## 📦 Installation

To use this workflow, you need to place the file in Antigravity's **Global Workflows** directory.

### 1. Locate the Directory
Open the appropriate directory for your OS. Create the folder if it doesn't exist.

#### macOS / Linux
```bash
~/.gemini/antigravity/global_workflows/
```

#### Windows

```powershell
%USERPROFILE%\.gemini\antigravity\global_workflows\
```

### 2. Save the File

Download `setup-assistant.md` from this repository and save it to the directory above.

## 💻 Usage

1. Open a **new project (empty folder)** in Antigravity.
2. Enter the following command in the chat area (Agent):

> **"Run setup"** or **"Setup workflow"**

3. The AI will start up, scan the directory, and propose a setup. Answer the AI's questions (e.g., "Shall I create this?") to proceed.

## 📂 Generated Structure

After setup is complete, the following structure will be created:

```text
.
├── .agent/               <-- [AI Config] (Hidden folder)
│   ├── rules/            <-- Behavioral guidelines for AI
│   ├── workflows/        <-- Project-specific workflows
│   └── skills/           <-- Custom skills (MCP, etc.)
├── docs/                 <-- [Documentation]
│   └── design/
├── src/                  <-- [Source Code]
├── tests/                <-- [Test Code]
├── GEMINI.md             <-- [Project Definition]
├── scratchpad.md         <-- [AI Work Log]
├── .gitignore            <-- [Git Config]
└── .geminiignore         <-- [AI Exclusion Config]
```

## ⚠️ If the Hidden Folder (.agent) Is Not Visible

This workflow stores configuration files in a hidden folder called `.agent`. If it's not visible in your file explorer, follow the instructions below.

### macOS (Finder)

* Keyboard shortcut: Press **`Command` + `Shift` + `.` (dot)** to toggle hidden file visibility.

### Windows (File Explorer)

1. Click the **[View]** tab at the top of File Explorer.
2. Check the **[Hidden items]** checkbox.

### VS Code (Editor Settings)

Hidden folders are usually visible by default, but if `.agent` doesn't appear in the sidebar, check your `settings.json` and ensure the following setting is not excluding it:

```json
"files.exclude": {
    "**/.agent": false
}
```

## License

MIT License
