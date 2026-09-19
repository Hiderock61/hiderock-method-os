# 自動化実例011｜Jotform相談→Airtable案件台帳化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-19

## 目的

Jotformの仕事相談送信を、Notionではなく実務用Airtableレコードへ変換する。

```text
Jotform
  ↓
submission READ / 個別構造化
  ↓
Airtable
  ↓
1 submission = 1 record
  ↓
再READ
```

## Airtable実体

Base:
**実機試験#056｜Airtable最小テスト**

Base ID:
`appoJtVWhxi2XjOXG`

Table:
**仕事相談案件**

Table ID:
`tblblDFSN0pkSPnet`

## フィールド

- Submission ID
- 現状
- 望む状態
- 参考URL
- 返信先
- 状態

## 使用したJotform送信

- `6652201416321967587`
- `6652189256324301051`
- `6652171863308633759`

## Airtableレコード

- `recmewGecP3BUfgMF`
- `recWHLwIl0QZNIq13`
- `rec0mKyueqU4kyE0k`

## 再READ結果

3件すべてをAirtableから再取得し、
Submission ID / 現状 / 望む状態 / 参考URL / 返信先 / 状態を確認。

**3 / 3 MATCH**

## この回路で増えた能力

以前:
相談内容を記録する。

今回:
**問い合わせを、状態付きの実務DBレコードとして運用できる。**

## 実機状態

- Jotform submission analysis = **PROVEN**
- Airtable workspace/base access = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable record create = **PROVEN**
- 3 records insert = **PROVEN**
- Airtable再READ = **PROVEN**
- 3/3一致 = **PROVEN**

## 境界

今回使用したのは既存のテスト送信3件。
実顧客の継続運用は未観測。

返信、案件受諾、外部連絡、公開は行っていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81e9b7b9ffd3aa8c5d54?pvs=204
