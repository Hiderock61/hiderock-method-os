# 自動化実例046｜Plugin Management＋Runtime→Airtable外付け能力接続台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Plugin Directory上のinstalled状態と、
runtime tool exposureを分離して観測し、
Airtableへ外付け能力接続台帳として保存する。

```text
Plugin Management search_plugins
  ↓
installed / status / policy

Runtime namespaces
  ↓
tool exposure

        ↘
         Airtable 外付け能力接続台帳
        ↗

reREAD
```

## Scope

4 search groups only:
- knowledge/work
- dev
- visual
- business/data

This is **not** a complete 85-system inventory.

## 17 plugins

- Trello
- Airtable
- monday.com
- Linear
- Notion
- Slack
- Vercel
- Supabase
- GitHub
- Replit
- Lovable
- Figma
- Canva
- Miro
- Adobe
- HubSpot
- Shopify

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**外付け能力接続台帳**

Table ID:
`tblPYGzWB3AlKevbk`

## Re-read

- plugin = 17/17 MATCH
- plugin ID = 17/17 MATCH
- installed = 17/17 true
- runtime exposed = 17/17 true
- runtime prefix = 17/17 MATCH
- directory status = ENABLED
- installation policy = AVAILABLE

## Critical rule

**Installed ≠ Connected ≠ Tool Exposed ≠ Real Data Available ≠ PROVEN**

This example proves the audit circuit,
not every plugin's end-to-end capability.

## Proven

- Plugin Management search_plugins = **PROVEN**
- installed metadata read = **PROVEN**
- runtime exposure audit = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No install.
No uninstall.
No permission changes.
No OAuth changes.
No complete 85-system sweep.

## Notion

https://app.notion.com/p/3e0c10ec598c81c490b2eee11841f64a?pvs=204
