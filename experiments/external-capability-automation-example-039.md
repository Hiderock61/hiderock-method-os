# 自動化実例039｜Gmail System Labels→Airtable受信インフラ台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Gmail本文には入らず、System Label metadataだけを
Airtableの受信インフラ台帳へ保存する。

```text
Gmail System Labels
  ↓
count / unread / visibility metadata
  ↓
Airtable 受信インフラ台帳
  ↓
reREAD
```

## Gmail scope

System labels only:
- INBOX
- SENT
- DRAFT
- SPAM
- TRASH
- STARRED
- IMPORTANT
- CATEGORY_PERSONAL
- CATEGORY_SOCIAL
- CATEGORY_PROMOTIONS
- CATEGORY_UPDATES
- CATEGORY_FORUMS

No email body, subject, sender, or custom label names were read.

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**受信インフラ台帳**

Table ID:
`tblI6y8zkBb6ZMdeM`

## Re-read

- Label = 12/12 MATCH
- Label ID = 12/12 MATCH
- messages total/unread = 12/12 MATCH
- threads total/unread = 12/12 MATCH
- visibility = MATCH

## Audit

- System labels only
- Do not sum labels as if mutually exclusive
- No email-content read

## Proven

- Gmail list_labels = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No send.
No draft creation.
No label mutation.
No archive/delete.
No email body read.

## Notion

https://app.notion.com/p/3e0c10ec598c8189994df9c54789cd55?pvs=204
