# 自動化実例038｜Alpaca→Airtable市場スナップショット台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Alpacaのread-only stock snapshotを取得し、
Airtableへ時点付き市場観測台帳として保存する。

```text
Alpaca market clock
  ↓
AAPL / MSFT / NVDA snapshots
  ↓
IEX feed
  ↓
Airtable 市場スナップショット台帳
  ↓
reREAD
```

## Alpaca

Market:
- is_open = false
- next_open = 2026-09-21T09:30:00-04:00

Feed:
**IEX**

### AAPL
- latest trade: 335.73
- daily close: 335.73
- previous close: 337.09

### MSFT
- latest trade: 493.10
- daily close: 493.10
- previous close: 497.67

### NVDA
- latest trade: 221.39
- daily close: 222.04
- previous close: 219.40

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**市場スナップショット台帳**

Table ID:
`tblkgsG224OnLVt6c`

## Re-read

- Symbol = 3/3 MATCH
- Latest Trade = 3/3 MATCH
- Daily Close = 3/3 MATCH
- Previous Close = 3/3 MATCH
- Feed = IEX
- Market Status = closed
- Next Open = MATCH

## Audit

- Preserve IEX feed label
- Do not call closed-market snapshot a live consolidated market price
- Preserve timestamps
- Do not turn this into trade advice

## Proven

- Alpaca get_clock = **PROVEN**
- Alpaca get_stock_snapshot = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No orders.
No trades.
No account action.
No positions.
No investment recommendation.

## Notion

https://app.notion.com/p/3e0c10ec598c81029790c3c4f0b0e30f?pvs=204
