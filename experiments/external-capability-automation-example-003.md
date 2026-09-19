# 自動化実例003｜Notion→Xmind＋FigJam｜同一内容の多視点化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

Notionにある同じ運用ルールを、別々の認知形式へ変換して比較する。

```text
Notion
  ↓
  ├─ Xmind / Tree Chart
  │    ↓
  │  階層・分類として再READ
  │
  └─ Figma / FigJam Flowchart
       ↓
     工程・分岐・循環として再READ
  ↓
ChatGPTで視点差を比較
  ↓
Notionへ実例記録
```

## 入力

「Plugin組み合わせ発見工場」の運用ルール。

主な内容：
- 監査ルーム
- 配線ルーム
- 自動化実例図鑑
- 成功条件
- 非昇格条件

## Xmindで見えたもの

Tree Chartでは、

- 監査ルーム
- 配線ルーム
- 自動化実例図鑑
- 非昇格

が上位ブランチとして分離した。

特に、成功条件・保存先・現在の実例などが親子関係として読めた。

### Xmind向き

- 分類
- 親子関係
- 棚
- 構成要素

> 何がどこに属するかを見る。

Xmind file ID: `VK7SWvJJ`

## FigJamで見えたもの

Flowchartでは、

```text
監査ルーム
→ PROVEN能力
→ 配線ルーム
→ 現実の工程が進む
→ 再READ / 別センサー
→ E2E成功?
```

が明示された。

さらに、

```text
Yes → Notion実例カード → 自動化実例図鑑
Yes → GitHub再利用Markdown → 自動化実例図鑑
No  → 監査ログへ戻す → 監査ルーム
```

という分岐と循環が可視化された。

### FigJam向き

- 手順
- 因果
- 分岐
- 循環

> 何が次に起こるかを見る。

Figma Diagram ID: `fc01dc06-1ca2-421c-8c89-bf3080bd37b5`

## 比較結果

同じ正本でも、出力形式によって見つかる構造が異なる。

- **Xmind** = 静的な構造・分類
- **FigJam** = 動的な流れ・分岐

## この回路で増えた能力

以前：
Notionの文章を一形式で読む。

今回：
**同じ正本を複数の認知形式へ変換し、その視点差自体を比較できる。**

## 実機状態

- Notion正本READ = **PROVEN**
- Xmind Tree Chart生成 = **PROVEN**
- Xmind再READ = **PROVEN**
- FigJam Flowchart生成 = **PROVEN**
- FigJam再READ = **PROVEN**
- 階層 vs 工程の比較 = **PROVEN**
- Notionへの実例記録 = **PROVEN**

## 再利用先

- 企画
- 研究計画
- 方法©️
- 自分史
- 本館リニューアル
- Plugin配線
- 長い会話の整理

## Notion正本

https://app.notion.com/p/3e0c10ec598c81a99565c685f5811cd6?pvs=204
