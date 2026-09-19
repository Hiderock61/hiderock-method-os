# 自動化実例025｜Bigdata.com→Miro Plugin提供企業ミニマップ

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

外付け能力棚に登場している企業をBigdata.comのKnowledge Graphで正式解決し、
Miroへ企業属性比較表として落とす。

```text
Bigdata.com
  ↓
company entity resolution
  ↓
country / sector / industry / listing type / listing
  ↓
Miro
  ↓
企業比較表
  ↓
再READ
```

## 対象3社

### Adobe Inc.
- RavenPack entity ID: `C9881C`
- Country: United States
- Sector: Technology
- Industry: Software
- Listing type: PUBLIC
- Main listing: `XNAS:ADBE`

### Atlassian Corp.
- RavenPack entity ID: `RDU3ZQ`
- Country: United States
- Sector: Technology
- Industry: Software
- Listing type: PUBLIC
- Main listing: `XNAS:TEAM`

### Monday.com Ltd.
- RavenPack entity ID: `85150E`
- Country: Israel
- Sector: Technology
- Industry: Application Software
- Listing type: PUBLIC
- Main listing: `XNAS:MNDY`

## Miro実体

Board:
**能力棚 #029｜Miro実機試験**

Table:
**外付け能力｜Plugin提供企業ミニマップ**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684278108686

## 再READ結果

- Adobe = MATCH
- Atlassian = MATCH
- monday.com = MATCH
- total rows = 3

**3 / 3 MATCH**

## この回路で増えた能力

以前:
PluginをChatGPTの追加能力として見る。

今回:
**そのPluginを提供・支える企業を、企業エンティティとして別レイヤーで観測できる。**

将来は企業イベント、earnings、funding、workforce signals等を、
Plugin運用と切り分けて追跡できる。

## 実機状態

- Bigdata.com find_securities ×3 = **PROVEN**
- company entity resolution = **PROVEN**
- listing type / country / sector / industry / listing取得 = **PROVEN**
- Miro table create = **PROVEN**
- Miro rows write ×3 = **PROVEN**
- Miro rows reREAD = **PROVEN**
- board_show = **PROVEN**
- 3/3一致 = **PROVEN**

## 境界

今回は企業属性だけ。
株価、アナリスト評価、投資判断、将来予測は扱っていない。

企業評価やランキングでもない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81b0855fdea12b8a2fea?pvs=204
