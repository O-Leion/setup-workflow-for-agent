# setup-workflow-for-agent

🌐 [日本語版 (Japanese)](./README.md)

**AI Agent Workspace Setup Workflow Collection**

A collection of workflows for automatically configuring the special files (configuration files, rule definitions, workflows, etc.) required when using various AI agent services.
Quickly set up an optimized workspace environment for AI agents through an interactive process when starting a new project.

## 📋 Supported AI Agents

| AI Agent Service       |   Status    | Folder                                   | Notes                                     |
| :--------------------- | :---------: | :--------------------------------------- | :---------------------------------------- |
| **Google Antigravity** | ✅ Supported | [`for_antigravity/`](./for_antigravity/) | Expert setup with `.agent/` configuration |
| **GitHub Copilot**     |  🔲 Planned  | -                                        | `.github/copilot-instructions.md`, etc.   |
| **Cursor**             |  🔲 Planned  | -                                        | `.cursor/rules/`, etc.                    |
| **Windsurf (Codeium)** |  🔲 Planned  | -                                        | `.windsurfrules`, etc.                    |
| **Cline**              | ✅ Supported | [`for_Cline/`](./for_Cline/)             | `.clinerules/` rule management            |
| **Aider**              |  🔲 Planned  | -                                        | `.aider.conf.yml`, etc.                   |
| **Roo Code**           | ✅ Supported | [`for_RooCode/`](./for_RooCode/)         | `.roo/rules/` mode-specific rules         |
| **Amazon Q Developer** |  🔲 Planned  | -                                        | -                                         |

> 💡 Workflows for additional agents will be added over time. Requests and contributions are welcome!

## 🚀 Usage

1. Clone or download this repository.
2. Open the folder corresponding to the AI agent you want to use (e.g., `for_antigravity/`).
3. Follow the `README.md` inside the folder to place the workflow file in the appropriate location.
4. Run the workflow in your AI agent and proceed with the interactive setup.

## 📂 Repository Structure

```text
.
├── README.md                 <-- Main file (Japanese)
├── README_EN.md              <-- English version
├── LICENSE
├── for_antigravity/          <-- Google Antigravity
│   ├── README.md / README_EN.md
│   └── setup-assistant.md
├── for_Cline/                <-- Cline
│   ├── README.md / README_EN.md
│   └── setup-assistant.md
└── for_RooCode/              <-- Roo Code
    ├── README.md / README_EN.md
    └── setup-assistant.md
```

## 🤝 Contributing

When adding a workflow for a new AI agent, please follow these conventions:

1. Create a `for_<service_name>/` folder
2. Place a `README.md` (setup guide) and the workflow file inside the folder
3. Update the support status table in this root `README.md`

## License

MIT License
