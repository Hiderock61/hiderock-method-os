# 自動化実例004｜Binance→Flourish→Notion｜市場データ可視化

Status: **E2E PROVEN**  
Date: 2026-09-19

## 目的

公開市場データを取得し、

```text
Binance
  ↓
時系列データREAD
  ↓
ChatGPTで小さいCSVへ整形
  ↓
Flourish
  ↓
編集可能チャートへ変換
  ↓
Flourish再READ
  ↓
Notionへ記録
```

まで一続きで通す。

## 試験データ

- Symbol: BTCUSDT
- Interval: 1h
- Bars: 24
- Used value: Close

この実例の目的は売買判断ではなく、Plugin配線の実証。

## Flourish

Visualisation ID: `30301974`

- Template: Line, bar and pie charts
- Uploaded rows: 24
- Headers: TimeUTC / CloseUSDT
- label binding: TimeUTC
- value binding: CloseUSDT
- metadata binding: TimeUTC
- chart_type: line
- facet_layout: single
- aggregation_mode: none
- is_published: false

## 途中の復旧

テンプレートのサンプルデータ由来で、データ差し替え直後にvalue bindingが旧列を指した。

その後、
- label → TimeUTC
- value → CloseUSDT
- metadata → TimeUTC

へ再bindingし、3/3 successful。

設定更新時には入力スキーマが `[{id, value}]` の配列形式であることを確認し、修正後に3設定を再READした。

## 実機状態

- Binance spot kline READ = **PROVEN**
- 24 bars取得 = **PROVEN**
- CSV整形 = **PROVEN**
- Flourish visualisation作成 = **PROVEN**
- Flourish data upload = **PROVEN**
- bindings修正 = **PROVEN**
- chart settings固定 = **PROVEN**
- Flourish data再READ = **PROVEN**
- 未公開状態確認 = **PROVEN**
- Notion記録 = **PROVEN**

## この回路で増えた能力

以前：
外部データを読む、または別途グラフを作る。

今回：
**外部データ → 構造化 → 編集可能チャート → 再検証 → 記録**
を一続きにできた。

## 再利用先

- 市場時系列
- 研究データ
- 実験結果
- Web/API由来の数値
- 公開前の非公開可視化レビュー

## Notion正本

https://app.notion.com/p/3e0c10ec598c81aa9b1bf6b07b442574?pvs=204
