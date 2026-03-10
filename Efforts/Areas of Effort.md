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

```dataviewjs
const areas = dv.pages('"Efforts/Areas"')
  .sort(a => a.rank ?? -9999, 'desc');

const rows = areas.map(a => {
  const count = dv.pages('"Efforts/Projects"')
    .where(p => p.area && p.area.path === a.file.link.path)
    .length;
  return [a.file.link, a.rank ?? "", count];
});

dv.table(["File", "Rank", "Projects"], rows);
```

---

> [!tip] Creating Areas of Effort
> Create a new note in `Efforts/Areas/` for each broad category of work or life focus.
> Examples: Health, Career, Creative Work, Learning, Relationships, Finance
