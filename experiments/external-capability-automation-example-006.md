# 自動化実例006｜公開サイト→Xmind導線地図化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

公開中のWebサイトを外側から読み、

```text
TinyFish
  ↓
公開ページ本文＋リンク抽出
  ↓
内部導線 / 外部出口を分類
  ↓
Xmind
  ↓
Tree Chart化
  ↓
Xmind再READ
  ↓
Notion
```

まで一続きで通す。

## 対象

`https://hiderock61.github.io/`

## Xmind上位枝

1. 本館トップ
2. 代表作品・アプリ
3. Web制作ポートフォリオ
4. 正本・背景
5. アーカイブ
6. 外部出口

## Xmind実体

File ID: `UYKYOFjp`

https://app.xmind.com/share/UYKYOFjp

## 途中の部品交換

最初にFirecrawlで試した。

- map = トップ1件のみ → PARTIAL
- crawl = HTTP 429 → HOLD

そこで公開READ担当をTinyFishへ差し替えた。

TinyFishでは、
- 本館本文
- 内部リンク群
- 外部リンク群

を取得でき、そのままXmind化まで完走した。

## 実機状態

- Firecrawl map = **PARTIAL**
- Firecrawl crawl = **HOLD / 429**
- TinyFish public READ = **PROVEN**
- TinyFish link extraction = **PROVEN**
- 内部 / 外部分類 = **PROVEN**
- Xmind Tree Chart生成 = **PROVEN**
- Xmind再READ = **PROVEN**
- Notion記録 = **PROVEN**

## この回路で増えた能力

以前：
サイトを1ページずつ読む。

今回：
**公開サイトの導線を、外から見えているリンク関係として一枚の階層図へ変換できる。**

## 再利用先

- 本館リニューアル前後比較
- 大きなサイトの入口監査
- ポートフォリオ棚の増築確認
- リンク構造の俯瞰
- サービスサイトの導線棚卸し

## 重要

1部品がHOLDでも、
同じ役割を持つ別Pluginへ差し替えて本筋を完走できる。

## Notion正本

https://app.notion.com/p/3e0c10ec598c815fafbad541c6b32e41?pvs=204
