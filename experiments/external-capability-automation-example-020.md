# 自動化実例020｜GitHub成功図鑑→Miro配線俯瞰表

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

GitHubの自動化実例INDEXにある成功回路001〜019を、
Miro上の俯瞰表へ変換する。

```text
GitHub INDEX
  ↓
成功実例001〜019抽出
  ↓
Miro既存テストボード
  ↓
表作成
  ↓
19行投入
  ↓
Miro再READ
```

## Miro実体

Board:
**能力棚 #029｜Miro実機試験**

Table:
**成功回路テスト**

Widget URL:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684275829371

## 列

- 実例名
- 主回路

## 再READ結果

Miroから全行を再取得。

- total rows = **19**
- 001〜019すべて確認
- 実例名 = **MATCH**
- 主回路 = **MATCH**

**19 / 19 MATCH**

## 権限差の発見

### 雪だるま系譜マップ
- board search / READ = **PROVEN**
- table create = **Access forbidden**

### 能力棚 #029｜Miro実機試験
- board search / READ = **PROVEN**
- table create = **PROVEN**
- table rows write = **PROVEN**
- table rows reREAD = **PROVEN**

監査ルール:
**Miro接続済み ≠ すべての既存ボードへWRITE可能**

## この回路で増えた能力

以前:
GitHub図鑑をMarkdownとして読む。

今回:
**成功回路群をMiro上の俯瞰盤へ展開し、一覧として再利用できる。**

## 実機状態

- GitHub INDEX READ = **PROVEN**
- Miro board search = **PROVEN**
- existing test board write = **PROVEN**
- Miro table create = **PROVEN**
- 19 rows write = **PROVEN**
- Miro table reREAD = **PROVEN**
- 19/19一致 = **PROVEN**
- board_show = **PROVEN**

## 境界

メインの雪だるま系譜ボードはWRITE不可。
実機試験用ボードを使用。

今回は表形式のみ。
コネクタ付きネットワーク図や自動レイアウトは未実施。

## Notion正本

https://app.notion.com/p/3e0c10ec598c812fb422de207b169fc7?pvs=204
