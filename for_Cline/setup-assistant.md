# Workflow: Cline Expert Setup

あなたはCline（VS Code AI拡張機能）のエキスパート・アーキテクトです。
プロジェクトに最適化されたCline構成を構築します。

## Step 1: 現状確認と作成開始
1.  現在のディレクトリをスキャンしてください。
2.  もし `.clinerules` や `.clineignore` が存在しない場合:
    * 「Clineのエキスパート構成でセットアップを開始します。よろしいですか？」と確認してください。
3.  **ユーザーの承認を待ってください。**

## Step 2: 標準ファイルの作成 (Execution)
ユーザーが承認したら、以下のファイルを**一括で作成**してください。作成完了までユーザーに質問しないでください。

### 1. ディレクトリ構造
以下の構造を作成し、空フォルダには `.gitkeep` を配置してください。

* **.clinerules/** (Clineルール設定)
    * `01-coding-standards.md` (コーディング規約)
    * `02-project-conventions.md` (プロジェクト慣例)
* **docs/** (要件・設計)
    * `design/`
* **src/** (実装)
* **tests/** (テスト)

### 2. ルートファイル群
以下のファイルを作成してください。

#### A. `.clinerules/01-coding-standards.md` (コーディング規約)
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

#### B. `.clinerules/02-project-conventions.md` (プロジェクト慣例)
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

#### C. `.clineignore` (AI除外設定)
"""
# Dependencies
node_modules/

# Build outputs
dist/
build/

# Version control
.git/

# Environment
.env
.env.local

# OS files
.DS_Store
Thumbs.db

# Python
.venv/
__pycache__/
"""

#### D. `scratchpad.md` (AI Memory)
"""
# Scratchpad (AI Work Log)
## Current Status
- [x] Cline expert setup completed.
"""

#### E. `.gitignore`
* `node_modules/`, `.DS_Store`, `.env`, `dist/`, `.venv/`

### 3. `README.md` (プロジェクト概要)
"""
# Project Name

## Overview
(ここにプロジェクトの概要を記述してください)

## Structure
- `src/`: Source code
- `docs/`: Documentation & Requirements
- `.clinerules/`: Cline AI rules & configuration
"""

## Step 3: 作成報告とカスタマイズ確認
1.  作成したファイルツリーを表示してください（`.clinerules/` が含まれていることを強調）。
2.  **相談フェーズ**: 以下のメッセージを表示してください。
    > 「Clineのエキスパート構成でのセットアップが完了しました。
    > AIルールは全て `.clinerules/` フォルダ内に格納されています。
    >
    > **カスタマイズの相談:**
    > 続けて、コーディングルールの追加・編集や、MCP (Model Context Protocol) ツール連携の設定を行いますか？
    > 不要であればこれで終了します。」

## Step 4: 分岐処理
* **ユーザーが「不要」「終了」と答えた場合**:
    * 「承知しました。セットアップを完了します。`docs/requirements.md` (未作成の場合は作成) に要件を書いて開発を始めてください。」と言って終了してください。
* **ユーザーが「必要」「カスタマイズしたい」と答えた場合**:
    * 「どのファイルを編集しますか？（例: `.clinerules/03-api-guidelines.md` を作りたい、等）」と聞き、対話モードに入ってください。
