---
aliases:
  - Inbox
  - Plus
  - Captures
---

# ➕ Plus — Inbox

> Your inbox for fresh ideas, quick captures, and unprocessed notes.
> Everything new lands here first. Process regularly and move to the right place.

[[Home Base]] ← Back to Home

---

## 📥 All Captures (Newest First)

```dataview
TABLE file.cday AS "Captured", file.tags AS "Tags"
FROM "Plus"
WHERE file.name != "Plus Inbox"
  AND !contains(file.folder, "Plus/Extras")
SORT file.cday DESC
```

---

## 📊 Inbox Stats

```dataview
LIST length(rows) + " notes awaiting processing"
FROM "Plus"
WHERE file.name != "Plus Inbox"
  AND !contains(file.folder, "Plus/Extras")
GROUP BY "Total"
```

---

## Processing Workflow

> [!tip] How to process your inbox
> 1. **Review** each captured note
> 2. **Enrich** — Add context, personal reflection, and links
> 3. **Move** to the right home:
>    - Knowledge/concepts → `Atlas/`
>    - Projects → `Efforts/Projects/Active|Simmering|Sleeping/`
>    - Time-based notes → `Calendar/`
>    - Not useful → Delete or move to `Plus/Extras/`
> 4. **Apply templates** as needed for structure
>
> 🎯 Goal: Keep Plus empty or near-empty. It's an inbox, not a storage bin.

---

> [!info] Quick Capture
> - **Desktop:** `Cmd+N` / `Ctrl+N` → type idea → done *(automatically saved to `Plus/` — configured in Obsidian Settings → Files & Links → Default location for new notes)*
> - **Mobile:** Tap 🔍 → type idea → enter → done
> - Don't worry about organizing during capture — just get it down!
> - **Note:** QuickAdd commands (New Project, New Meeting, etc.) route to their own folders and are unaffected by this setting.