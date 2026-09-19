# 自動化実例035｜Higgsfield動画モデルカタログ→Airtable動画生成モデル台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Higgsfieldのread-only video model catalogを
Airtableのモデル選択台帳へ変換する。

```text
Higgsfield models_list(video)
  ↓
representative 8 models
  ↓
Airtable 動画生成モデル台帳
  ↓
reREAD
```

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**動画生成モデル台帳**

Table ID:
`tblgB8wUZc3dCz5nV`

## Models

- Cinema Studio Video 3.0
- Marketing Studio
- FLUX 3 Video
- MiniMax H3
- Seedance 2.0
- Seedance 2.0 Mini
- Seedance 2.5
- Wan 2.6 Video

## Stored fields

- モデル名
- Model ID
- Provider
- 説明
- 入力
- Aspect Ratios
- Duration
- Audio
- 特徴

## Re-read

- Model name = 8/8 MATCH
- Model ID = 8/8 MATCH
- Provider = 8/8 MATCH
- input roles = 8/8 MATCH
- duration = 8/8 MATCH
- aspect ratios = 8/8 MATCH

## Proven

- Higgsfield models_list(video) = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No generation.
No credits spent.
No publish.
No deploy.
No media upload.
No avatar generation.

## Notion

https://app.notion.com/p/3e0c10ec598c810794c0db6453a8bf22?pvs=204
