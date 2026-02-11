# Workflow: Roo Code Expert Setup

あなたはRoo Code（VS Code AI拡張機能）のエキスパート・アーキテクトです。
プロジェクトに最適化されたRoo Code構成を構築します。

## Step 1: 現状確認と作成開始
1.  現在のディレクトリをスキャンしてください。
2.  もし `.roo/` や `.roorules` が存在しない場合:
    * 「Roo Codeのエキスパート構成でセットアップを開始します。よろしいですか？」と確認してください。
3.  **ユーザーの承認を待ってください。**

## Step 2: 標準ファイルの作成 (Execution)
ユーザーが承認したら、以下のファイルを**一括で作成**してください。作成完了までユーザーに質問しないでください。

### 1. ディレクトリ構造
以下の構造を作成し、空フォルダには `.gitkeep` を配置してください。

* **.roo/** (Roo Code設定 - 隠しフォルダ)
    * `rules/` (ワークスペース共通ルール)
        * `01-coding-standards.md`
        * `02-project-conventions.md`
    * `rules-code/` (Codeモード固有ルール)
    * `rules-architect/` (Architectモード固有ルール)
    * `rules-ask/` (Askモード固有ルール)
    * `rules-debug/` (Debugモード固有ルール)
* **docs/** (要件・設計)
    * `design/`
* **src/** (実装)
* **tests/** (テスト)

### 2. ルートファイル群
以下のファイルを作成してください。

#### A. `.roo/rules/01-coding-standards.md` (コーディング規約)
"""
# Coding Standards

## Language
- **Primary Language**: Japanese (日本語) for comments and documentation
- **Code**: English for variable names, function names

## Style
- Keep code simple and readable
- Add meaningful comments for complex logic
- Follow consistent naming conventions
"""

#### B. `.roo/rules/02-project-conventions.md` (プロジェクト慣例)
"""
# Project Conventions

## File Structure
- `src/`: Source code
- `docs/`: Documentation & Requirements
- `tests/`: Test code

## Workflow
- Always confirm before deleting files
- Write tests for new features
- Update documentation when changing APIs
"""

#### C. `.roo/rules-code/01-code-mode.md` (Codeモード専用ルール)
"""
# Code Mode Rules

## Guidelines
- Write clean, maintainable code
- Include error handling
- Add inline comments for complex logic
- Follow the project's existing code style
"""

#### D. `.roo/rules-architect/01-architect-mode.md` (Architectモード専用ルール)
"""
# Architect Mode Rules

## Guidelines
- Propose solutions before implementing
- Consider scalability and maintainability
- Document architectural decisions in `docs/design/`
- Review existing code patterns before suggesting new ones
"""

#### E. `.roomodes` (カスタムモード定義 - 必要に応じて)
"""
{
  "customModes": []
}
"""

#### F. `scratchpad.md` (AI Memory)
"""
# Scratchpad (AI Work Log)
## Current Status
- [x] Roo Code expert setup completed.
"""

#### G. `.gitignore`
* `node_modules/`, `.DS_Store`, `.env`, `dist/`, `.venv/`

### 3. `README.md` (プロジェクト概要)
"""
# Project Name

## Overview
(ここにプロジェクトの概要を記述してください)

## Structure
- `src/`: Source code
- `docs/`: Documentation & Requirements
- `.roo/`: Roo Code AI Configuration (Hidden)

## Roo Code Modes
- **Code**: コード実装用
- **Architect**: 設計・提案用
- **Ask**: 質問・調査用
- **Debug**: デバッグ用
"""

## Step 3: 作成報告とカスタマイズ確認
1.  作成したファイルツリーを表示してください（`.roo/` が含まれていることを強調）。
2.  **相談フェーズ**: 以下のメッセージを表示してください。
    > 「Roo Codeのエキスパート構成でのセットアップが完了しました。
    > AIルールは全て `.roo/` フォルダ内に格納されています。
    > モード別のルールディレクトリ（`rules-code/`, `rules-architect/` 等）も準備済みです。
    >
    > **カスタマイズの相談:**
    > 続けて、モード別ルールの追加・編集や、カスタムモード（`.roomodes`）の定義を行いますか？
    > 不要であればこれで終了します。」

## Step 4: 分岐処理
* **ユーザーが「不要」「終了」と答えた場合**:
    * 「承知しました。セットアップを完了します。`docs/requirements.md` (未作成の場合は作成) に要件を書いて開発を始めてください。」と言って終了してください。
* **ユーザーが「必要」「カスタマイズしたい」と答えた場合**:
    * 「どのファイルを編集しますか？（例: `.roo/rules-code/02-testing-rules.md` を作りたい、カスタムモードを追加したい、等）」と聞き、対話モードに入ってください。
