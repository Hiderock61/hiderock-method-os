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
- HOLD / BLOCKED
- PARTIALのまま現実工程が閉じていないもの
- 一般論として「できるはず」の案

それらは成果物047など監査ログ側に残す。

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

```text
GitHub仕事受付ページ
  ↓
Jotform実フォーム
  ↓
4項目・Form ID・状態を照合
  ↓
Notion
```

- Web側4項目 = Form側4項目と一致
- CTA Form ID = READしたForm IDと一致
- Jotform status = ENABLED
- READ-only監査として完走

[実例005 Markdown](./external-capability-automation-example-005.md)

## 次

新しい組み合わせがE2Eで成功した時だけ、
`external-capability-automation-example-006.md` 以降を追加する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本
