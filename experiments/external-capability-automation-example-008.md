# 自動化実例008｜Jotform相談→Notion案件カード化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-19

## 目的

Jotformの相談フォーム送信を読み、
送信1件をNotion案件カード1件へ変換する。

```text
Jotform
  ↓
submissions READ
  ↓
各送信を個別構造化
  ↓
Notion
  ↓
1 submission = 1案件カード
  ↓
Notion再READ
```

## 対象フォーム

**仕事相談受付（オノノケホールディングス）**

Form ID:
`262565341165053`

## 実験データ

既存のテスト送信3件を使用。
実在顧客案件ではなく、公開導線・フォーム・送信動作の確認用データ。

## 変換項目

各Submissionから以下をNotionへ保存。

1. 現状
2. 望む状態
3. 参考URL
4. 返信先
5. Submission ID

## Notion側

親ページ:
**📨 Jotform相談受付｜案件カード化テスト**

3件の案件カードを作成。

- `6652201416321967587`
- `6652189256324301051`
- `6652171863308633759`

## 再READ

3件すべてをNotionから再取得し、
Jotform側の内容と保存内容を照合。

**3 / 3 MATCH**

## この回路で増えた能力

以前:
フォーム送信はJotform受信箱にあるだけ。

今回:
**フォーム送信を、後から追跡できるNotion案件カードへ変換できる。**

## 実機状態

- Jotform submissions list = **PROVEN**
- Jotform submission analysis = **PROVEN**
- 3件個別構造化 = **PROVEN**
- Notion親ページ作成 = **PROVEN**
- Notion案件カード3件作成 = **PROVEN**
- Notion再READ = **PROVEN**
- 3/3内容一致 = **PROVEN**

## 境界

今回のE2Eはテスト送信データで実証。

実顧客からの新規相談に対する継続運用は、
実データ到着後に同じ回路で観測する。

返信メール送信、案件受諾、外部連絡はこの回路に含めない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81758191c0e8aa3f9542?pvs=204
