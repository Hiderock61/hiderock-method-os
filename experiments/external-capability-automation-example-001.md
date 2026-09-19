# 自動化実例001｜本館・公開監査ルート

Status: **E2E PROVEN**  
Date: 2026-09-19

## これは何か

85系統のPlugin能力を組み合わせて、実際に1本通った自動化例。

各Pluginの単体能力ではなく、

> 複数Pluginを配線すると、現実の仕事を1工程自動監査できた

という実例を残す。

## 目的

GitHubの本館正本と、実際に公開されているWebサイトが一致しているかを確認する。

## 配線

```text
GitHub
  ↓
正本READ
  ↓
TinyFish ↔ Firecrawl
  ↓
公開Web二眼観測
  ↓
正本と公開物の差分判定
  ↓
Notionへ監査結果を記録
```

## 実際に起きたこと

本館Heroの「仕事の相談」リンクをGitHubで変更した。

変更直後は、

- GitHub正本 = 新リンク
- 公開Web = 旧リンク

だった。

ここで、

> WRITE成功 ≠ Deploy成功 ≠ 公開反映成功

を実機で確認した。

その後、再監査すると、

- GitHub = 新リンク
- TinyFish = 新リンク
- Firecrawl = 新リンク

へ揃ったため、公開反映まで確認できた。

## 実機状態

- GitHub正本READ = PROVEN
- TinyFish公開READ = PROVEN
- Firecrawl公開READ = PROVEN
- TinyFish ↔ Firecrawl 二眼比較 = PROVEN
- 正本 ↔ 公開差分判定 = PROVEN
- Notion記録 = PROVEN
- 主要5導線監査 = 5/5 PASS

## 主要5導線

1. 仕事 → `/ononoke-holdings/`
2. 代表アプリ → `/new-kit-gaw/`
3. 方法 → `/methods/`
4. 自分史 → `/music-history/`
5. 外付け能力棚 → `/akechi-port/`

## 判定ロジック

- GitHub = 新 / TinyFish = 新 / Firecrawl = 新 → PASS
- GitHub = 新 / TinyFish = 旧 / Firecrawl = 旧 → HOLD / 公開反映待ち
- TinyFish ≠ Firecrawl → SENSOR DIFF
- GitHub hrefなし → SOURCE MISSING
- 公開リンクあり / 遷移先READ失敗 → DESTINATION FAIL

## 今回使ったPlugin

- GitHub
- TinyFish
- Firecrawl
- Notion

## PROVEN範囲に含めないもの

Linear連携は設計・READ確認まで行ったが、実際のFAIL発生時Issue作成は未実行。

したがって、

- Linear Workspace READ = PROVEN
- Linear Team READ = PROVEN
- Linear Issue検索 = PROVEN
- FAIL → Linear Issue作成 = NOT YET PROVEN

とする。

## 再利用先

この回路は、本館以外にも応用できる。

- Webサイト公開確認
- リンク切れ監査
- デプロイ後確認
- 公開ドキュメント差分確認
- 外部サービス表示確認

## 位置づけ

監査ルーム = 部品検査  
配線ルーム = 実際に使える部品を組んで仕事にする

このファイルは、その最初の完成例。

## Notion正本

https://app.notion.com/p/3e0c10ec598c8106b0cfeb68fbeba861?pvs=204
