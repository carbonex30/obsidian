---
aliases:
  - Home
  - Dashboard
  - HQ
---

# 🏠 Home Base

> *Your central command center. Everything starts here.*

---

## 🗺️ Atlas — Things to Know

> Your knowledge base — reference materials, concepts, and evergreen notes.

- [[Atlas Dashboard]]

---

## ⚡ Efforts — Things to Do

> Your active work — projects, areas of effort, and tasks.

- [[Projects Dashboard]]
- [[Areas of Effort]]

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

---

## 📅 Calendar — Make It Whole

> Your timeline — daily notes, meetings, and time-based reflections.

- [[Calendar Dashboard]]
- **Today's Note:** Use `Cmd+D` / `Ctrl+D` to open today's daily note

**Recent Daily Notes**

```dataview
TABLE file.cday AS "Created"
FROM "Calendar/Daily Notes"
SORT file.cday DESC
LIMIT 7
```

---

## ➕ Plus — Capture What's New

> Your inbox — fresh ideas, quick captures, and unprocessed notes.

- [[Plus Inbox]]

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
