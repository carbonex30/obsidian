---
aliases:
  - Calendar
  - Timeline
---

# 📅 Calendar Dashboard

> Your timeline — daily notes, meetings, and time-based reflections.
> This is where you **make it whole** by connecting thinking across time.

[[Home Base]] ← Back to Home

---

## 📝 Recent Daily Notes

```dataview
TABLE file.cday AS "Date"
FROM "Calendar/Daily Notes"
SORT file.name DESC
LIMIT 14
```

---

## 🤝 Recent Meetings

```dataview
TABLE date AS "Date", attendees AS "Attendees"
FROM "Calendar/Meetings"
SORT date DESC
LIMIT 10
```

---

## 📆 Daily Notes by Month

> Browse your daily notes grouped by month.

```dataview
TABLE length(rows) AS "# Notes"
FROM "Calendar/Daily Notes"
GROUP BY dateformat(file.cday, "yyyy-MM") AS "Month"
SORT rows[0].file.cday DESC
```

---

## 🕰️ On This Day — Across All Years

> Notes created on today's date in previous years.

```dataview
LIST
FROM ""
WHERE file.cday.month = date(today).month
  AND file.cday.day = date(today).day
  AND file.cday.year != date(today).year
SORT file.cday ASC
```

---

> [!tip] Quick Actions
> - **Create today's daily note:** `Cmd+D` / `Ctrl+D` (or use Daily Notes plugin)
> - **Template:** Use `Templates/Daily Note Template` for consistent structure
> - **Meeting note:** Create a new note in `Calendar/Meetings/` using the Meeting Note Template
