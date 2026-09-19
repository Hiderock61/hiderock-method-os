# 自動化実例047｜Plugin Management→Airtable外付け能力・権限監査台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

ChatGPT Plugin Management上のpermission設定をREADし、
Provider側authorizationとは別レイヤーとして
Airtableへ監査記録する。

```text
Plugin Management get_app_permissions
  ↓
global permission
app-specific permission
override/inherit
  ↓
Airtable 外付け能力・権限監査台帳
  ↓
reREAD
```

## Targets

- Notion
- GitHub
- Slack
- HubSpot
- Miro

## Results

Global default:
**Allow low-risk actions**

App-specific:
- Notion = Allow all actions
- GitHub = Allow all actions
- Slack = Allow all actions
- HubSpot = Use my default
- Miro = Allow all actions

## Key rule

**App Permission ≠ Provider OAuth ≠ Tool-specific confirmation ≠ PROVEN**

Examples:
- Slack List creation can still require provider auth
- HubSpot CONTACT write can still require reauthorization
- Miro new-board creation can still require explicit confirmation

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**外付け能力・権限監査台帳**

Table ID:
`tblEYjQxc9Ps6Ixg4`

## Re-read

- plugin = 5/5 MATCH
- global permission = 5/5 MATCH
- app permission = 5/5 MATCH
- override mode = 5/5 MATCH
- provider gate note = 5/5 MATCH

## Proven

- Plugin Management get_app_permissions = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No permission changes.
No install/uninstall.
No OAuth changes.
No provider reauthorization.

## Notion

https://app.notion.com/p/3e0c10ec598c8132aae8c0cfc696c86c?pvs=204
