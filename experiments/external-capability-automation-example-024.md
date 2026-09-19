# 自動化実例024｜Exa→Firecrawl→Miro AIプロトタイピング実例比較

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

ExaでAIプロトタイピング / AI-assisted MVPのケーススタディを発見し、
Firecrawlで本文を再取得し、
Miroへ比較マトリクスとして落とす。

```text
Exa
  ↓
候補発見
  ↓
Firecrawl
  ↓
本文再確認
  ↓
Miro
  ↓
比較マトリクス
  ↓
再READ
```

## 対象3事例

### Restive
Sydney start-up AI life-admin platform

- 出発点: 初期構想
- 期間: 6か月
- AI: AWS Bedrockによる文書分類、情報抽出、動的テンプレ、会話型ガイダンス
- 人間: アーキテクチャ、セキュリティ、デザインシステム、Web/モバイル実装、統合
- 成果物: 本番運用可能なWeb＋モバイルMVP。顧客へコードとアーキテクチャを引き渡し

### SCAND
Famous.ai prototype → production MVP

- 出発点: 顧客自身がFamous.aiで作った動作するAI生成プロトタイプ
- 期間: 10営業日
- AI: 既存プロトタイプ分析とAI-assisted engineering
- 人間: 業務フロー復元、コード監査、移行戦略、アーキテクチャ安定化、テスト、CI/CD、本番配備
- 成果物: AIプラットフォーム依存を外した独立SaaS MVP、GitHub完全ソース、テスト、開発フロー、本番配備

### Daniel Carral
Sophia Nexus research MVP

- 出発点: 心理療法研究の蓄積と長年の構想
- 期間: 3週間。第1週末に共有可能な初期プロトタイプ
- AI: 発想、コード生成、UI設計、Gemini APIによる要約・概念マップ・会話探索
- 人間: 週次の計画→構築→フィードバック、ユーザーインタビュー、方向修正、知識構造化
- 成果物: デプロイ済み研究MVP＋共有Notionの意思決定記録とロードマップ

## Miro実体

Board:
**能力棚 #029｜Miro実機試験**

Table:
**AIプロトタイピング実例｜Exa×Firecrawl比較マトリクス**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684276924124

## 再READ結果

- Restive = MATCH
- SCAND = MATCH
- Daniel Carral = MATCH
- total rows = 3

**3 / 3 MATCH**

## 観測

3事例とも「AIが全部やる」ではなく、
AIは速度を上げる一方で、

- アーキテクチャ
- セキュリティ
- 技術判断
- ユーザー検証
- 引き渡し可能な運用基盤

は人間側の重要工程として残っていた。

## 実機状態

- Exa web search = **PROVEN**
- 3候補選定 = **PROVEN**
- Firecrawl scrape ×3 = **PROVEN**
- Miro table create = **PROVEN**
- Miro rows write ×3 = **PROVEN**
- Miro rows reREAD = **PROVEN**
- board_show = **PROVEN**
- 3/3一致 = **PROVEN**

## 境界

各成果・期間は各社自身のケーススタディ記載。
第三者による独立検証ではない。

これはサービス品質ランキングではなく、事例構造の比較。

## Notion正本

https://app.notion.com/p/3e0c10ec598c818b94f0f63fd97dbbe2?pvs=204
