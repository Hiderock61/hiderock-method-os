# 自動化実例021｜Canva→Airtable制作資産台帳化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

Canvaにある既存デザインを正式メタデータ付きでAirtableへ棚卸しする。

```text
Canva
  ↓
owned designs search
  ↓
get_design
  ↓
正式metadata
  ↓
Airtable制作資産台帳
  ↓
再READ
```

## 対象5件

1. 能力棚🔌｜外付け能力接続ランタイム
   - Canva Design ID: `DAHVKED22io`
2. 青と緑 抽象的 アート ストーリー
   - Canva Design ID: `DAHIej18D4A`
3. 人生から「さぁ、どうする？」と問われた日
   - Canva Design ID: `DAG4K1lXgIE`
4. Canva 10デザインマイルストーンバッジ
   - Canva Design ID: `DAGamprKzWM`
5. Today I work from home. Girl with laptop instagram stories
   - Canva Design ID: `DAGZPfpcOck`

## Airtable実体

Base:
**実機試験#056｜Airtable最小テスト**

Base ID:
`appoJtVWhxi2XjOXG`

Table:
**Canva制作資産台帳**

Table ID:
`tblpawEmztmN6uxO5`

## フィールド

- タイトル
- Canva Design ID
- ページ数
- 作成日時
- 更新日時
- Design Type
- View URL

## 再READ結果

5件をAirtableから再取得し、
タイトル / Design ID / page count / created_at / updated_at / design type / view URL を確認。

**5 / 5 MATCH**

## この回路で増えた能力

以前:
Canvaの中で個別デザインを見る。

今回:
**Canvaの制作資産を、横断検索・棚卸しできる外部DBへ変換できる。**

Google Drive資産台帳と並べることで、
文書資産とデザイン資産を別棚で管理できる。

## 実機状態

- Canva owned design search = **PROVEN**
- Canva get_design ×5 = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create ×5 = **PROVEN**
- Airtable再READ = **PROVEN**
- 5/5一致 = **PROVEN**

## 境界

デザイン内容そのものの品質評価や画像解析はしていない。
メタデータのみを使用。

新規デザイン生成、編集、公開、共有変更は行っていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81e0a515f7fa4bb30bb5?pvs=204
