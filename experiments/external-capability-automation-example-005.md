# 自動化実例005｜GitHub仕事受付↔Jotform整合監査

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

Webページに書いてある受付仕様と、実際の入力フォームがズレていないかを監査する。

```text
GitHub
  ↓
仕事受付ページREAD
  ↓
Jotform
  ↓
実フォームREAD
  ↓
ChatGPT
  ↓
項目・ID・状態を照合
  ↓
Notion
```

## GitHub側

対象：
`ononoke-holdings/index.html`

「最初にあると助かる4つ」：

1. 今どうなっている？
2. どうなれば助かる？
3. 参考資料やURLはある？（任意）
4. 返信先

CTA:
`https://www.jotform.com/262565341165053`

## Jotform側

- Form ID: `262565341165053`
- Title: 仕事相談受付（オノノケホールディングス）
- Status: ENABLED
- Submission count: 3

入力項目：
- 今どうなっていますか？
- どうなれば助かりますか？
- 参考にできる資料やURLがあれば教えてください（任意）
- 返信先メールアドレス

## 照合結果

Web側4項目とForm側4項目は意味対応で一致。

- 現状 = 一致
- 望む状態 = 一致
- 参考資料 / URL = 一致
- 返信先 = 一致

CTAのForm IDとREADしたForm IDも一致。

## この回路で増えた能力

以前：
Webページとフォームを別々に見る。

今回：
**ページ上の約束と実フォームの実装が一致しているかを監査できる。**

## 実機状態

- GitHub page READ = **PROVEN**
- CTA Form ID抽出 = **PROVEN**
- Jotform form READ = **PROVEN**
- status READ = **PROVEN**
- questions READ = **PROVEN**
- 仕様↔質問項目照合 = **PROVEN**
- Notion記録 = **PROVEN**

## 再利用先

- サービスページ ↔ 問い合わせフォーム
- LP ↔ 申込フォーム
- イベント案内 ↔ 申込フォーム
- 求人ページ ↔ 応募フォーム
- FAQ ↔ 問い合わせカテゴリ

## 注意

フォームの新規作成、編集、送信テストはしていない。
今回はREAD-only監査として完走。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81dfa764f48bdc77c3d0?pvs=204
