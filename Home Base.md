---
aliases:
  - Home
  - Dashboard
  - HQ
---

# 🏠 Home Base

> *Your central command center. Everything starts here.*

---

## 🕐 Recently Modified

> Pick up exactly where you left off — vault-wide activity stream, always current.
> → [[Recents]] for full view by area

```dataview
TABLE WITHOUT ID dateformat(file.mtime, "MM/dd/yy HH:mm") AS "Modified", file.folder AS "Area", file.link AS "File"
FROM ""
WHERE !contains(file.folder, "Templates")
  AND file.name != "Home Base"
  AND file.name != "Recents"
SORT file.mtime DESC
LIMIT 10
```

---

## 🗺️ Atlas — Things to Know

> Your knowledge base — reference materials, concepts, and evergreen notes.

- [[Atlas Dashboard]]

```button
name 📝 New Atlas Note
type command
action QuickAdd: New Atlas Note
color blue
```

---

## ⚡ Efforts — Things to Do

> Your active work — projects, areas of effort, and tasks.

- [[Projects Dashboard]]
- [[Areas of Effort]]

```button
name 🚀 New Project
type command
action QuickAdd: New Project
color purple
```
```button
name 🎯 New Area of Effort
type command
action QuickAdd: New Area of Effort
color purple
```

**🔥 Active Projects**

```dataview
TABLE rank AS "Rank"
FROM "Efforts/Projects/Active"
SORT rank DESC
```

**♨️ Simmering Projects**

```dataview
TABLE rank AS "Rank"
FROM "Efforts/Projects/Simmering"
SORT rank DESC
```

**📋 Outstanding Project Next Actions**

```dataview
TASK
FROM "Efforts/Projects"
WHERE !completed
```

---

## 📅 Calendar — Make It Whole

> Your timeline — daily notes, meetings, and time-based reflections.

- [[Calendar Dashboard]]
- **Today's Note:** Use `Cmd+D` / `Ctrl+D` to open today's daily note

```button
name 📅 New Daily Note
type command
action QuickAdd: New Daily Note
color green
```
```button
name 🤝 New Meeting Note
type command
action QuickAdd: New Meeting Note
color green
```

**Recent Daily Notes**

```dataview
TABLE file.cday AS "Created"
FROM "Calendar/Daily Notes"
SORT file.cday DESC
LIMIT 7
```

**☑️ Outstanding Daily Tasks**

```dataview
TASK
FROM "Calendar/Daily Notes"
WHERE !completed
SORT file.name DESC
```

---

## ➕ Plus — Capture What's New

> Your inbox — fresh ideas, quick captures, and unprocessed notes.

- [[Plus Inbox]]

```button
name ⚡ Quick Capture
type command
action QuickAdd: New Capture
color yellow
```

**Recently Added Notes**

```dataview
TABLE file.cday AS "Captured"
FROM "Plus"
SORT file.cday DESC
LIMIT 10
```

---

## 📦 Extras — The Overflow

> Miscellaneous items, attachments, and things that don't fit elsewhere.

- [[Extras]]

---

## 🧭 Quick Navigation

| Section | Purpose | Go To |
|---------|---------|-------|
| 🕐 Recents | Activity Stream | [[Recents]] |
| 🗺️ Atlas | Things to Know | [[Atlas Dashboard]] |
| ⚡ Efforts | Things to Do | [[Projects Dashboard]] |
| 📅 Calendar | Make It Whole | [[Calendar Dashboard]] |
| ➕ Plus | Capture What's New | [[Plus Inbox]] |
| 📦 Extras | The Overflow | [[Extras]] |

---

> [!tip] Daily Workflow
> 1. **Morning** — Open Home Base → Review active projects → Check calendar
> 2. **Throughout the day** — Capture ideas to Plus (Cmd+N / Ctrl+N)
> 3. **Evening** — Process Plus inbox → Update project ranks → Reflect in daily note
