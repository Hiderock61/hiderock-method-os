# 自動化実例017｜Airtable案件DB→monday.com→Vibe内部アプリ化

Status: **E2E PROVEN（テストデータ）**  
Date: 2026-09-19

## 目的

Airtableの仕事相談案件をmonday.comの業務ボードへ展開し、
そのボード自体から内部用トリアージアプリを生成する。

```text
Airtable
  ↓
案件DB
  ↓
monday.com
  ↓
業務ボード
  ↓
monday Vibe
  ↓
内部用トリアージアプリ
  ↓
READY / LIVE code version
  ↓
コード再確認
```

## Vibe実体

App:
**Job Triage Board**

App ID:
`10522390`

Editor:
https://akechikuncoms-team.monday.com/vibe/app/10522390

Variant:
**BOARD_VIEW**

Published:
**false**

## Code Version

Version:
**1｜Initial version**

Version ID:
`89f77963-3368-4f04-9ac1-c7b80a179486`

Status:
**LIVE**

Deployed:
`2026-09-19T09:06:02.699Z`

## 完成状態

- status = **READY**
- is_busy = **false**
- is_published = **false**
- code version 1 = **LIVE**

## Vibe ASKによる再確認

現在コードをREAD-onlyで確認。

表示項目:
- 案件名
- Submission ID
- 現状
- 望む状態
- 参考URL
- 状態

機能:
- 状態別タブ
- 件数バッジ
- 案件名リアルタイム検索
- 受付日時による並び替え
- monday.com上のステータス管理

確認結果:
- 外部公開機能 = **なし**
- 自動メール送信 = **なし**
- 外部API送信 = **なし**

## この回路で増えた能力

以前:
Airtable → monday.com で業務台帳を作る。

今回:
**業務ボードそのものから、専用の内部UIを生成できる。**

つまり、
**データ → 業務面 → 専用アプリ**
まで接続できた。

## 実機状態

- Airtable案件DB = **PROVEN**
- monday board = **PROVEN**
- Vibe app create = **PROVEN**
- board接続 = **PROVEN**
- generated code = **PROVEN**
- deploy = **PROVEN**
- status READY = **PROVEN**
- code version LIVE = **PROVEN**
- Vibe ASKコード再確認 = **PROVEN**
- 非公開状態 = **PROVEN**

## 境界

実顧客データではなく既存テスト相談3件を使用。
外部公開、メール送信、課金、予約、通知は行っていない。

## Notion正本

https://app.notion.com/p/3e0c10ec598c8135aef4e99e880cfb6f?pvs=204
