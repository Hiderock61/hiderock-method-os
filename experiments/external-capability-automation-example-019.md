# 自動化実例019｜Apple Music×Shazam→音源版監査DB

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

Apple Musicで採用した参照曲をShazam検索でも再検索し、
同名曲・別ID・別版・ISRC差をAirtableへ記録する。

```text
Apple Music
  ↓
採用する参照曲を確定
  ↓
Shazam searchMusic
  ↓
検索トップ / 候補順位 / 版違いを監査
  ↓
Airtable
  ↓
監査列更新
  ↓
再READ
```

## Airtable追加列

- Shazam検索トップID
- Shazam照合判定
- 版監査メモ

## 3曲の結果

### ユー・クッド・ビー・マイン
- 台帳ID: `1389971339`
- Shazam検索トップID: `1389971339`
- 判定: **同一IDが検索トップ**
- 2022 Remaster / Liveなど別版も存在

### Killing In The Name
- 台帳ID: `578028952`
- Shazam検索トップID: `191450927`
- 判定: **台帳IDは検索2位、トップは別版**
- Demo版 `578028993` も存在

### Walk This Way (feat. Aerosmith)
- 台帳ID: `253155642`
- Shazam検索トップID: `254344996`
- 判定: **Top5では別ID、同一ISRC候補あり**
- 台帳曲と検索トップはISRC `USAR19900334`
- 7インチ版は別ISRC `USAR19901588`

## 監査ルール

- **曲名一致 ≠ 同じ音源版**
- **Apple Music ID違い ≠ 必ず別録音**
- ISRC / アルバム / 長さ / 版表記まで見る

## 実機状態

- Apple Music reference metadata = **PROVEN**
- Shazam searchMusic = **PROVEN**
- version candidate observation = **PROVEN**
- same ID detection = **PROVEN**
- alternate ID detection = **PROVEN**
- same ISRC / different ID observation = **PROVEN**
- Airtable field create ×3 = **PROVEN**
- Airtable records update ×3 = **PROVEN**
- Airtable再READ = **PROVEN**
- 3/3一致 = **PROVEN**

## Shazam周辺の補足

- `getInfluencers`: 今回サーバーエラー
- `getBandMembers`: 取得は成功したが一覧が限定的

完全な系譜・メンバー表としては使わない。

## 境界

Shazam searchMusicはApple Musicカタログを利用するため、
独立した別データ源とのクロスチェックではない。
音響波形やマスタリング内容そのものも比較していない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81e0a263e857f5a5b395?pvs=204
