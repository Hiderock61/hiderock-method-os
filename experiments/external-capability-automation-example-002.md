# 自動化実例002｜Web調査→学術根拠監査→正本化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

Web上の主張をそのまま採用せず、

```text
Firecrawl
  ↓
Web / Research検索
  ↓
Scite
  ↓
学術論文・引用文脈・本文抜粋で監査
  ↓
ChatGPT
  ↓
支持側と限界側を分離して統合
  ↓
Notion
```

まで一つの回路として通す。

## 試験テーマ

**RAGはLLMのハルシネーションをどこまで減らせるか**

## Firecrawl観測

Web / research検索で、
- RAGをハルシネーション低減策として扱う研究
- hybrid retrievalなど検索品質改善の研究
- 検索失敗・ノイズ・誤情報がRAG自身の誤りを増やす限界

の両側を取得。

## Scite監査

Sciteでは、
- RAGが外部知識でLLMをgroundingし、精度・信頼性を改善する方向の論文
- retrieval noise / irrelevant context / misleading evidence / internal knowledge conflict
- evidence不足時に回答を控える abstention

を扱う論文群を別クエリで取得。

## 結論

> RAGはハルシネーション低減に有力だが、検索品質が悪いと誤情報やノイズを生成側へ注入する。  
> したがって「RAGを付ければ安全」ではなく、retrieval quality・reranking・evidence alignment・abstentionまで含めた監査が必要。

## 実機状態

- Firecrawl web / research search = **PROVEN**
- Scite literature search = **PROVEN**
- Scite citation context / excerpt取得 = **PROVEN**
- 支持側・限界側の二方向検索 = **PROVEN**
- 統合判定 = **PROVEN**
- Notion正本化 = **PROVEN**
- Tavily = **今回不使用 / 接続失敗HOLD**

## この回路で増えた能力

以前：
Web検索と論文検索を別々に見る。

今回：
**Web側の主張を学術側で二重監査してから正本化する。**

## 再利用先

- AIニュースの話題→論文監査
- 技術記事の根拠確認
- 商品・サービスの技術主張の裏取り
- 方法©️の外部根拠確認
- 研究テーマの初期スクリーニング

## 注意

Tavilyはこの回路の必須部品ではない。
接続復旧後は前段検索センサーとして追加可能。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81bf9677c66a30ffc513?pvs=204
