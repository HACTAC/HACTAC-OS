---
title: GitHub Operation
status: draft
domain: process
sensitivity: public
knowledge_type: decision
owner: HACTAC
last_reviewed: 2026-06-26
---

# GitHub Operation

このファイルは、HACTAC IntelligenceをGitHubで管理するための運用方針を定義する文書である。

GitHubは、HACTAC Intelligenceにおける正式知識の正本である。

ただし、現時点ではGitHubに置く正式知識を「外部AIにも読ませられる会社OS」に限定する。クライアント情報、案件情報、個人情報、金額、社内事情はGitHubの管理対象から外し、ローカルで管理する。

## GitHubを正本として扱う方針

正式知識、承認済みの判断基準、テンプレート、AIエージェント指示はGitHub上のMarkdownを正本とする。

口頭、チャット、メモアプリ、ローカルファイルにある情報は、GitHubへ反映されるまでは正式知識ではなく、参照情報または提案として扱う。

GitHubは、HACTACの会社の脳として扱う。

置けるものは可能な限りGitHubに集約する。ただし、単なる情報置き場ではなく、判断基準、思想、業務プロセス、テンプレート、失敗事例、運用ルールを整理して蓄積する。

重要なのは、知識ベースではなく判断ベースとして運用することである。

## GitHubに置く情報

- Brand OS
- Judgment OS
- 業務フロー
- 提案書テンプレート
- デザイン判断基準
- コーディングルール
- 営業・顧客対応の考え方
- 失敗事例
- n8n等の自動化運用方針
- Codex運用方針
- AI活用ルール

## GitHubに置かない情報

以下はGitHubに置かず、ローカル管理とする。

- クライアント名、担当者名、個人名
- 案件名、具体案件の進行状況
- 見積金額、予算感、請求、契約、交渉状況
- 社内メンバーの評価、認知特性、個別指導内容
- クライアントとの関係性、金銭感覚、注意すべき表現
- 具体例から相手を推測できる失敗事例や判断履歴
- Slack、Asana、n8n、GitHubなどの内部URLや権限情報

迷った場合はGitHubに上げない。GitHubへ反映する場合は、具体情報を除き、判断基準、仕事の型、汎用テンプレートとして抽象化する。

## ローカル管理する領域

`clients/`、`projects/`、`relationship/`、クライアントプロファイルは、今後具体情報が入りやすいためローカル管理を基本とする。

これらの領域から得た学びをGitHubへ反映する場合は、実名、金額、案件名、関係性を削り、`company/`、`process/`、`design/`、`learning/` のいずれかに抽象化して記録する。

## ブランチ運用

現時点では、小さな変更は作業ブランチで行い、Pull Requestで確認してから反映する方針を基本とする。

推奨ブランチ名:

- `docs/foundation-update`
- `docs/client-template`
- `learning/proposal-YYYYMMDD-title`
- `process/github-operation`

緊急性の低い設計変更や複数ファイルに影響する変更は、必ず作業ブランチを分ける。

## コミットメッセージ方針

コミットメッセージは、何を変えたかが分かる短い日本語または英語で記載する。

例:

- `docs: HACTAC Intelligenceの承認フローを追加`
- `templates: クライアントプロファイル雛形を追加`
- `process: GitHub運用方針を追加`

## Pull Requestの扱い

Pull Requestでは、以下を明記する。

- 変更したファイル
- 変更理由
- 設計上の意図
- 影響範囲
- CEO確認が必要な点
- 未整理の論点

## Codexが直接変更してよい範囲

Codexは、以下を直接変更してよい。

- ユーザーが明示した内容の反映
- 誤字脱字、表記ゆれ、見出し構造の整理
- テンプレートの追加
- `learning/` への承認前提案の作成
- 承認済み提案の正式ファイルへの反映

## CEO確認が必要な変更

以下はCEO確認を必須とする。

- 会社の思想、目的、価値観に関する変更
- 代表の思考や判断の定義
- クライアント理解、関係性、金銭感覚に関する記述
- AIエージェントの権限変更
- GitHub運用や承認フローの変更
- 外部公開される可能性がある文章

## 機密情報を扱う場合の注意

クライアント情報、金額、交渉状況、個人情報、関係性に関する情報は、必ず `sensitivity` を確認する。

`confidential` または `restricted` の情報を扱う場合は、公開リポジトリ、外部共有、生成AIへの入力可否を確認する。

公開リポジトリで扱えるのは、原則として `sensitivity: public` の文書のみとする。`internal`、`confidential`、`restricted` は、公開前に内容を確認し、必要に応じて公開版として書き換える。

## 要確認

- `main` ブランチを正式正本とするか
- Pull Requestレビューの必須化
- Issueで学習提案や承認履歴を管理するか
- private repository運用の確認
