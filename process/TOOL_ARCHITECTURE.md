---
title: Tool Architecture
status: draft
domain: process
sensitivity: public
knowledge_type: decision
owner: HACTAC
last_reviewed: 2026-06-26
---

# Tool Architecture

このファイルは、HACTAC Intelligenceを支えるツールの役割分担を整理する文書である。

HACTAC Intelligenceは、AI単体ではなく、社員、社長、GitHub、Codex、ChatGPT、n8n、NASが連携する会社の知能システムである。

## 基本構成

- ChatGPT: 思考の壁打ち、Brand OS、Judgment OS、意思決定支援
- Codex: GitHub更新、コード修正、実装支援、ドキュメント整備
- GitHub: 会社知識と判断基準の正本
- n8n: 定型業務の自動実行基盤
- NAS: n8nなどのセルフホスト基盤
- 社員: 判断、共感、対人対応、最終確認
- 社長: 思想の源泉、最終的な方向づけ

## GitHub

GitHubは、HACTACの会社の脳として扱う。

置けるものは可能な限りGitHubに集約する。ただし、単なる情報置き場ではなく、判断基準、思想、業務プロセス、テンプレート、失敗事例、運用ルールを整理して蓄積する。

重要なのは、知識ベースではなく判断ベースとして運用することである。

## n8n と NAS

n8nは、定型業務の自動実行基盤である。

n8nはすでにNAS上にセルフホスト済みであり、必要になればいつでも運用開始できる状態にある。

ただし、現時点では無理に自動化を進めない。業務が整理され、反復処理や確認漏れのリスクが見えた段階で活用する。

## Codex

Codexは、GitHub上の正本を更新する実装・編集エージェントである。

文書整備、コード修正、テンプレート作成、運用ルールの反映を担う。ただし、正式知識の意味を変える変更は、CEO確認または明示指示を前提とする。

## ChatGPT

ChatGPTは、思考の壁打ち、Brand OS、Judgment OS、意思決定支援を担う。

社員に対しては、答えを渡すだけでなく、HACTACの判断基準を説明し、自立思考を支援する。

## 関連ファイル

- `process/GITHUB_OPERATION.md`
- `process/AUTOMATION_POLICY.md`
- `agents/AI_ROLES.md`
- `agents/CODEX.md`
- `agents/CHATGPT.md`

## 要確認

- n8nで最初に自動化する業務
- NAS上の運用ルール
- GitHubとn8nの連携方法
