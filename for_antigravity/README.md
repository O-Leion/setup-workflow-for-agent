# setup-workflow-4-Antigravity

🌐 [English Version](./README_EN.md)

**AI Agent Workspace Scaffolder for Google Antigravity**

Google Antigravity（AI-first IDE）において、AIエージェント開発に最適化されたワークスペース環境を自動構築するためのワークフローです。
「エキスパート構成（Expert Configuration）」と呼ばれる、設定ファイルを `.agent` フォルダに集約した高度なディレクトリ構成を、対話形式で安全にセットアップします。

## 🚀 特徴 (Features)

* **対話型セットアップ**: いきなりファイルを生成するのではなく、AIが現状を確認し、ユーザーの意図を汲みながらセットアップを進めます。
* **エキスパート構成の採用**: ルールやスキル定義を `.agent/` （隠しフォルダ）に集約し、ルートディレクトリをクリーンに保ちます。
* **ベストプラクティスの適用**:
    * `GEMINI.md`: プロジェクトのコンテキスト定義
    * `.gitignore` & `.geminiignore`: GitとAIそれぞれの除外設定
    * `scratchpad.md`: AIの思考・タスクログ保存用ファイル
* **ディレクトリ構造化**: `docs` (仕様), `src` (実装), `tests` (テスト) の分離を自動化。

## 📦 インストール方法 (Installation)

このワークフローを使用するには、Antigravityの **Global Workflows** ディレクトリにファイルを配置する必要があります。

### 1. ディレクトリの確認
お使いのOSに合わせて、以下のディレクトリを開いてください。もしフォルダが存在しない場合は作成してください。

#### macOS / Linux
```bash
~/.gemini/antigravity/global_workflows/
```

#### Windows

```powershell
%USERPROFILE%\.gemini\antigravity\global_workflows\
```

### 2. ファイルの保存

本リポジトリの `setup-assistant.md` をダウンロードし、上記のディレクトリに保存してください。

## 💻 使い方 (Usage)

1. Antigravityで **新規プロジェクト（空のフォルダ）** を開きます。
2. チャットエリア（Agent）で以下のコマンドを入力・送信してください。

> **「セットアップを実行」** または **「Setup workflow」**

3. AIが起動し、ディレクトリ内をスキャンした上でセットアップの提案を行います。AIの質問（「作成しますか？」など）に答えて進めてください。

## 📂 生成される構成 (Directory Structure)

セットアップ完了後、以下の構成が作成されます。

```text
.
├── .agent/               <-- [AI設定] (隠しフォルダ)
│   ├── rules/            <-- AIへの行動指針
│   ├── workflows/        <-- プロジェクト固有ワークフロー
│   └── skills/           <-- カスタムスキル (MCP等)
├── docs/                 <-- [ドキュメント]
│   └── design/
├── src/                  <-- [ソースコード]
├── tests/                <-- [テストコード]
├── GEMINI.md             <-- [プロジェクト定義書]
├── scratchpad.md         <-- [AI作業ログ]
├── .gitignore            <-- [Git設定]
└── .geminiignore         <-- [AI除外設定]
```

## ⚠️ 隠しフォルダ (.agent) が見えない場合

本ワークフローは設定ファイルを `.agent` という隠しフォルダに格納します。エクスプローラーやFinderで見えない場合は、以下の設定を行ってください。

### macOS (Finder)

* キーボードショートカット: **`Command` + `Shift` + `.` (ドット)** を押すと、表示/非表示が切り替わります。

### Windows (エクスプローラー)

1. エクスプローラー上部の **[表示]** タブをクリックします。
2. **[隠しファイル]** のチェックボックスをオンにしてください。

### VS Code (エディタ設定)

通常は表示されますが、もしサイドバーに表示されない場合は `settings.json` を確認し、以下の設定を除外してください。

```json
"files.exclude": {
    "**/.agent": false
}
```

## License

MIT License
