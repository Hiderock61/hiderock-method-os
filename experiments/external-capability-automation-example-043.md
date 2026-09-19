# 自動化実例043｜Linear＋Trello＋monday.com→Miroワークフロー翻訳盤

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Linear / Trello / monday.com のnative workflow schemaを
同じMiro tableへ並べる。

```text
Linear Issue Status ─┐
Trello Lists ────────┼→ Miro workflow translation board → reREAD
monday.com Status ───┘
```

## Miro

Board:
https://miro.com/app/board/uXjVHnIlKBU=/

Table:
**ワークフロー翻訳盤｜Linear × Trello × monday.com**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684302244324

## Source rows

### Linear
6 states:
- Backlog / backlog
- Todo / unstarted
- In Progress / started
- Done / completed
- Canceled / canceled
- Duplicate / duplicate

### Trello
3 lists:
- 完了 / position 4096
- 確認中 / position 8192
- 新規 / position 16384

### monday.com
4 labels:
- 対応中 / index 0
- 完了 / index 1
- スタック / index 2
- 新規 / index 3

## Re-read

- Linear rows = 6
- Trello rows = 3
- monday.com rows = 4
- total = 13
- native fields = 13/13 MATCH

## Audit

- Preserve each tool's native terminology
- Do not infer equivalence across tools
- Do not invent Linear order
- Preserve Trello positions
- Preserve monday status indexes
- No ranking

## Proven

- Linear status READ = **PROVEN**
- Trello list READ = **PROVEN**
- monday.com board/schema READ = **PROVEN**
- Miro table create = **PROVEN**
- Miro row sync = **PROVEN**
- Miro reREAD = **PROVEN**

## Boundary

No issue/card/item body read.
No status mutation.
No card move.
No item update.
No board config change.

## Notion

https://app.notion.com/p/3e0c10ec598c8198800fd3993a28a259?pvs=204
