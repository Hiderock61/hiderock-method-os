# 自動化実例028｜Linear→GitHub Issue実装入口化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-20

## 目的

Airtable → Trello → Linearまで進んでいた相談受付課題を、
GitHub本館repoのIssueへ渡してコード側の作業入口にする。

```text
Airtable
  ↓
Trello
  ↓
Linear HID-12
  ↓
GitHub Issue #1
  ↓
再READ
```

## GitHub実体

Repository:
`Hiderock61/hiderock61.github.io`

Issue:
**#1｜実機試験｜相談受付導線の確認**

URL:
https://github.com/Hiderock61/hiderock61.github.io/issues/1

State:
**open**

## 引き継いだ情報

- Linear HID-12 URL
- 元TrelloカードURL
- Submission ID `6652201416321967587`
- 現状
- 望む状態
- 実機試験メモ

## 再READ結果

GitHub fetch_issueで再取得し、

- issue number = 1
- title = MATCH
- state = open
- Linear link = MATCH
- Trello link = MATCH
- Submission ID = MATCH
- 現状 = MATCH
- 望む状態 = MATCH

を確認。

## この回路で増えた能力

以前:
Linearで実装課題として管理する。

今回:
**実装課題を実際のコードrepo側のIssueへ渡せる。**

役割:
- Airtable = 案件DB
- Trello = 現場進行
- Linear = 実装課題
- GitHub Issue = コード側の作業入口

## 実機状態

- Linear issue READ = **PROVEN**
- GitHub create_issue = **PROVEN**
- Linear link handoff = **PROVEN**
- Trello link handoff = **PROVEN**
- Submission ID handoff = **PROVEN**
- GitHub fetch_issue = **PROVEN**
- content match = **PROVEN**

## 境界

コード変更、branch作成、commit、PR作成は行っていない。
今回はIssue化まで。

## Notion正本

https://app.notion.com/p/3e0c10ec598c81c6b4d6e542c83390af?pvs=204
