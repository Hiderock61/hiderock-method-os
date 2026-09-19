# 自動化実例041｜Google Calendar metadata→Airtable時間インフラ台帳

Status: **E2E PROVEN**  
Date: 2026-09-20

## 目的

Google Calendarのevent内容には入らず、
calendar-level metadataだけをAirtableへ保存する。

```text
Google Calendar list_calendars
  ↓
get_colors
  ↓
Airtable 時間インフラ台帳
  ↓
reREAD
```

## Calendars

1. Primary calendar
   - primary = true
   - access role = owner
   - color ID = 14

2. 日本の祝日
   - primary = false
   - access role = reader
   - color ID = 8

3. Holidays in Japan
   - primary = false
   - access role = reader
   - color ID = 8

## Airtable

Base:
`appoJtVWhxi2XjOXG`

Table:
**時間インフラ台帳**

Table ID:
`tblnxnz2iKkobcsbS`

## Re-read

- calendar names = 3/3 MATCH
- primary = MATCH
- access roles = 3/3 MATCH
- color IDs = 3/3 MATCH
- color values = 3/3 MATCH

## Audit

- Calendar-level metadata only
- No event body/title/attendees
- Personal email-like calendar ID not copied into Airtable
- Colors resolved from Google Calendar palette

## Proven

- Google Calendar list_calendars = **PROVEN**
- Google Calendar get_colors = **PROVEN**
- Airtable table create = **PROVEN**
- Airtable records create = **PROVEN**
- Airtable reREAD = **PROVEN**

## Boundary

No event search.
No event content read.
No create/update/delete.
No RSVP.

## Notion

https://app.notion.com/p/3e0c10ec598c81d89605d0016393428c?pvs=204
