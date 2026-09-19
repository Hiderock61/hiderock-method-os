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

```text
Podcast App
  ↓
テーマ検索
  ↓
観測軸付きで選別
  ↓
Notion研究カード
  ↓
再READ
```

- 5エピソードを研究カード化
- 5/5再READ一致
- カタログ説明は番組メタデータとして扱う

[実例010 Markdown](./external-capability-automation-example-010.md)

### 011｜Jotform相談→Airtable案件台帳化｜E2E PROVEN（テストデータ）

```text
Jotform
  ↓
相談送信READ
  ↓
Airtable案件台帳
  ↓
再READ
```

- 実機試験用Airtable Baseを使用
- 仕事相談案件テーブルを新規作成
- Jotformテスト送信3件 → Airtable 3 records
- 3/3再READ一致
- 運用DBとして「新規」状態を保持

[実例011 Markdown](./external-capability-automation-example-011.md)

### 012｜Google Drive→Airtable制作資料台帳化｜E2E PROVEN

```text
Google Drive
  ↓
制作資料metadata
  ↓
Airtable資産台帳
  ↓
再READ
```

- 制作・方法系6件を対象
- 本文は読まずmetadataのみ使用
- Airtable「Drive制作資料台帳」を新規作成
- 6 files → 6 records
- 6/6再READ一致

[実例012 Markdown](./external-capability-automation-example-012.md)

### 013｜Airtable案件DB→Trello作業ボード化｜E2E PROVEN（テストデータ）

```text
Airtable
  ↓
案件DB
  ↓
Trelloカンバン
  ↓
新規 / 確認中 / 完了
  ↓
再READ
```

- 非公開テストボード作成
- 3 lists作成
- Airtable 3 records → Trello 3 cards
- 3/3再READ一致

[実例013 Markdown](./external-capability-automation-example-013.md)

### 014｜Airtable案件DB→Trello→Linear課題化｜E2E PROVEN（テストデータ）

```text
Airtable
  ↓
Trello進行カード
  ↓
Linear実装Issue
  ↓
再READ
```

- Airtable案件1件をTrelloカード経由でLinearへ昇格
- HID-12作成
- 元Trelloカードをリンク添付
- Linear再READ一致

[実例014 Markdown](./external-capability-automation-example-014.md)

### 015｜Google Drive資産→Adobe PDFカタログ化｜E2E PROVEN

```text
Google Drive
  ↓
制作資料metadata
  ↓
Adobe PDF
  ↓
properties / render確認
```

- Drive側6資料を再READ
- Adobeで2ページPDF生成
- PDF properties再READ
- PDF→PNG render処理成功
- 独立目視監査のみPARTIAL

[実例015 Markdown](./external-capability-automation-example-015.md)

### 016｜Airtable案件DB→monday.com業務ボード化｜E2E PROVEN（テストデータ）

```text
Airtable
  ↓
案件DB
  ↓
monday.com業務ボード
  ↓
再READ
```

- 非公開テストボード作成
- 5列追加
- Airtable 3 records → monday 3 items
- 状態「新規」を保持
- 3/3再READ一致

[実例016 Markdown](./external-capability-automation-example-016.md)

## READY｜実行可能・実データ待ち

### R-001｜Gmail予定候補↔Google Calendar取りこぼし監査

確認済み：
- Gmail search = PROVEN
- Gmail絞り込み = PROVEN
- Google Calendar一覧READ = PROVEN
- Calendar期間検索 = PROVEN

未実証：
- 実予定メールとCalendar予定のE2E照合

現在札：
**READY / NO TEST DATA**

### R-002｜GitHub実例図鑑→Lucid配線図化

確認済み：
- GitHub INDEX READ = PROVEN
- Mermaid構造生成 = PROVEN
- Lucidchart document create = PROVEN
- Lucid metadata READ = PROVEN
- Lucid document fetch = PROVEN

現在札：
**READY / PARTIAL**

Lucid document:
https://lucid.app/lucidchart/322e7e2b-b674-4c8c-88d2-75a19264ef7f/edit

### R-003｜Dropbox→Airtable資産台帳化

確認済み：
- Dropbox search = PROVEN
- folder READ = PROVEN

未実証：
- 実ファイル→Airtable台帳化

現在札：
**READY / NO TEST DATA**

対象候補フォルダ直下にファイルが無かったため、実データ待ち。

### R-004｜Jotform→HubSpot Contact化

確認済み：
- CONTACT read = AVAILABLE
- test@example.com検索 = 0件

未実証：
- CONTACT create

現在札：
**READY / AUTH GATE**

HubSpot CONTACT write が REQUIRES_REAUTHORIZATION。

### R-005｜Airtable→Slack List作業面化

確認済み：
- Slack channel READ = PROVEN
- Slack public search = PROVEN
- ChatGPT側Slack permission = Allow all actions

未実証：
- Slack List create

現在札：
**READY / AUTH GATE**

Slack Lists追加認証フローが接続エラー。

### R-006｜Fireflies会議ログ→Airtable実務レコード化

確認済み：
- Fireflies transcript query = PROVEN
- mine:true で検索 = PROVEN

未実証：
- summary / action items → Airtable

現在札：
**READY / NO TEST DATA**

自分所有の会議ログが0件だったため、実データ待ち。

### R-007｜GitHub→Netlify/Vercelデプロイ監査

現在札：
**READY / NO DEPLOYMENT DATA**

- Vercel teams = 0
- Netlify team = 1
- Netlify projects = 0

### R-008｜Airtable→SupabaseバックエンドDB化

現在札：
**READY / NO PROJECT**

- Supabase list projects = PROVEN
- projects = 0

### R-009｜Notion→WordPress Draft化

現在札：
**READY / NO SITE**

- WordPress.com connector = PROVEN
- user sites list = PROVEN
- accessible sites = 0

サイトが存在した時点で、
Notion正本 → Draft記事 → 再READ を再実行する。

## 次

新しい組み合わせがE2Eで成功した時だけ、
`external-capability-automation-example-017.md` 以降を追加する。

READY候補は成功番号を消費せず、`R-001 / R-002...` で管理する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本  
READY = 能力は揃っており、実データが来れば試せる回路
