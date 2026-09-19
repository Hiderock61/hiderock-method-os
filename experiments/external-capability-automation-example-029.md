# 自動化実例029｜GitHub Issue→Todoist実行タスク化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-20

## 目的

GitHub IssueをTodoistの実行タスクへ変換し、
案件から個人実行までを一本につなぐ。

```text
Airtable
  ↓
Trello
  ↓
Linear
  ↓
GitHub Issue #1
  ↓
Todoist task
  ↓
再READ
```

## Todoist実体

Task:
**本番Web→CTA→Jotform→送信→受信を実機確認する**

Task ID:
`6hXHGM4QpWfP8RC4`

State:
**incomplete**

Priority:
**p4**

## 引き継いだ情報

- GitHub Issue #1 URL
- Linear HID-12 URL
- 元TrelloカードURL
- Submission ID `6652201416321967587`
- 目的
- コード変更 / PR作成は含めないという境界

## 再READ結果

Todoist fetch_objectで再取得し、

- title = MATCH
- GitHub URL = MATCH
- Linear URL = MATCH
- Trello URL = MATCH
- Submission ID = MATCH
- checked = false
- priority = p4

を確認。

## この回路で増えた能力

以前:
GitHub Issueまでコード側の作業入口を作る。

今回:
**Issueを、実際に今日やる個人タスクへ落とせる。**

役割:
- Airtable = 案件DB
- Trello = 現場進行
- Linear = 実装課題
- GitHub Issue = コード側の作業入口
- Todoist = 実行面

## 実機状態

- GitHub Issue source = **PROVEN**
- Todoist add_tasks = **PROVEN**
- link handoff = **PROVEN**
- Submission ID handoff = **PROVEN**
- Todoist fetch_object = **PROVEN**
- content match = **PROVEN**

## 境界

期限、リマインダー、担当者割当は設定していない。
タスク完了操作もしていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81a59fc5e742b567be0d?pvs=204
