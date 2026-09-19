# 自動化実例030｜Coda制作資産統合台帳→Adobe紙カタログPDF化

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Google Drive文書とCanvaデザインを統合したCoda制作資産台帳を、
Adobeで印刷・確認用PDFカタログへ変換する。

```text
Google Drive + Canva
  ↓
Coda制作資産統合台帳
  ↓
7 assets READ
  ↓
Markdown構造化
  ↓
Adobe PDF
  ↓
pdf_properties
```

## 元台帳

Coda:
**制作資産統合台帳｜Google Drive＋Canva**

URL:
https://coda.io/d/_dDBkL1-5lz-

- Google Drive = 4件
- Canva = 3件
- total = 7

## Adobe PDF

Asset ID:
`urn:aaid:sc:AP:5d027aea-8933-4bcd-a454-5d5d5f49245f`

Temporary URL:
https://at.adobe.com/lQ2PkKBwyTBByOT95VmEsB7SDe5F

## PDF properties

- page count = 2
- file size = 318.27 KB
- PDF version = 1.6
- tagged = true
- encrypted = false
- signed = false
- portfolio = false
- has embedded files = true
- Producer = Adobe HTML2PDF creator 2.0.08162018

## 実機状態

- Coda table rows READ = **PROVEN**
- 7 rows取得 = **PROVEN**
- Markdown構造化 = **PROVEN**
- Adobe markdown_to_pdf = **PROVEN**
- Adobe PDF生成 = **PROVEN**
- Adobe pdf_properties = **PROVEN**
- PDF property再READ = **PROVEN**

## この回路で増えた能力

以前:
制作資産をCodaで媒体横断管理する。

今回:
**統合された制作資産棚を、そのまま紙カタログ候補PDFへ変換できる。**

## 境界

独立した目視レイアウト監査は今回未実施。
PDFはAdobe側の一時成果物で永続保存していない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81f4a847cbd7bf8f5745?pvs=204
