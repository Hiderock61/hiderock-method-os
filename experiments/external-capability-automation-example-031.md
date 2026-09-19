# 自動化実例031｜Supermetrics Google Trends→Flourish検索関心可視化

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

SupermetricsのGoogle Trends connectorから公開検索関心を取得し、
Flourishで時系列可視化する。

```text
Supermetrics
  ↓
Google Trends
  ↓
Japan / last 90 days
  ↓
interest over time
  ↓
Flourish line chart
  ↓
再READ
```

## 検索語

- AI prototyping
- vibe coding
- no-code

## 条件

- Country: JP
- Search type: Web
- Date range: last 90 days
- Timezone: Asia/Tokyo
- Metric: Interest 0–100

## 有効値日数

- AI prototyping: 0
- vibe coding: 37
- no-code: 5

vibe coding:
- max 100
- min 9

no-code:
- max 56
- min 4

## Flourish実体

Visualisation ID:
`30304212`

Edit URL:
https://app.flourish.studio/visualisation/30304212/edit

Published:
**false**

## データ処理

AI prototypingは全期間空白。
0で補完せず、グラフ系列から除外して
「有効値0件」と明示。

可視化系列:
- vibe coding
- no-code

## 再READ

- total rows = 90
- 2026-07-10 vibe coding = 100
- 2026-07-01 no-code = 56
- visualisation is_published = false

## 監査ルール

- Google Trends値は絶対検索数ではない
- 空白 ≠ 0検索
- 条件を変えると相対指数も変わる
- 全空白列を0で埋めない

## 実機状態

- Supermetrics discovery = **PROVEN**
- Google Trends query = **PROVEN**
- 3語比較 = **PROVEN**
- Flourish create = **PROVEN**
- data upload = **PROVEN**
- bindings = **PROVEN**
- line chart = **PROVEN**
- data再READ = **PROVEN**
- unpublished state = **PROVEN**

## Notion正本

https://app.notion.com/p/3e0c10ec598c81db895ad556c35dc792?pvs=204
