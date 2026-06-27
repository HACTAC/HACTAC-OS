---
title: ARCHITECTURE
status: draft
domain: foundation
sensitivity: public
knowledge_type: decision
owner: HACTAC
last_reviewed: 2026-06-26
---

# ARCHITECTURE

このファイルは、HACTAC Intelligenceの情報構造と運用構造を整理する文書である。

どこに何を置くかだけでなく、正式知識、承認前提案、案件知、クライアント知をどう分けるかを定義する。

## 概念構造

HACTAC Intelligenceは、概念上は次の3つのみで構成する。

1. HACTAC OS
2. Intelligence
3. Client Memory

この3つはディレクトリ名ではなく、会社の知能システムを整理するための上位構造である。

## HACTAC OS

HACTAC OSは、会社の思想、ブランド、判断基準をまとめた中核である。

ブランドブックであり、教育教材であり、AIの判断基準でもある。

扱う内容は、Identity、Philosophy、Brand、Approach、Decisionを中心とする。

`FOUNDATION.md`、`company/`、`brand/`、`design/`、`process/` は、HACTAC OSを構成する実装領域として扱う。

## Intelligence

Intelligenceは、ドキュメントではなくAIの役割である。

目的は、社長の考えを、社員一人ひとりの認知特性に合わせて翻訳することである。

AIは理解度を推測し、抽象論だけで説明せず、具体例を使い、答えだけを渡さず、問いを返す。最後はHACTAC OSへ戻る。

`agents/` は、この役割を実行するAIエージェントの方針を管理する実装領域である。

## Client Memory

Client Memoryは、案件管理ではない。

クライアントとの関係性を記録し、誰が担当してもその会社らしい対応ができる状態をつくるための仕組みである。

扱う内容は、会社概要、ブランドの背景、担当者の考え方、価値観、提案履歴、成功例、失敗例、注意点を中心とする。

`clients/`、`projects/`、`relationship/` は、Client Memoryを支える実装領域として扱う。

## 実装構造

- `FOUNDATION.md`: 思想・目的・基本原則
- `ARCHITECTURE.md`: 情報構造と運用構造
- `founder/`: 代表の思考・判断
- `company/`: HACTACの会社知
- `brand/`: ブランド知、Brand OS
- `clients/`: クライアント知
- `projects/`: 案件知
- `relationship/`: 関係知
- `design/`: デザイン制作知
- `process/`: 業務プロセス
- `agents/`: AIエージェントの役割と指示
- `learning/`: 承認前の学習提案
- `templates/`: 各種テンプレート
- `knowledge/`: 技術・業界知識

## `founder/` と `company/` の境界

`founder/` は、代表個人の思考、問いの立て方、判断の癖、価値観の源泉を扱う。

`company/` は、HACTACとして社員やAIエージェントが共有すべき会社知、判断基準、意思決定ルールを扱う。

代表の個人的な思考をそのまま会社の正式基準にしない。会社として採用する場合は、`learning/` で提案化し、承認後に `company/` へ反映する。

`company/JUDGMENT_OS.md` は、代表の思想を会社として参照できる判断基準へ翻訳する中心ファイルである。

## Brand OS と Judgment OS

Brand OSは、HACTACらしさ、価値観、世界観、言葉遣い、体験設計を扱う。

Judgment OSは、日々の判断、問いの立て方、意思決定の癖、優先順位づけを扱う。

Brand OSは「どう見られ、どう伝わるか」を支え、Judgment OSは「どう考え、どう決めるか」を支える。

両者は分離するが、矛盾させない。判断に迷った場合は、Judgment OSで選択肢を整理し、Brand OSとの整合性を確認する。

## 正式知識と学習提案

正式知識は、承認済みの判断や確認済みの情報を記録する場所に置く。

AIが作成した新しい解釈、改善案、分類案、ルール案は、まず `learning/` に提案として置く。承認後、該当する正式ファイルへ反映する。

## `learning/` と正式知識の境界

`learning/` は、承認前の学び、改善案、仮説、運用変更案を置く場所である。

正式知識は、`company/`、`brand/`、`clients/`、`projects/`、`relationship/`、`process/`、`agents/`、`knowledge/` など、該当する領域に置く。

AIは未承認の提案を正式知識へ直接混ぜない。正式ファイルへ反映するには、提案、根拠、影響範囲、承認状態が確認できる必要がある。

## クライアント知の扱い

`clients/` は機密性が高い情報を扱う領域である。

クライアントごとの事実、観察、仮説、関係性、提案履歴、案件知を混同しないように整理する。外部共有可能な内容と社内限定の内容は分ける。

## `clients/` と `relationship/` の境界

`clients/` は、クライアント単位の理解を扱う。会社情報、事業構造、意思決定傾向、金銭感覚、提案方針、注意すべき表現などを記録する。

`relationship/` は、個別クライアントをまたぐ関係性、協力会社、地域、コミュニティ、紹介経路、継続的な接点を扱う。

特定クライアントに閉じる情報は `clients/` に置く。複数の案件や人間関係にまたがる情報は `relationship/` に置く。

## `design/` を独立領域として残す理由

`design/` は、HACTACの中核業務であるデザイン制作の判断基準を扱うため、独立領域として残す。

`brand/` はHACTAC自身のブランド知、`process/` は業務の進め方、`knowledge/` は技術・業界知識を扱う。一方で `design/` は、制作物の品質、情報設計、レビュー観点、表現判断など、実務上のデザイン判断を蓄積する場所である。

将来的に内容が増えた場合は、`design/web/`、`design/vi/`、`design/proposal/` のように分ける。

## AI・GitHub・自動化基盤の関係

HACTAC Intelligenceは、AI単体ではなく、社員、社長、GitHub、ChatGPT、Codex、n8n、NASが連携する会社の知能システムである。

- ChatGPT: 思考の壁打ち、Brand OS、Judgment OS、意思決定支援
- Codex: GitHub更新、コード修正、実装支援、ドキュメント整備
- GitHub: 会社知識と判断基準の正本
- n8n: 定型業務の自動実行基盤
- NAS: n8nなどのセルフホスト基盤
- 社員: 判断、共感、対人対応、最終確認
- 社長: 思想の源泉、最終的な方向づけ

詳細は `agents/AI_ROLES.md`、`process/TOOL_ARCHITECTURE.md`、`process/AUTOMATION_POLICY.md` を参照する。

## 事実・観察・仮説・判断・提案の書き分け

- 事実: 確認済みの情報。出典や確認日をできるだけ明記する。
- 観察: 対話、案件、制作過程から見えた傾向。断定しない。
- 仮説: 検証前の解釈や可能性。必ず仮説と明記する。
- 判断: HACTACとして採用する方針。承認状態を確認する。
- 提案: まだ正式化していない改善案。原則として `learning/` に置く。

## 追加判断

情報は増やすこと自体を目的にしない。

新しいページや分類を追加する前に、既存のHACTAC OS、Intelligence、Client Memoryのどこへ統合できるかを確認する。

統合できる場合は追加しない。分ける場合は、社員が実務で参照しやすくなる、AIが誤読しにくくなる、機密性を守りやすくなる、のいずれかを理由として明記する。

## メタデータ

すべてのMarkdownは、READMEに定義した共通メタデータを持つことを基本とする。

特に `status`、`sensitivity`、`knowledge_type` は、AIと人間が文書の扱いを判断するための必須情報として扱う。

## 要確認

- `foundation/` ディレクトリを作るか、上位ファイルで管理するか
- `clients/` と `projects/` の紐づけ方法
- `relationship/` に記録する範囲
- `design/` の下位カテゴリ
