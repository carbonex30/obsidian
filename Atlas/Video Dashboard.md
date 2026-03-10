---
aliases:
  - Videos
  - Video Tracker
  - Video Library
---

# 🎬 Video Dashboard

> Track YouTube videos you've watched or want to watch — capture knowledge, insights, and connections.
> Auto-summarized videos live in `Atlas/Videos/YT Summaries/`. Manually added notes live in `Atlas/Videos/`.

[[Home Base]] ← Back to Home | [[Atlas Dashboard]] ← Back to Atlas

---

```button
name 🎬 New Video Note
type command
action QuickAdd: New Video Note
color blue
```

---

## 📺 Recently Added

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  channel AS "Channel",
  video_type AS "Type",
  published AS "Published"
FROM "Atlas/Videos"
SORT file.cday DESC
LIMIT 10
```

---

## 👀 Unwatched / To Watch

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  channel AS "Channel",
  video_type AS "Type"
FROM "Atlas/Videos"
WHERE status = "unwatched"
SORT file.cday DESC
```

---

## ✅ Watched

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  channel AS "Channel",
  video_type AS "Type",
  rating AS "Rating",
  published AS "Published"
FROM "Atlas/Videos"
WHERE status = "watched"
SORT file.mday DESC
```

---

## 🤖 Auto-Summarized (Needs Review)

```dataview
TABLE WITHOUT ID
  file.link AS "Title",
  channel AS "Channel",
  video_type AS "Type",
  published AS "Published"
FROM "Atlas/Videos"
WHERE contains(tags, "autosummarizer")
SORT file.cday DESC
```

---

## 📊 Video Stats

**By Channel**

```dataview
TABLE WITHOUT ID
  channel AS "Channel",
  length(rows) AS "Videos"
FROM "Atlas/Videos"
GROUP BY channel
SORT length(rows) DESC
```

**By Type**

```dataview
TABLE WITHOUT ID
  video_type AS "Type",
  length(rows) AS "Videos"
FROM "Atlas/Videos"
GROUP BY video_type
SORT length(rows) DESC
```

---

> [!tip] How to Use the Video Tracker
> 1. **Auto-summarized videos** — upload to `Atlas/Videos/YT Summaries/`. They appear here automatically as long as frontmatter includes `tags: [autosummarizer, video]` and `status:`
> 2. **Manual entries** — Click the button above or use `QuickAdd: New Video Note` for videos you find yourself
> 3. **Review and enrich** — After watching, update `status` to `watched`, add a `rating`, and fill in your personal reflections and connections
> 4. **Build knowledge** — Use the Connections section to link videos to related Atlas notes, projects, or other videos
