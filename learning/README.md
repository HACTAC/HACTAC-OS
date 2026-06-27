---
title: Learning
status: proposed
domain: learning
sensitivity: public
knowledge_type: proposal
owner: HACTAC
last_reviewed: 2026-06-26
---

# Learning

このディレクトリは、承認前の学習提案を蓄積する場所である。

AIや人間が実務から見つけた改善案、分類案、ルール案、仮説は、いきなり正式知識へ反映せず、まずここに置く。

## 役割

- AIが見つけた改善案を保留する
- 未承認の仮説を正式知識と分ける
- 実務から得た学びを提案として記録する
- 承認後に正式ファイルへ反映する候補を管理する

## 運用方法

提案は小さな単位で作成する。

各提案には、根拠、影響範囲、反映先候補、確認事項を記載する。

承認フローの詳細は `learning/APPROVAL_FLOW.md` を参照する。

## 提案テンプレート

正式な提案テンプレートは `templates/LEARNING_PROPOSAL.md` を使う。

```md
---
title: 提案タイトル
status: proposed
domain: learning
sensitivity: public
knowledge_type: proposal
owner: HACTAC
last_reviewed: YYYY-MM-DD
---

# 提案タイトル

## 提案

## 根拠

## 反映先候補

## 影響範囲

## 要確認
```

## 要確認

- 提案番号や命名ルール
- 承認済み提案の移動またはアーカイブ方法
