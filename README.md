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

### 利用可能なコマンド

| コマンド | 説明 |
| --- | --- |
| `/code-reviewer <PR URL>` | 指定したプルリクエストをcode-reviewerサブエージェントでレビュー |

### 使用例

```bash
/code-reviewer https://github.com/owner/repo/pull/123
```

### コマンドをグローバルに設定

```bash
mkdir -p ~/.claude/commands
cp .claude/commands/*.md ~/.claude/commands/
```

## 使い方

このリポジトリのCLAUDE.mdファイルをプロジェクトで参照することで、一貫したAI支援を受けることができます。

## ライセンス

MIT License

## 最終更新

2025-11-12
