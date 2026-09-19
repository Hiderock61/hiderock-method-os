# 自動化実例012｜Google Drive→Airtable制作資料台帳化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

Google Drive上の制作・方法系ドキュメントを、
本文を読まずにメタデータだけでAirtable資産台帳へ変換する。

```text
Google Drive
  ↓
制作資料を検索
  ↓
metadata抽出
  ↓
安全対象を選別
  ↓
Airtable
  ↓
1 file = 1 record
  ↓
再READ
```

## 対象6件

- Kit Gaw｜外向け詳細企画書 v0.8.3｜思想・循環統合版
- Kit Gaw｜外向け詳細企画書 v0.8.1C｜カラー版
- Kit Gaw｜外向け詳細企画書 v0.8.1
- Kit Gaw｜外向け企画書 v0.8
- OSテンプレ
- ヒデロツク資料総目録©️｜Googleドキュメント棚卸し 第1次

本文は読まず、メタデータのみ使用。

## Airtable実体

Base:
**実機試験#056｜Airtable最小テスト**

Base ID:
`appoJtVWhxi2XjOXG`

Table:
**Drive制作資料台帳**

Table ID:
`tblgU5TPv1vz5MSoH`

## フィールド

- タイトル
- カテゴリ
- Drive File ID
- MIME
- 更新日時
- 最終閲覧日時
- 共有済み
- URL

## 再READ結果

Airtableから6件を再取得し、
title / category / file ID / MIME / timestamps / URLを確認。

共有済み=trueの2件も保持。

**6 / 6 MATCH**

## この回路で増えた能力

以前:
Drive内の資料を検索して、その場で見る。

今回:
**Driveの制作資産を、横断検索・分類・棚卸しできる運用台帳へ変換できる。**

## 実機状態

- Google Drive search = **PROVEN**
- metadata READ = **PROVEN**
- 安全対象6件選別 = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable 6 records insert = **PROVEN**
- Airtable再READ = **PROVEN**
- 6/6一致 = **PROVEN**

## 補足

Airtable dateTime field作成時にtimezone値がAPI側で弾かれたため、
更新日時・最終閲覧日時はISO文字列として保存した。

## 再利用先

- Google Drive制作資料棚卸し
- バージョン違い資料の管理
- 公開候補 / 非公開資料の整理
- 制作物カタログ
- 古い資料の発掘キュー

## Notion正本

https://app.notion.com/p/3e0c10ec598c81ce821bfd1936adcd3f?pvs=204
