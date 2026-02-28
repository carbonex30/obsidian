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
