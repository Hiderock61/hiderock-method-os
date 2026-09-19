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

```text
GitHub
  ↓
TinyFish ↔ Firecrawl
  ↓
正本と公開Webの差分判定
  ↓
Notion
```

[実例001 Markdown](./external-capability-automation-example-001.md)

### 002｜Web調査→学術根拠監査→正本化｜E2E PROVEN

```text
Firecrawl
  ↓
Scite
  ↓
支持 / 限界の根拠監査
  ↓
Notion
```

[実例002 Markdown](./external-capability-automation-example-002.md)

### 003｜Notion→Xmind＋FigJam｜同一内容の多視点化｜E2E PROVEN

```text
Notion
  ↓
Xmind = 階層・分類
FigJam = 工程・分岐・循環
  ↓
再READして視点差を比較
  ↓
Notion
```

- Notion正本READ = PROVEN
- Xmind生成＋再READ = PROVEN
- FigJam生成＋再READ = PROVEN
- 階層 vs 工程の比較 = PROVEN

[実例003 Markdown](./external-capability-automation-example-003.md)

## 次

新しい組み合わせがE2Eで成功した時だけ、
`external-capability-automation-example-004.md` 以降を追加する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本
