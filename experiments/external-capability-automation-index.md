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
[実例008 Markdown](./external-capability-automation-example-008.md)

### 009｜Consensus→Xmind研究地図化｜E2E PROVEN
[実例009 Markdown](./external-capability-automation-example-009.md)

### 010｜Podcast App→Notion研究棚化｜E2E PROVEN
[実例010 Markdown](./external-capability-automation-example-010.md)

### 011｜Jotform相談→Airtable案件台帳化｜E2E PROVEN（テストデータ）
[実例011 Markdown](./external-capability-automation-example-011.md)

### 012｜Google Drive→Airtable制作資料台帳化｜E2E PROVEN
[実例012 Markdown](./external-capability-automation-example-012.md)

### 013｜Airtable案件DB→Trello作業ボード化｜E2E PROVEN（テストデータ）
[実例013 Markdown](./external-capability-automation-example-013.md)

### 014｜Airtable案件DB→Trello→Linear課題化｜E2E PROVEN（テストデータ）
[実例014 Markdown](./external-capability-automation-example-014.md)

### 015｜Google Drive資産→Adobe PDFカタログ化｜E2E PROVEN
[実例015 Markdown](./external-capability-automation-example-015.md)

### 016｜Airtable案件DB→monday.com業務ボード化｜E2E PROVEN（テストデータ）
[実例016 Markdown](./external-capability-automation-example-016.md)

### 017｜Airtable案件DB→monday.com→Vibe内部アプリ化｜E2E PROVEN（テストデータ）

```text
Airtable
  ↓
monday.com業務ボード
  ↓
monday Vibe
  ↓
内部用トリアージアプリ
  ↓
READY / LIVE
```

- App ID 10522390
- Job Triage Board
- code version 1 = LIVE
- status = READY
- is_published = false
- Vibe ASKで表示項目・フィルタ・外部送信なしを再確認

[実例017 Markdown](./external-capability-automation-example-017.md)

## READY｜実行可能・実データ待ち

### R-001｜Gmail予定候補↔Google Calendar取りこぼし監査
**READY / NO TEST DATA**

### R-002｜GitHub実例図鑑→Lucid配線図化
**READY / PARTIAL**

### R-003｜Dropbox→Airtable資産台帳化
**READY / NO TEST DATA**

### R-004｜Jotform→HubSpot Contact化
**READY / AUTH GATE**

### R-005｜Airtable→Slack List作業面化
**READY / AUTH GATE**

### R-006｜Fireflies会議ログ→Airtable実務レコード化
**READY / NO TEST DATA**

### R-007｜GitHub→Netlify/Vercelデプロイ監査
**READY / NO DEPLOYMENT DATA**

### R-008｜Airtable→SupabaseバックエンドDB化
**READY / NO PROJECT**

### R-009｜Notion→WordPress Draft化
**READY / NO SITE**

## 次

新しい組み合わせがE2Eで成功した時だけ、
`external-capability-automation-example-018.md` 以降を追加する。

READY候補は成功番号を消費せず、`R-001 / R-002...` で管理する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本  
READY = 能力は揃っており、実データが来れば試せる回路
