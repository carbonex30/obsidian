---
aliases:
  - Atlas
  - Knowledge Base
---

# 🗺️ Atlas Dashboard

> Your knowledge base — reference materials, concepts, maps of content, and evergreen notes.
> This is where **things to know** live.

[[Home Base]] ← Back to Home

---

## 📚 All Atlas Notes

```dataview
TABLE WITHOUT ID dateformat(file.cday, "MM/dd/yyyy") AS "Created", dateformat(file.mday, "MM/dd/yyyy") AS "Modified", file.link AS "Note"
FROM "Atlas"
WHERE file.name != "Atlas Dashboard"
SORT file.mday DESC
```

---

## 💬 Quotes Collection

```dataview
TABLE by AS "By", source AS "Source"
FROM #quote
SORT file.cday DESC
```

---

## 🏷️ Browse by Tag

> Use Obsidian's tag pane or search `tag:#yourtag` to explore by topic.

---

## How to Use Atlas

> [!info] Atlas is for permanent, reference-quality notes
> - **Concepts** — Evergreen notes about ideas you want to develop
> - **MOCs (Maps of Content)** — Index notes that curate and link related concepts
> - **Quotes** — Memorable quotes with personal reflection
> - **Reference Materials** — Anything you want to be able to find again
>
> 💡 When a note in **Plus** has been processed and refined, move it here.
