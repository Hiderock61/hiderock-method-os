# 自動化実例053｜Google Drive＋Dropbox→Miroファイル資産現在地観測

Status: **E2E PROVEN**  
Date: 2026-09-20

## Purpose

Compare representative file assets across Google Drive and Dropbox without mutating either store.

```text
Google Drive recent docs ─┐
                          ├→ representative asset table → Miro → reREAD
Dropbox root sample ──────┘
```

## Google Drive sample

- 次期Uber生産設備・市場観測
- 雪だるま能力台帳 v0.1｜能力グラフ・実機証拠台帳
- AI最高の友達｜人間とAIの関係性研究原典

## Dropbox sample

- MP3
- Send and track
- 送信済みファイル

Dropbox root read used recursive=false.

The response had `has_more=true`, so this is **not a complete Dropbox inventory**.

## Miro

Table:
**Drive × Dropbox｜ファイル資産の現在地観測**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684304365853

## Re-read

6 rows matched:
- source
- representative asset
- observed modified
- coverage note
- observed role

## Audit

Observed Role is an analysis label based on filenames and observed dates.
It is not provider-supplied taxonomy.

Personal/private-looking Dropbox folder names were excluded from the comparison table.

## Proven

- Google Drive recent_documents = **PROVEN**
- Dropbox root direct-children read = **PROVEN**
- Miro table create/sync/read = **PROVEN**

## Boundary

No Drive writes.
No Dropbox writes.
No sharing changes.
No file-body reads.
No exhaustive Dropbox traversal.

## Notion

https://app.notion.com/p/3e0c10ec598c815cac26f2f94afbedfe?pvs=204
