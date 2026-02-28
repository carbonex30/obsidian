---
aliases:
  - Areas
  - Effort Areas
---

# 🎯 Areas of Effort

> Higher-level categories that group related projects and ongoing responsibilities.
> Each area can contain multiple projects across Active, Simmering, and Sleeping states.

[[Home Base]] ← Back to Home | [[Projects Dashboard]] ← All Projects

---

## All Areas

```dataview
LIST
FROM "Efforts/Areas"
SORT file.name ASC
```

---

## Projects by Area

```dataview
TABLE
  rank AS "Rank",
  file.folder AS "Status"
FROM "Efforts/Projects"
WHERE area != null
GROUP BY area
SORT area ASC
```

---

> [!tip] Creating Areas of Effort
> Create a new note in `Efforts/Areas/` for each broad category of work or life focus.
> Examples: Health, Career, Creative Work, Learning, Relationships, Finance
