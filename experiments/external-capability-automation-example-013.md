# 自動化実例013｜Airtable案件DB→Trello作業ボード化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-19

## 目的

Airtableに保存された仕事相談案件を、
実際に動かすためのTrelloカンバンへ変換する。

```text
Airtable
  ↓
案件3件READ
  ↓
Trello
  ↓
非公開ボード作成
  ↓
新規 / 確認中 / 完了
  ↓
1 record = 1 card
  ↓
再READ
```

## Trello実体

Board:
**仕事相談案件｜Airtable連携テスト**

URL:
https://trello.com/b/PlgY8hwF/%E4%BB%95%E4%BA%8B%E7%9B%B8%E8%AB%87%E6%A1%88%E4%BB%B6%EF%BD%9Cairtable%E9%80%A3%E6%90%BA%E3%83%86%E3%82%B9%E3%83%88

Board ID:
`ari:cloud:trello::board/workspace/6aac3e260d90f05342f73a31/6aae4b42f90973ef3af3a17f`

## リスト

- 新規
- 確認中
- 完了

## 作成した3カード

1. 本番公開テスト｜相談受付導線
   - Submission ID: `6652201416321967587`

2. ブラウザ往復テスト｜相談受付導線
   - Submission ID: `6652189256324301051`

3. 問い合わせ導線｜実機確認
   - Submission ID: `6652171863308633759`

3件とも初期状態として **新規** に配置。

## 再READ結果

Trelloからボード内を再取得し、

- 3 lists = MATCH
- 3 cards = MATCH
- 3 cardsとも「新規」 = MATCH
- Submission ID / 現状 / 望む状態 / 参考URL = 保持

**3 / 3 MATCH**

## この回路で増えた能力

以前:
Airtableで案件を保存・分類する。

今回:
**保存された案件を、実際に動かすカンバン作業へ変換できる。**

役割分担:
- Airtable = 案件DB
- Trello = 現場の進行面

## 実機状態

- Airtable案件READ = **PROVEN**
- Trello workspace READ = **PROVEN**
- Trello board create = **PROVEN**
- Trello list create ×3 = **PROVEN**
- Trello card create ×3 = **PROVEN**
- Trello board再READ = **PROVEN**
- 3/3一致 = **PROVEN**

## 境界

使用したのは既存のテスト相談3件。
実顧客案件ではない。

カード移動、完了処理、担当者割当、通知は今回の回路には含めない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81e7bda2cde60c7fbc4a?pvs=204
