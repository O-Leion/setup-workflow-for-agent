# setup-workflow-for-agent

🌐 [English Version](./README_EN.md)

**AI Agent Workspace Setup Workflow Collection**

各種AIエージェントサービスを使用する際に必要となる特殊ファイル（設定ファイル、ルール定義、ワークフロー等）を自動構成するためのワークフロー集です。
新しいプロジェクトを始める際に、AIエージェントが最適に動作するワークスペース環境を対話形式で素早くセットアップできます。

## 📋 対応状況 (Supported AI Agents)

| AIエージェントサービス | ステータス | フォルダ                                 | 備考                                         |
| :--------------------- | :--------: | :--------------------------------------- | :------------------------------------------- |
| **Google Antigravity** |  ✅ 対応済  | [`for_antigravity/`](./for_antigravity/) | `.agent/` 構成によるエキスパートセットアップ |
| **GitHub Copilot**     |  🔲 未対応  | -                                        | `.github/copilot-instructions.md` 等         |
| **Cursor**             |  🔲 未対応  | -                                        | `.cursor/rules/` 等                          |
| **Windsurf (Codeium)** |  🔲 未対応  | -                                        | `.windsurfrules` 等                          |
| **Cline**              |  🔲 未対応  | -                                        | `.clinerules` 等                             |
| **Aider**              |  🔲 未対応  | -                                        | `.aider.conf.yml` 等                         |
| **Roo Code**           |  🔲 未対応  | -                                        | `.roo/rules/` 等                             |
| **Amazon Q Developer** |  🔲 未対応  | -                                        | -                                            |

> 💡 対応ワークフローは順次追加予定です。リクエストや貢献を歓迎します！

## 🚀 使い方

1. このリポジトリをクローンまたはダウンロードします。
2. 使用したいAIエージェントに対応するフォルダ（例: `for_antigravity/`）を開きます。
3. フォルダ内の `README.md` に従って、ワークフローファイルを所定の場所に配置します。
4. AIエージェント上でワークフローを実行し、対話形式でセットアップを進めます。

## 📂 リポジトリ構成

```text
.
├── README.md                 <-- このファイル
├── LICENSE
└── for_antigravity/          <-- Google Antigravity用ワークフロー
    ├── README.md             <-- 導入手順 (日本語)
    ├── README_EN.md          <-- 導入手順 (English)
    └── setup-assistant.md    <-- ワークフロー本体
```

## 🤝 コントリビューション

新しいAIエージェント用のワークフローを追加する場合は、以下の規則に従ってください：

1. `for_<サービス名>/` フォルダを作成する
2. フォルダ内に `README.md`（導入手順）と `ワークフローファイル` を配置する
3. このルート `README.md` の対応状況テーブルを更新する

## License

MIT License
