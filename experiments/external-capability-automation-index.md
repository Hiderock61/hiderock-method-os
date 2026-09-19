# 自動化実例図鑑｜External Capability Automation Examples

このファイルは、Plugin単体の能力表ではなく、**複数Pluginを組み合わせて実際に通った自動化回路**だけを残す索引。

## 昇格条件
次の4条件を満たしたものだけ `実例00X` として追加する。

1. 複数Pluginを実際に組み合わせた
2. 現実の工程が1つ以上進んだ
3. 実行結果を再READまたは別センサーで確認できた
4. PROVEN範囲と未実証範囲を分けて書ける

## 実例一覧

001〜021は既存正本を参照。

### 022｜GitHub成功図鑑→Plugin頻度集計→Flourish可視化｜E2E PROVEN

```text
GitHub INDEX
  ↓
001〜021の主回路集計
  ↓
Plugin出現回数
  ↓
Flourish bar chart
  ↓
再READ
```

- 24 Pluginを集計
- Notion 9
- Airtable 9
- GitHub 4
- Xmind 3
- Jotform 3
- Flourish visualisation ID 30302746
- is_published = false

[実例022 Markdown](./external-capability-automation-example-022.md)

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
`external-capability-automation-example-023.md` 以降を追加する。

READY候補は成功番号を消費せず、`R-001 / R-002...` で管理する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本  
READY = 能力は揃っており、実データが来れば試せる回路
