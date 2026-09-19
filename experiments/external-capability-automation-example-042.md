# 自動化実例042｜Linear workflow schema→Airtable開発ワークフロー設計台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

LinearのIssue内容には入らず、
TeamとIssue Status schemaだけを
Airtableへ保存する。

```text
Linear Team
  ↓
Issue Status schema
  ↓
Airtable 開発ワークフロー設計台帳
  ↓
reREAD
```

## Team

- name: Hiderock
- visibility: public

## Workflow States

- Backlog = backlog
- Todo = unstarted
- In Progress = started
- Done = completed
- Canceled = canceled
- Duplicate = duplicate

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**開発ワークフロー設計台帳**

Table ID:
`tblLZrnwJqUAM8DM0`

## Re-read

- State = 6/6 MATCH
- Type = 6/6 MATCH
- Status ID = 6/6 MATCH
- Team = Hiderock
- Team Visibility = public

## Audit

- No issue body/comment read
- Preserve Linear type/name/ID
- No inferred ordering/colors/classification

## Proven

- Linear list_teams = **PROVEN**
- Linear list_issue_statuses = **PROVEN**
- Linear get_issue_status ×6 = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No issue create/update.
No status mutation.
No comments.
No project mutation.

## Notion

https://app.notion.com/p/3e0c10ec598c81f8b30df4074873e95b?pvs=204
