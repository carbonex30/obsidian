<%*
const noteDate = moment(tp.file.title, "YYYY-MM-DD");
const prevDay  = noteDate.clone().subtract(1, "days").format("YYYY-MM-DD");
const nextDay  = noteDate.clone().add(1, "days").format("YYYY-MM-DD");
const dayName  = noteDate.format("dddd");
_%>
---
tags:
  - daily-note
---

# <% tp.file.title %> — <% dayName %>

**← [[<% prevDay %>]]** | [[Home Base]] ← Home | [[Calendar Dashboard]] ← Calendar | **[[<% nextDay %>]] →**

---

## 🌅 Morning Intentions

> *What do I want to focus on today?*

- 

---

## 📝 Notes & Thoughts

*Capture ideas, observations, and thoughts throughout the day.*



---

## ✅ Tasks

- [ ] 

---

## 🌙 Evening Reflection

> *What went well? What did I learn? What am I grateful for?*



---

## 🕰️ On This Day

> Notes created on this date in previous years.

```dataview
LIST
FROM ""
WHERE file.cday.month = this.file.cday.month
  AND file.cday.day = this.file.cday.day
  AND file.cday.year != this.file.cday.year
SORT file.cday ASC
```

---

**← [[<% prevDay %>]]** | **[[<% nextDay %>]] →**
