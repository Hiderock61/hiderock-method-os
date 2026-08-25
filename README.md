# ヒデロック発明OS©️

更新: 2026-08-26

これは、ヒデロックが発明した **AI方法©️ / 協働方法©️ / OS / プロトコル / ガイド** を保存し、別部屋・別AIでも読み直して再実行するための公開可能な設計図リポジトリ。

目的は、**AIの長期記憶や特定の会話部屋に依存せず、必要な方法をファイルから読み込んで同じ型で作業できるようにすること**。

> **記憶に頼るAI運用から、設計図を読み込ませるAI運用へ。**

---

## 最初に読む

1. [METHOD_HOME.md](./METHOD_HOME.md) — 発明品の種類と索引
2. [RECOVERY.md](./RECOVERY.md) — 別部屋・別AIへの復旧ルート
3. 必要な個別正本ファイル

### 🎭 BONSAI©️を使いたい場合

一般索引を読む前後どちらでもよいが、**BONSAI©️の初見理解は必ずここから始める**。

- [BONSAI_START_HERE.md](./BONSAI_START_HERE.md) — 「何のための方法か」「劇団員とは何か」をゼロ前提で説明
- [methods/006_hiderock-gekidan-method.md](./methods/006_hiderock-gekidan-method.md) — v0.5実行アルゴリズム
- [methods/006A_hiderock-gekidan-roster.md](./methods/006A_hiderock-gekidan-roster.md) — 全52役・11系統の観測器台帳
- [methods/006B_hiderock-gekidan-emoji-legend.md](./methods/006B_hiderock-gekidan-emoji-legend.md) — 全52役＋構造記号の視覚凡例
- [prompts/bonsai-start-prompt.md](./prompts/bonsai-start-prompt.md) — 別部屋・別AI用コピペ

**重要:** BONSAI©️の「劇団」は寸劇の意味ではない。劇団員は、異なる角度を安定して測るための**観測器 / 認知レンズ**として使う。

---

## 発明品の5分類

- **🤖 AI方法©️**：入力を渡せばAIが主要処理を開始できる。
- **🤝 協働方法©️**：AI処理と人間側の実機・現実行動の往復で成立する。
- **🔑 OS**：生活や作業全体の置き方を決める運用体系。
- **🧰 プロトコル**：正本・登録・復旧など仕組みを守る規則。
- **🧭 ガイド**：人間が現実で動くための探索・行動ガイド。AIは補助役。

---

## 正本の役割分担

- **Notion**：運用正本。日常運用で更新する生きたカード。
- **GitHub / このリポジトリ**：別AIへ渡せる再現用設計図。
- **Hiderock61/hiderock61.github.io `/methods/`**：公開総合索引。

札:

> **Notionに運用正本、GitHubに設計図、本館に入口。**

---

## 別AIへの最短指示

```text
このリポジトリはヒデロック発明OS©️の再現用設計図です。
README.md、METHOD_HOME.md、RECOVERY.md を読み、対象の発明品の正本ファイルを確認してから実行してください。
記憶だけで方法を再現しないでください。
```

BONSAI©️なら:

```text
BONSAI_START_HERE.md を入口にし、006本体・006A全52役台帳・006B絵文字凡例を読んでから実行してください。
```

---

## 主要ファイル

```text
hiderock-method-os/
├── README.md
├── METHOD_HOME.md
├── RECOVERY.md
├── BONSAI_START_HERE.md
├── methods/
│   ├── 001_...
│   ├── ...
│   ├── 006_hiderock-gekidan-method.md
│   ├── 006A_hiderock-gekidan-roster.md
│   ├── 006B_hiderock-gekidan-emoji-legend.md
│   ├── ...
│   └── 019_a-method.md
├── prompts/
│   ├── recovery-prompt.md
│   ├── bonsai-start-prompt.md
│   └── method-registration-prompt.md
└── docs/
```

全発明品の番号・用途・合図は [METHOD_HOME.md](./METHOD_HOME.md) を参照。

---

## 公開方針

このリポジトリには原則として、**方法・構造・再現仕様**を置く。

以下は置かない。

- 住所・電話番号・メールアドレス
- 非公開Notionリンク
- 非公開Googleドキュメントリンク
- 他者の個人情報
- 方法再現に不要な具体的な私生活情報

---

## 最重要思想

> **方法を覚えているAIを探すのではなく、初見AIでも読める方法を外に置く。**

> **再現できるかどうかは、本人との共通知識ではなく、設計図だけで意味と手順が復元できるかで判定する。**
