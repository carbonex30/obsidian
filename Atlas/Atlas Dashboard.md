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

```button
name 📝 New Atlas Note
type command
action QuickAdd: New Atlas Note
color blue
```
```button
name 📖 New Reading Note
type command
action QuickAdd: New Reading Note
color blue
```
```button
name 🎬 New Video Note
type command
action QuickAdd: New Video Note
color blue
```

---

## 📚 All Atlas Notes

```dataview
TABLE WITHOUT ID dateformat(file.cday, "MM/dd/yyyy") AS "Created", dateformat(file.mday, "MM/dd/yyyy") AS "Modified", file.link AS "Note"
FROM "Atlas"
WHERE file.name != "Atlas Dashboard"
SORT file.mday DESC
```

---

## 📖 Reading

> Track books, articles, and papers you're reading or want to read.

- [[Reading Dashboard]]

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  author AS "Author",
  status AS "Status"
FROM "Atlas/Reading"
WHERE status = "reading" OR status = "to-read"
SORT status ASC, file.cday DESC
LIMIT 5
```

---

## 🎬 Videos

> YouTube videos tracked for knowledge, insights, and connections.

- [[Video Dashboard]]

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  channel AS "Channel",
  video_type AS "Type"
FROM "Atlas/Videos"
SORT file.cday DESC
LIMIT 5
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
