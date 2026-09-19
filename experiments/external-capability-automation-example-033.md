# 自動化実例033｜Lovable→Airtable開発プロジェクト台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Lovableの既存プロジェクトをREADし、
Airtableの開発プロジェクト台帳へ保存して再READする。

```text
Lovable workspace
  ↓
list_projects
  ↓
get_project ×3
  ↓
Airtable 開発プロジェクト台帳
  ↓
reREAD
```

## Lovable

Workspace:
**Hideki's Lovable**

Workspace ID:
`DyIpkfYkMbHnGYHouMjT`

Projects:
1. Ability Weaver
2. Artifact Shelf
3. Suginami Water Fix

3件とも:
- ready / completed
- is_published = false

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**開発プロジェクト台帳**

Table ID:
`tblqeOUMQuZPxjska`

## Columns

- プロジェクト名
- 元サービス
- Project ID
- 状態
- 公開状態
- 最終編集
- 最新Commit
- 説明
- Editor URL
- Preview URL

## Re-read

- Ability Weaver = MATCH
- Artifact Shelf = MATCH
- Suginami Water Fix = MATCH
- Project ID = MATCH
- status = MATCH
- published = false
- URLs = MATCH
- total = 3

**3 / 3 MATCH**

## Audit rule

Airtable connectorのdateTime timezone schemaが今回弾かれたため、
最終編集は文字列で保持した。
推定変換はしない。

## Proven

- Lovable workspace READ = **PROVEN**
- Lovable list_projects = **PROVEN**
- Lovable get_project ×3 = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable record create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No code read.
No edit.
No deploy.
No publish.

## Notion

https://app.notion.com/p/3e0c10ec598c811b8a21c03f52b86a79?pvs=204
