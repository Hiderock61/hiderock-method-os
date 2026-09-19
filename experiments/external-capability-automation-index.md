# 自動化実例図鑑｜External Capability Automation Examples

このファイルは、Plugin単体の能力表ではなく、**複数Pluginを組み合わせて実際に通った自動化回路**だけを残す索引。

## 昇格条件

次の4条件を満たしたものだけ `実例00X` として追加する。

1. 複数Pluginを実際に組み合わせた
2. 現実の工程が1つ以上進んだ
3. 実行結果を再READまたは別センサーで確認できた
4. PROVEN範囲と未実証範囲を分けて書ける

## 保存先

成功したら毎回、同じ実例を2か所へ残す。

- **Notion**：背景、意味、使い道、次に何が増えたか
- **GitHub**：配線、判定ロジック、PROVEN範囲、再利用可能なMarkdown

## 図鑑へ入れないもの

- 単体Pluginの接続確認だけ
- ツール露出だけ
- BLOCKED
- 一般論として「できるはず」の案

HOLD / PARTIALでも、**構成能力が確認済みで、実データ待ちだけのもの**は READY 候補として別欄へ残す。

## 実例一覧

### 001｜本館・公開監査自動化｜E2E PROVEN
[実例001 Markdown](./external-capability-automation-example-001.md)

### 002｜Web調査→学術根拠監査→正本化｜E2E PROVEN
[実例002 Markdown](./external-capability-automation-example-002.md)

### 003｜Notion→Xmind＋FigJam｜同一内容の多視点化｜E2E PROVEN
[実例003 Markdown](./external-capability-automation-example-003.md)

### 004｜Binance→Flourish→Notion｜市場データ可視化｜E2E PROVEN
[実例004 Markdown](./external-capability-automation-example-004.md)

### 005｜GitHub仕事受付↔Jotform整合監査｜E2E PROVEN
[実例005 Markdown](./external-capability-automation-example-005.md)

### 006｜公開サイト→Xmind導線地図化｜E2E PROVEN
[実例006 Markdown](./external-capability-automation-example-006.md)

### 007｜GitHub図鑑→Coda台帳化｜E2E PROVEN
[実例007 Markdown](./external-capability-automation-example-007.md)

### 008｜Jotform相談→Notion案件カード化｜E2E PROVEN（テストデータ）

```text
Jotform
  ↓
送信内容READ
  ↓
1件ずつ構造化
  ↓
Notion案件カード
  ↓
再READ
```

- 既存テスト送信3件
- Notion案件カード3件作成
- 3/3再READ一致
- 返信・案件受諾など外部アクションは含めない

[実例008 Markdown](./external-capability-automation-example-008.md)

## READY｜実行可能・実データ待ち

### R-001｜Gmail予定候補↔Google Calendar取りこぼし監査

```text
Gmail
  ↓
予定候補抽出
  ↓
Google Calendar
  ↓
登録済み / 未登録 / 判断不能
  ↓
Notion
```

確認済み：
- Gmail search = PROVEN
- Gmail絞り込み = PROVEN
- Google Calendar一覧READ = PROVEN
- Calendar期間検索 = PROVEN

未実証：
- 実予定メールとCalendar予定のE2E照合

現在札：
**READY / NO TEST DATA**

実予定メールと比較対象Calendar予定が揃ったら再実行し、通ればその時点の次の空き成功番号へ昇格する。

### R-002｜GitHub実例図鑑→Lucid配線図化

```text
GitHub INDEX
  ↓
Mermaidへ構造化
  ↓
Lucidchart
  ↓
配線図
```

確認済み：
- GitHub INDEX READ = PROVEN
- Mermaid構造生成 = PROVEN
- Lucidchart document create = PROVEN
- Lucid metadata READ = PROVEN
- Lucid document fetch = PROVEN

現在の制約：
- Mermaid図がLucid側では1つの埋め込み図ブロックとして返る
- 内部ノード文字をLucid自身から再READできない
- document searchでも 001 / GitHub / Notion / 007 はヒットしない

現在札：
**READY / PARTIAL**

Lucid側でMermaid内部ノードを構造READできる手段が露出したら再監査する。

Lucid document:
https://lucid.app/lucidchart/322e7e2b-b674-4c8c-88d2-75a19264ef7f/edit

## 次

新しい組み合わせがE2Eで成功した時だけ、
`external-capability-automation-example-009.md` 以降を追加する。

READY候補は成功番号を消費せず、`R-001 / R-002...` で管理する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本  
READY = 能力は揃っており、実データが来れば試せる回路
