---
aliases:
  - Recents
  - Recently Modified
  - Activity Stream
---

# 🕐 Recents

```dataview
TABLE WITHOUT ID
  file.link AS "file name",
  dateformat(file.mtime, "yyyy-MM-dd") AS "modified",
  regexreplace(file.folder, "^.*/", "") AS "Parent Folder"
FROM ""
WHERE file.name != this.file.name
  AND !contains(file.folder, "Templates")
SORT file.mtime DESC
LIMIT 50
```

---

> [!tip] Pin to sidebar
> Right-click tab → **Open in new pane** → drag to right sidebar → right-click tab → **Pin**
