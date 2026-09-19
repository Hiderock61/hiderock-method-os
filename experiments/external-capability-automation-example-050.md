# 自動化実例050｜GitHub正本→Flourish外付け能力・現在地メーター

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

GitHub canonical indexから
PROVEN / READY / HOLD の現在件数を抽出し、
Flourishで可視化する。

```text
GitHub canonical index
  ↓
regex state count
  ↓
Flourish bar chart
  ↓
reREAD + publication audit
```

## Current state

- PROVEN = 49
- READY = 24
- HOLD = 6
- total state cards = 79

## Flourish

Visualisation:
**外付け能力・現在地メーター｜PROVEN / READY / HOLD｜2026-09-20**

ID:
`30304887`

Edit:
https://app.flourish.studio/visualisation/30304887/edit

Template:
`line-bar-pie`

Chart type:
`bar_grouped`

Published:
**false**

## Data

| State | Count |
|---|---:|
| PROVEN | 49 |
| READY | 24 |
| HOLD | 6 |

## Re-read

- PROVEN 49 = MATCH
- READY 24 = MATCH
- HOLD 6 = MATCH
- 3/3 metadata rows = MATCH
- publication state = unpublished

## Audit

This is **not a success rate**.

The three categories are canonical index state-card counts, not a shared denominator for performance evaluation.

## Proven

- GitHub index read = **PROVEN**
- state parsing = **PROVEN**
- Flourish create = **PROVEN**
- Flourish data upload = **PROVEN**
- Flourish bindings = **PROVEN**
- Flourish settings = **PROVEN**
- Flourish data reREAD = **PROVEN**

## Boundary

No publish.
No external share.
No ranking.
No state mutation.

## Notion

https://app.notion.com/p/3e0c10ec598c81c7a3d5d0f7e0a12c18?pvs=204
