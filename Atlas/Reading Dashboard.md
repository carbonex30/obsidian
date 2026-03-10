---
aliases:
  - Reading
  - Book Tracker
  - Reading List
---

# 📚 Reading Dashboard

> Track what you're reading, what you've learned, and what's next on your list.
> Each book or article gets its own note in `Atlas/Reading/`.

[[Home Base]] ← Back to Home | [[Atlas Dashboard]] ← Back to Atlas

---

```button
name 📖 New Reading Note
type command
action QuickAdd: New Reading Note
color blue
```

---

## 📖 Currently Reading

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  author AS "Author",
  type AS "Type",
  current-page + " / " + total-pages AS "Progress",
  start-date AS "Started"
FROM "Atlas/Reading"
WHERE status = "reading"
SORT start-date DESC
```

---

## 📋 To Read

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  author AS "Author",
  type AS "Type",
  source AS "Source"
FROM "Atlas/Reading"
WHERE status = "to-read"
SORT file.cday DESC
```

---

## ✅ Recently Finished

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  author AS "Author",
  type AS "Type",
  rating AS "Rating",
  finish-date AS "Finished"
FROM "Atlas/Reading"
WHERE status = "finished"
SORT finish-date DESC
```

---

## 🚫 Abandoned

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  author AS "Author",
  type AS "Type",
  start-date AS "Started"
FROM "Atlas/Reading"
WHERE status = "abandoned"
SORT start-date DESC
```

---

## 📊 Reading Stats

**By Status**

```dataview
TABLE WITHOUT ID
  status AS "Status",
  length(rows) AS "Count"
FROM "Atlas/Reading"
GROUP BY status
SORT status ASC
```

**By Type**

```dataview
TABLE WITHOUT ID
  type AS "Type",
  length(rows) AS "Count"
FROM "Atlas/Reading"
GROUP BY type
SORT type ASC
```

---

> [!tip] How to Use the Reading Tracker
> 1. **Add a book or article** — Click the button above or use `QuickAdd: New Reading Note`
> 2. **Update status** — Change the `status` property in frontmatter: `to-read` → `reading` → `finished`
> 3. **Log your sessions** — Add dated entries to the Reading Log section as you read piecemeal
> 4. **Capture learnings** — Use Key Takeaways and Highlights sections for things worth remembering
> 5. **Update progress** — Change `current-page` in frontmatter to track where you are
