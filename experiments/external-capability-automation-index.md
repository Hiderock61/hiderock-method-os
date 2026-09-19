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

- GitHub正本READ = PROVEN
- TinyFish公開READ = PROVEN
- Firecrawl公開READ = PROVEN
- 二眼比較 = PROVEN
- 正本↔公開差分判定 = PROVEN
- Notion記録 = PROVEN
- 主要5導線監査 = 5/5 PASS

[実例001 Markdown](./external-capability-automation-example-001.md)

## 次

新しい組み合わせがE2Eで成功した時だけ、

- `external-capability-automation-example-002.md`
- `external-capability-automation-example-003.md`

のように追加する。

監査ルーム = 部品検査  
配線ルーム = 組み合わせ発見  
この図鑑 = 成功して使える回路の完成見本
