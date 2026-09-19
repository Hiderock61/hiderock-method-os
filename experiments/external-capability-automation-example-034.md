# 自動化実例034｜Slack Channel metadata→Airtableコミュニケーション台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Slackのメッセージ本文には入らず、
Channel metadataだけをAirtableの共通台帳へ保存する。

```text
Slack workspace
  ↓
joined channel metadata
  ↓
Airtable communication channel ledger
  ↓
reREAD
```

## Slack workspace

- name: オノノケコーポレーション
- workspace ID: `T0BGEE2EEV8`

## Channels

1. #チャンネル-サンプル
   - `C0BG86RG13M`
   - Private

2. #general
   - `C0BGEE2RHDG`
   - Public

3. #小麦粉審査会
   - `C0BGJ5TQ3PE`
   - Public

4. #akechi-lab
   - `C0C2D5RCZ5Z`
   - Private

All four are unarchived.

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**コミュニケーションチャネル台帳**

Table ID:
`tblKTojK7VARtVSpU`

## Re-read

- 4 channel names = MATCH
- 4 channel IDs = MATCH
- Public / Private = MATCH
- Workspace = MATCH
- total = 4

**4 / 4 MATCH**

## Audit rules

- No message body read
- No DMs / group DMs
- Metadata only
- Keep public/private classification intact

## Proven

- Slack workspace READ = **PROVEN**
- Slack channel metadata READ = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No Slack message send.
No channel creation.
No invite.
No Slack List creation.
No Canvas creation.

## Notion

https://app.notion.com/p/3e0c10ec598c81259a24c56c4c9e4ba0?pvs=204
