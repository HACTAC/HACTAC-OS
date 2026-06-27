---
title: HACTAC Intelligence
status: draft
domain: foundation
sensitivity: public
knowledge_type: decision
owner: HACTAC
last_reviewed: 2026-06-26
---

# HACTAC Intelligence

HACTAC Intelligenceは、HACTAC株式会社の思想・判断・ブランド・仕事の進め方を、人とAIが共通して理解し、実践するための会社OSである。

このリポジトリは、単なる社内AIツール、社内OS、ナレッジベースではない。HACTACが何を大切にし、どのように考え、どのように判断し、どのように顧客と向き合い、どのように学習するかを管理する正本である。

GitHub上のこのリポジトリを、会社の脳であり、会社の知能の正本として扱う。

ただし、現時点ではGitHubに置く範囲を「外部AIにも読ませられる会社OS」に限定する。クライアント名、個人情報、金額、社内事情、具体案件情報などはGitHubへ上げず、ローカル管理とする。

## 現時点の定義

HACTAC Intelligenceは完成物ではなく、実務の中で更新される会社の知能基盤である。

目的は知識を増やすことではなく、判断基準を共有することである。

正式知識は、確認済みの事実、観察、仮説、判断を区別して記録する。AIが提案した内容は、承認前に正式ファイルへ直接混ぜず、原則として `learning/` に蓄積する。

## 成功状態

HACTAC Intelligenceの成功状態は、社員全員が同じ判断基準で動けること、社長がいなくても一定水準で会社が回ることである。

新人を無理にベテラン化することは目的ではない。重要なのは、判断基準、考え方、問いの立て方を共有することである。

## v1.0 の基本構成

HACTAC Intelligenceは、概念上は次の3つで構成する。

- HACTAC OS: 会社の思想、ブランド、判断基準をまとめた中核
- Intelligence: 社長の考えを、社員一人ひとりの認知特性に合わせて翻訳する教育AIの役割
- Client Memory: 案件管理ではなく、クライアントとの関係性を記録する仕組み

実装上のディレクトリは、この3構成を運用するための置き場所として扱う。

- `foundation/` または `FOUNDATION.md`: 思想・目的
- `founder/`: 代表の思考・判断
- `company/`: HACTACの会社知
- `brand/`: ブランド知
- `clients/`: クライアント知
- `projects/`: 案件知
- `relationship/`: 関係知
- `design/`: デザイン制作知
- `process/`: 業務プロセス
- `agents/`: AIエージェント
- `learning/`: 承認前の学習提案
- `templates/`: 各種テンプレート
- `knowledge/`: 技術・業界知識

## GitHubに置く情報と置かない情報

このリポジトリは、ChatGPT、Codex、将来のAIエージェントが共通参照できる公開可能な会社OSとして整備する。

GitHubに置く情報は、HACTACの思想、判断基準、仕事の型、AI運用ルール、汎用テンプレートなど、クライアントや個人を特定しない情報に限定する。

GitHubに置かない情報は、クライアント名、担当者名、案件名、金額、契約、交渉状況、個人情報、社内事情、具体的な関係性、具体案件から得た未抽象化の判断履歴である。

迷った場合はGitHubに上げず、ローカル管理に倒す。ローカル管理した情報をGitHubへ反映する場合は、具体情報を削り、判断基準や仕事の型として抽象化してから反映する。

`clients/`、`projects/`、`relationship/` は、今後具体情報が入りやすいため、GitHubでは原則管理しない。必要な場合は、公開可能な考え方だけを `company/`、`process/`、`design/`、`learning/` などへ抽象化して記録する。

## 共通メタデータ方針

すべてのMarkdownは、原則として先頭にYAML front matterを置く。

```yaml
---
title: 文書タイトル
status: draft | proposed | approved | archived
domain: foundation | founder | company | brand | clients | projects | relationship | process | agents | learning | templates | knowledge
sensitivity: public | internal | confidential | restricted
knowledge_type: fact | observation | hypothesis | decision | proposal | mixed
owner: HACTAC
last_reviewed: YYYY-MM-DD
---
```

`status` は文書の確からしさを示す。`learning/` の内容は原則 `proposed` とし、承認後に正式ファイルへ反映する。

`sensitivity` は情報の機密性を示す。特に `clients/` は原則 `confidential` 以上とし、外部共有前に必ず確認する。

`knowledge_type` は、事実・観察・仮説・判断・提案を混同しないために使う。複数が混在する場合は `mixed` とし、本文内でも区別する。

## 運用方法

変更は小さく、意味単位で行う。

不明点は推測で補わず、各ファイルの `要確認` に残す。AIは正式知識を勝手に書き換えず、判断が必要な内容は `learning/` に提案として記録する。

新しいページを追加する前に、既存のOSへ統合できないかを確認する。統合できる場合は、ページを増やさず既存ファイルを磨く。

## 最初に整備するファイル

- `FOUNDATION.md`
- `ARCHITECTURE.md`
- `company/COMPANY.md`
- `company/THINKING.md`
- `company/DECISION.md`
- `agents/CODEX.md`
- `agents/CHATGPT.md`
- `agents/AI_ROLES.md`
- `company/JUDGMENT_OS.md`
- `process/TOOL_ARCHITECTURE.md`
- `process/AUTOMATION_POLICY.md`
- `process/WORKFLOW.md`
- `clients/README.md`
- `learning/README.md`

## 要確認

- 正式なミッション、ビジョン、バリューの有無
- クライアント情報の機密区分
- AIが正式知識へ反映してよい範囲
- `learning/` の承認フロー
- GitHub運用、ブランチ、レビュー、コミットのルール
