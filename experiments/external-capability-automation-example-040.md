# 自動化実例040｜HubSpot Contact schema→Airtable CRM項目設計台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

HubSpotの実Contact recordには触れず、
Contact objectのproperty definitionsを
AirtableのCRM項目設計台帳へ保存する。

```text
HubSpot CONTACT schema
  ↓
search_properties
  ↓
get_properties
  ↓
Airtable CRM項目設計台帳
  ↓
reREAD
```

## Contact object access

- read: AVAILABLE
- write: REQUIRES_REAUTHORIZATION

No write was attempted.

## Fields

- email
- phone
- company
- jobtitle
- lifecyclestage

Types:
- 4 × string
- 1 × enumeration

Lifecycle Stage options:
- Subscriber
- Lead
- Marketing Qualified Lead
- Sales Qualified Lead
- Opportunity
- Customer
- Evangelist
- Other

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**CRM項目設計台帳**

Table ID:
`tbl5sQiIVXlRY3hhV`

## Re-read

- Property = 5/5 MATCH
- Label = 5/5 MATCH
- Type = 5/5 MATCH
- Description = 5/5 MATCH
- Lifecycle Stage options = MATCH
- read status = AVAILABLE
- write status = REQUIRES_REAUTHORIZATION

## Audit

- Schema only
- No contact records
- Preserve enumeration values from HubSpot
- Do not treat reauthorization-gated write as available

## Proven

- HubSpot get_user_details = **PROVEN**
- HubSpot search_properties = **PROVEN**
- HubSpot get_properties = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No contact read.
No contact create/update.
No associations.
No write reauthorization.

## Notion

https://app.notion.com/p/3e0c10ec598c814cb18ded21b3a058af?pvs=204
