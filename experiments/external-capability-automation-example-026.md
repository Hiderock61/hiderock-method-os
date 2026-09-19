# 自動化実例026｜Google Drive＋Canva→Coda制作資産統合台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Google Driveの文書資産とCanvaのデザイン資産を、
同じ列構造へ正規化してCodaの横断制作資産台帳へまとめる。

```text
Google Drive ─┐
              ├→ metadata正規化 → Coda統合台帳 → 再READ
Canva ────────┘
```

## Coda実体

Document:
**制作資産統合台帳｜Google Drive＋Canva**

URL:
https://coda.io/d/_dDBkL1-5lz-

Table:
**制作資産一覧**

Table URI:
`coda://docs/DBkL1-5lz-/pages/section-ImnsAhO9lU/tables/grid-YCAMFQV2il`

## 対象

Google Drive 4件:
- 【現役親仕様】Kit Gaw｜外向け企画書 v1.2｜地上語再設計版
- Kit Gaw｜外向け詳細企画書 v0.8.3｜思想・循環統合版
- OSテンプレ
- ヒデロツク資料総目録©️｜Googleドキュメント棚卸し 第1次

Canva 3件:
- 能力棚🔌｜外付け能力接続ランタイム
- 青と緑 抽象的 アート ストーリー
- 人生から「さぁ、どうする？」と問われた日

## 共通列

- 資産名
- 元サービス
- 種類
- Asset ID
- 更新日時
- 共有状態
- URL

## 再READ結果

- Google Drive = 4
- Canva = 3
- total rows = 7
- Asset ID = MATCH
- URL = MATCH
- 元サービス = MATCH

**7 / 7 MATCH**

## 実機状態

- Google Drive metadata READ = **PROVEN**
- Canva owned design READ = **PROVEN**
- Coda document create = **PROVEN**
- Coda table create = **PROVEN**
- explicit column typing = **PROVEN**
- 7 rows write = **PROVEN**
- Coda rows reREAD = **PROVEN**
- 7/7一致 = **PROVEN**

## 境界

本文・画像内容そのものは統合していない。
メタデータ台帳のみ。
用途不明・タイトル不明のCanva資産は除外した。

## Notion正本

https://app.notion.com/p/3e0c10ec598c8177bbe5d9ad3f3419f3?pvs=204
