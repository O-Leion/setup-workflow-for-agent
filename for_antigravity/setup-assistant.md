# Workflow: Antigravity Expert Setup

あなたはAntigravityのエキスパート・アーキテクトです。
「.agentフォルダを使用した高度な構成」を構築します。

## Step 1: 現状確認と作成開始
1.  現在のディレクトリをスキャンしてください。
2.  もし `GEMINI.md` や `.agent/` が存在しない場合:
    * 「エキスパート構成（.agentフォルダ仕様）でセットアップを開始します。よろしいですか？」と確認してください。
3.  **ユーザーの承認を待ってください。**

## Step 2: 標準ファイルの作成 (Execution)
ユーザーが承認したら、以下のファイルを**一括で作成**してください。作成完了までユーザーに質問しないでください。

### 1. ディレクトリ構造 (.agent構成)
以下の構造を作成し、空フォルダには `.gitkeep` を配置してください。

* **.agent/** (Antigravity設定 - 隠しフォルダ)
    * `rules/`
    * `workflows/`
    * `skills/`
        * `TemplateSkill/`
* **docs/** (要件・設計)
    * `design/`
* **src/** (実装)
* **tests/** (テスト)

### 2. ルートファイル群
以下のファイルを作成してください。

#### A. `GEMINI.md` (Project Context)
"""
# Project Context

## Overview
(プロジェクト概要を記述)

## Configuration
このプロジェクトは **Expert Configuration** を採用しています。
- **Rules**: `./.agent/rules/`
- **Skills**: `./.agent/skills/` (See `./.agent/skills/README.md`)
- **Workflows**: `./.agent/workflows/`

## Guidelines
- **Language**: Japanese (日本語)
- **Code Style**: Simple & Readable.
"""

#### B. `scratchpad.md` (AI Memory)
"""
# Scratchpad (AI Work Log)
## Current Status
- [x] Expert setup completed.
"""

#### C. `.gitignore` & `.geminiignore`
* `.gitignore`: `node_modules/`, `.DS_Store`, `.env`, `dist/`, `.venv/`
* `.geminiignore`: `.git/`, `node_modules/`, `dist/`

### 3. `README.md` (プロジェクト概要)
"""
# Project Name

## Overview
(ここにプロジェクトの概要を記述してください)

## Structure
- `src/`: Source code
- `docs/`: Documentation & Requirements
- `.agent/`: AI Configuration (Hidden)
"""

### 4. `.agent/skills/README.md`
"""
# Skills Directory
このディレクトリ (`.agent/skills/`) はAIスキルの格納場所です。
1スキル = 1フォルダの構成を守ってください。
"""

## Step 3: 作成報告とカスタマイズ確認
1.  作成したファイルツリーを表示してください（`.agent` が含まれていることを強調）。
2.  **相談フェーズ**: 以下のメッセージを表示してください。
    > 「エキスパート構成でのセットアップが完了しました。
    > AI設定は全て `.agent/` フォルダ内に格納されています。
    >
    > **カスタマイズの相談:**
    > 続けて、`GEMINI.md` に技術スタック（Python/Node.js等）を追記したり、初期ルールを `.agent/rules/` に作成しますか？
    > 不要であればこれで終了します。」

## Step 4: 分岐処理
* **ユーザーが「不要」「終了」と答えた場合**:
    * 「承知しました。セットアップを完了します。`docs/requirements.md` (未作成の場合は作成) に要件を書いて開発を始めてください。」と言って終了してください。
* **ユーザーが「必要」「カスタマイズしたい」と答えた場合**:
    * 「どのファイルを編集しますか？（例: `.agent/rules/coding-style.md` を作りたい、等）」と聞き、対話モードに入ってください。