# 自動化実例018｜Apple Music→Airtable音楽リファレンス台帳化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

曲作りで参照している実在曲をApple Musicで確認し、
Airtableの音楽リファレンスDBへ変換する。

```text
Apple Music
  ↓
artist / album / song検索
  ↓
曲単位metadata確認
  ↓
版違い監査
  ↓
Airtable
  ↓
1曲 = 1 record
  ↓
再READ
```

## 今回の3曲

1. ユー・クッド・ビー・マイン
   - Artist: ガンズ・アンド・ローゼズ
   - Album: Use Your Illusion II
   - Apple Music ID: 1389971339
   - Duration: 343640 ms
   - Release: 1991-06-21

2. Killing In The Name
   - Artist: レイジ・アゲインスト・ザ・マシーン
   - Album: Rage Against The Machine - XX (20th Anniversary Special Edition)
   - Apple Music ID: 578028952
   - Duration: 313573 ms
   - Release: 1992-11-02

3. Walk This Way (feat. Aerosmith)
   - Artist: RUN D.M.C
   - Album: The Best of Run–DMC
   - Apple Music ID: 253155642
   - Duration: 310707 ms
   - Release: 1986-05-15

## Airtable実体

Base:
**実機試験#056｜Airtable最小テスト**

Base ID:
`appoJtVWhxi2XjOXG`

Table:
**音楽リファレンス台帳**

Table ID:
`tblWuvuCCS2yuKqnp`

## 再READ結果

Airtableから3件を再取得し、
曲名 / artist / album / release / duration / genre / Apple Music ID / 観測軸 を確認。

**3 / 3 MATCH**

## 重要な発見

Apple Musicのbatch matchingでは、同名曲でも別版へ寄ることがある。

今回:
- Killing In The Name → Demo版候補
- Walk This Way → 7インチ版候補

が出たため、検索結果で通常版を再確認して台帳へ採用。

監査ルール:
**曲名一致 ≠ 同じ音源版**

## この回路で増えた能力

以前:
参照曲を会話や記憶の中で扱う。

今回:
**参照曲を、実在Apple Music ID付きの研究・制作DBとして管理できる。**

## 実機状態

- Apple Music catalog search = **PROVEN**
- song metadata READ = **PROVEN**
- batch matching = **PROVEN**
- version mismatch detection = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create ×3 = **PROVEN**
- Airtable再READ = **PROVEN**
- 3/3一致 = **PROVEN**

## 境界

楽曲の音響解析や歌詞分析はしていない。
Apple Musicのカタログメタデータと制作上の観測軸のみ保存。

プレイリスト作成、ライブラリ追加、購入は行っていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c812da6e0c1636a5dbe82?pvs=204
