---
aliases:
  - Projects
  - Project Hub
---

# ⚡ Projects Dashboard

> Manage all your projects by priority. Higher rank = higher priority.
> Move projects between **Active**, **Simmering**, and **Sleeping** as priorities shift.

[[Home Base]] ← Back to Home

---

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

---

## 🎯 Areas of Effort

> High-level categories that group your projects. Click any area to explore it in depth.

```dataviewjs
const areas = dv.pages('"Efforts/Areas"')
  .sort(a => a.rank ?? -9999, 'desc');

const rows = areas.map(a => {
  const count = dv.pages('"Efforts/Projects"')
    .where(p => p.area && p.area.path === a.file.link.path)
    .length;
  return [a.file.link, a.rank ?? "", count];
});

dv.table(["Area", "Rank", "Projects"], rows);
```

---

## 🔥 Active Projects

> Currently receiving focused attention and resources.

```dataview
TABLE
  rank AS "Rank",
  area AS "Area of Effort",
  file.cday AS "Created"
FROM "Efforts/Projects/Active"
SORT rank DESC
```

---

## ♨️ Simmering Projects

> Ideas with potential that require occasional attention.

```dataview
TABLE
  rank AS "Rank",
  area AS "Area of Effort",
  file.cday AS "Created"
FROM "Efforts/Projects/Simmering"
SORT rank DESC
```

---

## 💤 Sleeping Projects

> Concepts stored for future consideration with minimal current energy.

```dataview
TABLE
  rank AS "Rank",
  area AS "Area of Effort",
  file.cday AS "Created"
FROM "Efforts/Projects/Sleeping"
SORT rank DESC
```

---

## 📊 All Projects Overview

```dataview
TABLE
  rank AS "Rank",
  area AS "Area of Effort",
  file.folder AS "Status",
  file.cday AS "Created"
FROM "Efforts/Projects"
WHERE file.name != "Projects Dashboard"
SORT rank DESC
```

---

> [!info] How to Use This Dashboard
> - **Create a project:** Use the Project template in `Templates/` or create a note in the appropriate status folder
> - **Set priority:** Add `rank: 5.0` (or any number) to the frontmatter — higher = more important
> - **Change status:** Move the file between `Active/`, `Simmering/`, `Sleeping/` folders (right-click → Move file to...)
> - **Link to areas:** Add `area: "[[Your Area]]"` in frontmatter to group related projects
