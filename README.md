# my-claude-config

Claude AIの設定を管理するパブリックリポジトリです。

## 概要

このリポジトリには、Claude AIと作業する際の個人的な設定、ガイドライン、プロンプトが含まれています。

## ファイル構成

- `CLAUDE.md` - Claude AIの主要な設定ファイル
- `.claude/agents/` - Claude Codeサブエージェント設定
- `.claude/commands/` - カスタムスラッシュコマンド

## サブエージェント

このリポジトリには、Claude Code用のカスタムサブエージェントが含まれています。

### 利用可能なサブエージェント

| 名前 | 説明 |
| --- | --- |
| `python-expert` | Python開発タスク（コーディング、デバッグ、テスト、パッケージ管理など） |
| `code-reviewer` | コードレビュー（PR、品質分析、セキュリティ監査、パフォーマンスチェック） |
| `api-designer` | REST/GraphQL API設計、OpenAPI仕様、認証パターン |
| `backend-developer` | サーバーサイド開発（Node.js、Python、Go）、マイクロサービス |
| `frontend-developer` | UI/UX開発（React、Vue、Angular）、アクセシビリティ |
| `typescript-pro` | TypeScript開発、型システム、フルスタック型安全性 |
| `python-pro` | Python 3.11+開発、型安全、非同期プログラミング、データサイエンス |
| `llm-architect` | LLMアーキテクチャ、RAG実装、ファインチューニング、プロンプトエンジニアリング |
| `scrum-master` | アジャイル手法、スクラム、チームファシリテーション、継続的改善 |
| `technical-writer` | 技術文書、API ドキュメント、ユーザーガイド |
| `architect-reviewer` | アーキテクチャレビュー、システム設計検証、技術的意思決定評価 |

### 全プロジェクトで利用する方法

サブエージェントを全プロジェクト横断で利用するには、グローバルディレクトリにコピーします：

```bash
# グローバルディレクトリを作成
mkdir -p ~/.claude/agents

# サブエージェントをコピー
cp .claude/agents/*.md ~/.claude/agents/
```

### 設定場所の違い

| パス                | スコープ               | 優先度 |
|---------------------|------------------------|--------|
| `.claude/agents/`   | 現在のプロジェクトのみ | 高     |
| `~/.claude/agents/` | 全プロジェクト共通     | 低     |

プロジェクト固有の設定がグローバル設定より優先されます。

### 参考リポジトリ

サブエージェントの作成には以下のリポジトリを参考にしました：

- [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) - 100以上の専門サブエージェントのコレクション

## カスタムコマンド

このリポジトリには、各サブエージェント用のスラッシュコマンドが含まれています。

### 利用可能なコマンド

| コマンド | 説明 |
| --- | --- |
| `/code-reviewer <PR URL>` | 指定したプルリクエストをcode-reviewerサブエージェントでレビュー |
| `/api-designer <要件>` | API設計またはレビュー（api-designerサブエージェント使用） |
| `/architect-reviewer <トピック>` | システムアーキテクチャレビュー（architect-reviewerサブエージェント使用） |
| `/backend-developer <タスク>` | バックエンド開発タスク実行（backend-developerサブエージェント使用） |
| `/frontend-developer <タスク>` | フロントエンド開発タスク実行（frontend-developerサブエージェント使用） |
| `/typescript-pro <タスク>` | TypeScript開発タスク実行（typescript-proサブエージェント使用） |
| `/python-pro <タスク>` | Python開発タスク実行（python-proサブエージェント使用） |
| `/llm-architect <要件>` | LLMシステム設計（llm-architectサブエージェント使用） |
| `/scrum-master <トピック>` | アジャイル/スクラムガイダンス（scrum-masterサブエージェント使用） |
| `/technical-writer <タスク>` | 技術文書作成（technical-writerサブエージェント使用） |

### 使用例

```bash
# PRレビュー
/code-reviewer https://github.com/owner/repo/pull/123

# API設計
/api-designer ユーザーAPI設計、ページネーション、認証に対応

# アーキテクチャレビュー
/architect-reviewer モノリシック構成からマイクロサービスへの移行戦略

# バックエンド開発
/backend-developer FastAPI を使用したユーザー認証エンドポイント実装

# フロントエンド開発
/frontend-developer React でダッシュボード画面実装、TypeScript使用

# TypeScript開発
/typescript-pro tRPC の型安全性を活かしたAPI実装

# Python開発
/python-pro 非同期 SQLAlchemy を使用したデータ処理パイプライン

# LLMアーキテクチャ
/llm-architect チャットボットシステム、RAG 搭載、低遅延要件

# スクラムガイダンス
/scrum-master チーム速度の低下、原因分析と改善策

# 技術文書
/technical-writer REST API のドキュメント作成、サンプルコード含む
```

### コマンドをグローバルに設定

```bash
mkdir -p ~/.claude/commands
cp .claude/commands/*.md ~/.claude/commands/
```

### コマンド設定場所の違い

| パス                  | スコープ               | 優先度 |
|-----------------------|------------------------|--------|
| `.claude/commands/`   | 現在のプロジェクトのみ | 高     |
| `~/.claude/commands/` | 全プロジェクト共通     | 低     |

プロジェクト固有の設定がグローバル設定より優先されます。

## 使い方

このリポジトリのCLAUDE.mdファイルをプロジェクトで参照することで、一貫したAI支援を受けることができます。

## ライセンス

MIT License

## 最終更新

2025-11-12
