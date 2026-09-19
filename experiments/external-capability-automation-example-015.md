# 自動化実例015｜Google Drive資産→Adobe PDFカタログ化

Status: **E2E PROVEN / visual verification PARTIAL**  
Date: 2026-09-19

## 目的

Google Drive上の制作資料メタデータを、
配布・確認用のPDFカタログへ変換する。

```text
Google Drive
  ↓
制作資料metadata READ
  ↓
Markdown構造化
  ↓
Adobe Acrobat
  ↓
PDF生成
  ↓
PDF properties READ
  ↓
PDF→PNG render
```

## 対象6件

- Kit Gaw｜外向け詳細企画書 v0.8.3｜思想・循環統合版
- Kit Gaw｜外向け詳細企画書 v0.8.1C｜カラー版
- Kit Gaw｜外向け詳細企画書 v0.8.1
- Kit Gaw｜外向け企画書 v0.8
- OSテンプレ
- ヒデロツク資料総目録©️｜Googleドキュメント棚卸し 第1次

Drive側を再READして実在確認。

## Adobe PDF

Asset ID:
`urn:aaid:sc:AP:992e9300-7370-432e-8376-6f885d07609a`

一時URL:
https://at.adobe.com/5LUxcXMqWvyn22dMTZgBhkf1UcLo

Properties:
- page count: 2
- file size: 239.55 KB
- PDF version: 1.6
- encrypted: false
- signed: false
- tagged: true

## Render

PDF→PNG変換処理も成功。

Render asset ID:
`urn:aaid:sc:AP:7827b6b9-1fd6-490c-91d6-7185d218e5a7`

ただしAdobeの一時リンクをローカル計算環境へ再搬送できず、
PNGの独立目視確認は未完了。

## 実機状態

- Google Drive source READ = **PROVEN**
- 6資料実在確認 = **PROVEN**
- Markdown構造化 = **PROVEN**
- Adobe markdown_to_pdf = **PROVEN**
- Adobe pdf_properties = **PROVEN**
- Adobe pdf_to_image = **PROVEN**
- 独立目視レイアウト監査 = **PARTIAL**

## この回路で増えた能力

以前:
Driveの資料を検索・台帳化する。

今回:
**Driveの制作資産一覧を、PDF成果物へ変換できる。**

## 境界

本文はDriveから抽出していない。
資料名・ID・URL・共有状態などのメタデータを使用。

PDFはAdobeの一時成果物で、永続保存は未実施。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81639134d65a517bb108?pvs=204
