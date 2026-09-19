# 自動化実例016｜Airtable案件DB→monday.com業務ボード化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-19

## 目的

Airtableに保存された仕事相談案件を、
monday.comの列付き業務ボードへ変換する。

```text
Airtable
  ↓
案件DB
  ↓
monday.com
  ↓
業務ボード
  ↓
再READ
```

## monday.com実体

Board:
**仕事相談案件｜Airtable連携テスト**

Board ID:
`18431838556`

URL:
https://akechikuncoms-team.monday.com/boards/18431838556

Workspace:
**メインワークスペース**

## 追加列

- Submission ID
- 現状
- 望む状態
- 参考URL
- 状態

## 作成した3アイテム

1. 本番公開テスト｜相談受付導線
2. ブラウザ往復テスト｜相談受付導線
3. 問い合わせ導線｜実機確認

3件とも状態は **新規**。

## 再READ結果

monday.comから3件を再取得し、

- item name
- Submission ID
- 現状
- 望む状態
- 参考URL
- 状態

を確認。

**3 / 3 MATCH**

## この回路で増えた能力

以前:
Airtableで案件を保存する。
Trelloで案件をカードとして動かす。

今回:
**Airtableの案件を、列付きの業務台帳＋進行面へ変換できる。**

役割差:
- Airtable = DB
- Trello = カンバン進行
- monday.com = 業務台帳＋進行面

## 実機状態

- monday workspace READ = **PROVEN**
- monday private board create = **PROVEN**
- monday column create ×5 = **PROVEN**
- monday item create ×3 = **PROVEN**
- status label「新規」 = **PROVEN**
- monday item再READ = **PROVEN**
- 3/3一致 = **PROVEN**

## 境界

使用したのは既存のテスト相談3件。
担当者割当、期限、通知、自動メール、外部公開は行っていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81eca96fd3b221b279f9?pvs=204
