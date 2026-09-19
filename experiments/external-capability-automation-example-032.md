# 自動化実例032｜Parallel Search→Airtable AIエージェント公開観測台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

AIプロトタイピング／coding agent周辺の公開一次情報を検索し、
あとで差分追跡できるAirtable観測台帳へ保存する。

```text
Parallel Search
  ↓
official first-party sources
  ↓
selected pages fetch
  ↓
structured observations
  ↓
Airtable watch ledger
  ↓
reREAD
```

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**AIエージェント公開観測台帳**

Table ID:
`tbl8hXAv71AHLAIff`

## 3 observations

### JetBrains / Junie
- date: 2026-06-17
- change: leaves Beta / GA
- watch: planning, debugger use, contextual PR review, ACP-based IDE integration

### Google / Jules
- date: 2026-06-22
- change: proactive-agent evaluation focused on goals and insight policy
- watch: shift from autonomy/task completion toward deciding what matters and when to surface insights

### Anthropic / Claude Code
- date: 2026-06-18
- change: artifacts from coding sessions
- watch: live shareable pages built from codebase + connectors + conversation context

## Re-read

- 3 records returned
- company = MATCH
- date = MATCH
- URL = MATCH
- source = official first-party
- total = 3

**3 / 3 MATCH**

## Audit rules

- Prefer first-party official sources
- If search metadata and body date conflict, use the explicit date shown in the page body
- Company claims remain attributed claims, not independent verification

## Proven

- Parallel Search web_search = **PROVEN**
- Parallel Search web_fetch = **PROVEN**
- Airtable table create = **PROVEN**
- record creation = **PROVEN**
- Airtable reREAD = **PROVEN**

## Notion

https://app.notion.com/p/3e0c10ec598c814b96b4fd936d838468?pvs=204
