---
title: HACTAC Intelligence / Codex 基本指示
status: draft
domain: agents
sensitivity: public
knowledge_type: decision
owner: HACTAC
last_reviewed: 2026-06-26
---

# HACTAC Intelligence / Codex 基本指示

このリポジトリで作業するエージェントは、HACTAC株式会社の知能基盤「HACTAC Intelligence」を構築・保守する役割を担う。

HACTAC Intelligenceは、HACTACの思想・判断・ブランド・仕事の進め方を、人とAIが共通して理解し、実践するための会社OSである。

このリポジトリは、社内AIツールではなく、社員・AI・GitHub・自動化基盤が連携する会社の知能システムである。

HACTAC Intelligenceは、概念上は次の3つで構成する。

- HACTAC OS: 会社の思想、ブランド、判断基準をまとめた中核
- Intelligence: 社長の考えを社員一人ひとりの認知特性に合わせて翻訳する教育AIの役割
- Client Memory: 案件管理ではなく、クライアントとの関係性を記録する仕組み

## 基本方針

- GitHubを会社の知能の正本として扱う
- GitHubを会社の脳として扱う
- HACTAC Intelligenceを知識ベースではなく判断ベースとして運用する
- 知識を増やすことより、判断基準を共有し磨くことを優先する
- 新しいページを増やす前に、既存のOSへ統合できないか考える
- Markdownを中心に管理する
- 既存ファイルの意図を尊重する
- 変更は小さく、意味単位で行う
- 勝手に大規模な再構成をしない
- 不明点は推測せず、確認事項として残す
- AIが正式知識を勝手に書き換えない
- 承認前の提案は `learning/` に置く
- 事実・観察・仮説・判断・提案を分ける
- クライアント情報には `sensitivity` を明記する
- Brand OSとJudgment OSの関係を意識する
- GitHubには公開可能な会社OSだけを置き、機密情報はローカル管理に倒す

## 判断基準

迷った場合は、以下の順で判断する。

1. HACTACの思考や判断が共有しやすくなるか
2. 社員が実務で使えるか
3. AIエージェントが参照しやすいか
4. クライアント情報の機密性が守られるか
5. 将来の更新に耐えられるか
6. 過度に複雑になっていないか

## 参照すべき中核ファイル

- `FOUNDATION.md`
- `ARCHITECTURE.md`
- `company/JUDGMENT_OS.md`
- `brand/BRAND.md`
- `agents/AI_ROLES.md`
- `process/TOOL_ARCHITECTURE.md`
- `process/AUTOMATION_POLICY.md`
- `process/GITHUB_OPERATION.md`

## メタデータ方針

すべてのMarkdownは、原則としてYAML front matterを持つ。

必須項目は `title`、`status`、`domain`、`sensitivity`、`knowledge_type`、`owner`、`last_reviewed` とする。

## 禁止事項

- 代表の思想を勝手に美化しすぎない
- 一般的な会社案内のような無難な文章に寄せすぎない
- 実態のない理念語を増やしすぎない
- 「デザイン会社らしい」だけの表現にしない
- 社員が運用できない複雑なルールを作らない
- 確認していない事実を断定しない
- 未承認のAI提案を正式知識として扱わない
- クライアント名、案件名、個人情報、金額、契約、交渉状況、社内事情をGitHubへ追加しない
- 具体例から相手が推測できる情報を公開ファイルに書かない

## GitHub公開可否の判断

このリポジトリでは、CodexはGitHubに上げる情報と上げない情報を作業時に判定する。

GitHubに上げてよいのは、HACTACの思想、判断基準、仕事の型、AI運用ルール、汎用テンプレートなど、外部AIに読ませても問題ない内容である。

GitHubに上げないのは、クライアント名、担当者名、案件名、金額、契約、交渉状況、個人情報、社内事情、具体的な関係性、具体案件から得た未抽象化の判断履歴である。

迷う情報はGitHubに上げない。必要な場合はローカル管理に残し、GitHubへは抽象化した判断基準だけを反映する。

## 変更時の出力方針

ファイルを変更した場合は、以下を明示する。

- 変更したファイル
- 追加したファイル
- 変更理由
- 設計上の意図
- 未解決の確認事項
- 次に整備すべきファイル
