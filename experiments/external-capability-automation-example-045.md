# 自動化実例045｜Jotform＋HubSpot→Miro受付→CRM項目翻訳盤

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Jotformの仕事相談フォームschemaと
HubSpot Contact標準property schemaを比較し、
実データ同期前のfield mapping監査を行う。

```text
Jotform form schema ─┐
                     ├→ Miro 受付→CRM項目翻訳盤 → reREAD
HubSpot CONTACT schema ┘
```

## Jotform inputs

- 今どうなっていますか？
- どうなれば助かりますか？
- 参考にできる資料やURLがあれば教えてください（任意）
- 返信先メールアドレス

## HubSpot candidates

- email
- message
- website

## Mapping audit

| Jotform | HubSpot | Status |
|---|---|---|
| 今どうなっていますか？ | message | CANDIDATE |
| どうなれば助かりますか？ | message | CANDIDATE / COLLISION |
| 参考資料やURL | website | NOT SAFE |
| 返信先メール | email | DIRECT |

## Key finding

HubSpot標準Contact propertyだけでは、
Jotform 4入力を安全に1対1保持できない。

- 現状と望む状態がmessageへ衝突
- websiteは参考資料URLと意味が違う
- emailだけはdirect mapping可能

## Miro

Table:
**受付→CRM項目翻訳盤｜Jotform × HubSpot**

Widget:
https://miro.com/app/board/uXjVHnIlKBU=/?moveToWidget=3458764684302513366

## Re-read

- input = 4/4 MATCH
- candidate = 4/4 MATCH
- type = 4/4 MATCH
- mapping status = 4/4 MATCH
- rationale = 4/4 MATCH

## Audit

- No submission read
- No contact record read
- No automatic mapping by similar names
- No custom-property creation
- No HubSpot write reauthorization

## Proven

- Jotform form schema READ = **PROVEN**
- HubSpot property schema READ = **PROVEN**
- HubSpot property search = **PROVEN**
- Miro table create = **PROVEN**
- Miro row sync = **PROVEN**
- Miro reREAD = **PROVEN**

## Boundary

No submission data.
No contact data.
No CRM write.
No form edit.

## Notion

https://app.notion.com/p/3e0c10ec598c81f69a34c123680ce8e6?pvs=204
