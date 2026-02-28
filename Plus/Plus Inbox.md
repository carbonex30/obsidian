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
SORT file.cday DESC
```

---

## 📊 Inbox Stats

```dataview
LIST length(rows) + " notes awaiting processing"
FROM "Plus"
WHERE file.name != "Plus Inbox"
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
>    - Not useful → Delete or move to `Extras/`
> 4. **Apply templates** as needed for structure
>
> 🎯 Goal: Keep Plus empty or near-empty. It's an inbox, not a storage bin.

---

> [!info] Quick Capture
> - **Desktop:** `Cmd+N` / `Ctrl+N` → type idea → done (auto-lands in Plus)
> - **Mobile:** Tap 🔍 → type idea → enter → done
> - Don't worry about organizing during capture — just get it down!
