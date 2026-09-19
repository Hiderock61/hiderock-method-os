# 自動化実例027｜GitHub図鑑→Lucid native mind map→構造再READ

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

GitHubの自動化実例図鑑001〜026をLucidのnative mind mapへ変換し、
個別ノードをLucid自身から検索・structured fetchできることを確認する。

```text
GitHub INDEX
  ↓
実例001〜026
  ↓
Lucid native mind map
  ↓
document text search
  ↓
structured fetch
  ↓
PNG export
```

## Lucid実体

Document:
**Plugin自動化実例図鑑｜native mind map 001〜026**

Document ID:
`bb7ba55b-cd6a-4af4-ab5d-bdb80f20a297`

Edit:
https://lucid.app/lucidchart/bb7ba55b-cd6a-4af4-ab5d-bdb80f20a297/edit

View:
https://lucid.app/lucidchart/bb7ba55b-cd6a-4af4-ab5d-bdb80f20a297/view

## 検索監査

代表6ノードを検索:

- 001｜本館・公開監査自動化
- 007｜GitHub図鑑→Coda台帳化
- 014｜Airtable案件DB→Trello→Linear課題化
- 019｜Apple Music×Shazam→音源版監査DB
- 024｜Exa→Firecrawl→Miro AIプロトタイピング実例比較
- 026｜Google Drive＋Canva→Coda制作資産統合台帳

結果:
**6 / 6 HIT**

## structured fetch

page 1 / region 1をfetch。

各実例がLucid内部で
`IntelligentMindMapNodeBlock`
として個別に保持され、
`collectionPrimaryKey` と `TextAreas.t_Text` を取得できた。

## Mermaid版との比較

旧R-002のMermaid版:
`322e7e2b-b674-4c8c-88d2-75a19264ef7f`

Mermaid版は
`LucidNativeMermaidDiagramZeroStateBlock`
という1個の塊として保持され、
内部ノード文字列検索は0件だった。

Native mind mapでは個別ノード検索・fetchが可能。

## 監査ルール

**Lucidで後から構造READしたい図は、Mermaid一枚物ではなくnative mind map / native shapesを使う。**

## 実機状態

- GitHub INDEX READ = **PROVEN**
- Lucid native mind map create = **PROVEN**
- 26 child nodes create = **PROVEN**
- Lucid text search = **PROVEN**
- representative 6/6 hits = **PROVEN**
- structured fetch = **PROVEN**
- individual node labels READ = **PROVEN**
- PNG export = **PROVEN**

## 判定

**自動化実例027｜GitHub INDEX → Lucid native mind map → 構造再READ → PNG = E2E PROVEN**

旧R-002はこの実例へ昇格。

## Notion正本

https://app.notion.com/p/3e0c10ec598c819584eddf62c012bf4d?pvs=204
