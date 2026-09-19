# 自動化実例023｜SciSpace→Scite→Miro研究マトリクス

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

SciSpaceで論文候補を発見し、
SciteでDOI・引用状況を監査し、
Miroへ比較可能な研究マトリクスとして落とす。

```text
SciSpace
  ↓
論文候補
  ↓
Scite
  ↓
DOI / citation tally / Smart Citations
  ↓
Miro
  ↓
研究マトリクス
  ↓
再READ
```

## 対象3論文

### Cui et al. (2024)
The Productivity Effects of Generative AI: Evidence from a Field Experiment with GitHub Copilot  
DOI: `10.21428/e4baedd9.3ad85f1c`

- 1,974人、Microsoft / Accentureの2フィールド実験
- Copilot群で週あたりPull Request完了数が増える傾向
- Scite: citing publications 9 / supporting 0 / contrasting 0 / mentioning 1
- 注意: 予備的結果。推定は不精確で統計的有意性は仕様に依存

### Tan et al. (2024)
How far are AI-powered programming assistants from meeting developers' needs?  
DOI: `10.48550/arxiv.2404.12000`

- 27人のCS学生、3種類のAIコーディング支援、3タイプの開発タスク
- 全体では完了率・時間・コード品質・自己評価生産性が改善
- 経験者では完了時間が増える場合も観測
- Scite: citing publications 1 / supporting 0 / contrasting 0 / mentioning 3
- 注意: 学生サンプルで職業開発者全体への一般化は不可

### Pandey et al. (2024)
Transforming Software Development: Evaluating the Efficiency and Challenges of GitHub Copilot in Real-World Projects  
DOI: `10.48550/arxiv.2406.17910`

- 大規模独自コードベース、15種類の開発タスク
- 文書化・補完で最大50%、反復実装等で30–40%の時間短縮を報告
- 複雑タスク・複数ファイル・独自文脈では弱い
- Scite: citing publications 15 / supporting 0 / contrasting 0 / mentioning 10
- 注意: 分類済み引用はmentioningのみ

## Miro実体

Board:
**能力棚 #029｜Miro実機試験**

Table:
**AIコーディング支援｜SciSpace×Scite研究マトリクス**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684276543851

## 列

- 論文
- 方法
- 主な結果
- Scite引用状況
- 注意点

## 再READ結果

- Cui = MATCH
- Tan = MATCH
- Pandey = MATCH
- total rows = 3

**3 / 3 MATCH**

## 監査ルール

**引用されている ≠ 支持されている**

今回の3論文ではSciteのsupporting / contrasting分類はいずれも0で、
分類済みSmart Citationsはmentioningのみだった。

## 実機状態

- SciSpace search = **PROVEN**
- 3論文選定 = **PROVEN**
- Scite DOI metadata = **PROVEN**
- Scite citation tally = **PROVEN**
- Miro table create = **PROVEN**
- Miro rows write ×3 = **PROVEN**
- Miro rows reREAD = **PROVEN**
- board_show = **PROVEN**
- 3/3一致 = **PROVEN**

## Elicit代替経路

Elicitは `api_access_denied`。
現在プランではAPI access対象外のため **R-011｜READY / PLAN GATE**。

## 境界

主張はSciSpace検索結果の要旨とSciteのメタデータ・引用状況に基づく。
3論文全文を通読したレビューではない。

supporting / contrasting が0であることは「反証がない」ことを意味しない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81fe922df08d934d29ff?pvs=204
