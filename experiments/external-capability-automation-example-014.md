# 自動化実例014｜Airtable案件DB→Trello→Linear課題化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-19

## 目的

Airtableに保存された案件をTrelloで進行管理し、
必要な1件だけをLinearの実装課題へ昇格する。

```text
Airtable
  ↓
案件DB
  ↓
Trello
  ↓
進行カード
  ↓
Linear
  ↓
実装Issue
  ↓
再READ
```

## 元データ

Airtableの仕事相談案件テーブルから、
Submission ID `6652201416321967587` のテスト案件を使用。

## Trello

Card:
**本番公開テスト｜相談受付導線**

URL:
https://trello.com/c/nMEA3bpz/1-%E6%9C%AC%E7%95%AA%E5%85%AC%E9%96%8B%E3%83%86%E3%82%B9%E3%83%88%EF%BD%9C%E7%9B%B8%E8%AB%87%E5%8F%97%E4%BB%98%E5%B0%8E%E7%B7%9A

## Linear

Issue:
**HID-12｜実機試験｜相談受付導線の確認**

URL:
https://linear.app/hiderock/issue/HID-12/実機試験相談受付導線の確認

Status:
**Backlog**

## 引き継いだ情報

- Submission ID
- 現状
- 望む状態
- 元TrelloカードURL

## 再READ結果

Linear get_issue で以下を再確認。

- title = MATCH
- Submission ID = MATCH
- 現状 = MATCH
- 望む状態 = MATCH
- Trello link = MATCH
- status = Backlog

## この回路で増えた能力

以前:
案件をTrello上で動かす。

今回:
**進行中の作業から、実装が必要なものだけLinearの開発課題へ昇格できる。**

## 実機状態

- Airtable案件DB = **PROVEN**
- Trello card = **PROVEN**
- Linear issue create = **PROVEN**
- Trello link attachment = **PROVEN**
- Linear get_issue再READ = **PROVEN**
- 内容一致 = **PROVEN**

## 境界

今回はテスト案件1件のみ。
担当者割当、優先度変更、完了処理、通知は行っていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81d8ad28c6b372ed95b4?pvs=204
