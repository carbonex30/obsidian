---
tags:
  - guide
  - reference
---

# 🚀 Getting Started with Home Base

> A quick reference for using your Home Base + ACE system.

[[Home Base]] ← Start Here

---

## 🔑 Essential Keyboard Shortcuts

| Action                          | Mac                         | Windows/Linux                |     |
| ------------------------------- | --------------------------- | ---------------------------- | --- |
| Open today's daily note         | `Cmd+D`                     | `Ctrl+D`                     |     |
| Create new note (in current folder) | `Cmd+N`                 | `Ctrl+N`                     |     |
| Move file to another folder     | `Cmd+M`                     | `Ctrl+M`                     |     |
| Open quick switcher             | `Cmd+O`                     | `Ctrl+O`                     |     |
| Open command palette            | `Cmd+P`                     | `Ctrl+P`                     |     |
| Insert template                 | `Cmd+P` → "Insert template" | `Ctrl+P` → "Insert template" |     |

---

## 📁 Your Folder Structure (ACE Framework)

```
Vault Root/
├── 🏠 Home Base.md          ← START HERE
├── 🕐 Recents.md             ← Vault-wide activity stream
├── 🗺️ Atlas/                ← Things to Know
│   ├── Atlas Dashboard.md
│   ├── Reading Dashboard.md  ← Books & articles tracker
│   ├── Video Dashboard.md    ← YouTube video tracker
│   ├── ACE Framework.md
│   ├── Home Base System.md
│   ├── Getting Started with Home Base.md
│   ├── Reading/              ← Individual book & article notes
│   └── Videos/               ← Video notes (manual + auto-summarized)
│       └── YT Summaries/     ← Auto-summarized video uploads land here
├── 📅 Calendar/              ← Make It Whole
│   ├── Calendar Dashboard.md
│   ├── Daily Notes/
│   └── Meetings/
├── ⚡ Efforts/               ← Things to Do
│   ├── Projects Dashboard.md
│   ├── Areas of Effort.md
│   ├── Areas/
│   └── Projects/
│       ├── Active/
│       ├── Simmering/
│       └── Sleeping/
├── ➕ Plus/                   ← Capture What's New (Inbox)
│   ├── Plus Inbox.md
│   └── 📦 Extras/            ← The Overflow (nested in Plus)
│       └── Extras.md
└── 📋 Templates/             ← Note Templates
    ├── Daily Note Template.md
    ├── Project Template.md
    ├── Quote Template.md
    ├── Area of Effort Template.md
    ├── Meeting Note Template.md
    ├── Reading Note Template.md  ← Books & articles
    └── Video Note Template.md    ← YouTube videos
```

---

## 🏠 Home Base — What's On It

Home Base is your command center. It shows live Dataview queries so you always have a current snapshot:

| Section | What It Shows |
|---------|---------------|
| 🕐 **Recently Modified** | Last 10 modified notes across the entire vault (links to [[Recents]] for full list) |
| 📖 **Currently Reading** | Books/articles with `status: reading` from `Atlas/Reading/` |
| 🎬 **Recent Videos** | Last 5 video notes added to `Atlas/Videos/` |
| ⚡ **Active Projects** | All active projects sorted by rank |
| ♨️ **Simmering Projects** | All simmering projects sorted by rank |
| 📋 **Outstanding Project Next Actions** | Unchecked tasks from all project notes |
| ☑️ **Outstanding Daily Tasks** | Unchecked tasks from daily notes |
| 📅 **Recent Daily Notes** | Last 7 daily notes |
| ➕ **Recently Added Notes** | Last 10 notes captured to Plus |
| 🧭 **Quick Navigation** | One-click links to every dashboard |

---

## 🕐 Recents — Vault Activity Stream

[[Recents]] is a standalone note that shows the **50 most recently modified files** across your entire vault, grouped with their parent folder. Use it to quickly find what you were just working on.

> [!tip] Pin Recents to your sidebar
> Right-click the Recents tab → **Open in new pane** → drag to right sidebar → right-click tab → **Pin**

---

## 🔄 Daily Workflow

### Morning (5 min)
1. Open [[Home Base]]
2. Scan **Active Projects** — are priorities still right?
3. Check **Recently Added** in Plus — anything from yesterday to process?
4. Open today's daily note (`Cmd+D`) and set intentions

### Throughout the Day
- **Got an idea?** → Use the **⚡ Quick Capture** button on Home Base, or navigate to Plus first then `Cmd+N`
- **Working on a project?** → Navigate from Home Base → Efforts → Projects
- **In a meeting?** → Create note in `Calendar/Meetings/` using Meeting template
- **Watched a video?** → Use the **🎬 New Video Note** button or update the auto-summarized note in `Atlas/Videos/`
- **Reading a book/article?** → Use the **📖 New Reading Note** button and log your session in the Reading Log

### Evening (10 min)
1. Process **Plus inbox** — move items to Atlas, Efforts, or Calendar
2. Update project ranks if priorities shifted
3. Fill in evening reflection in today's daily note

### Weekly (15 min)
- Review Simmering projects — promote or archive?
- Clean up Plus inbox completely
- Check Areas of Effort — still relevant?
- Celebrate completed projects!

---

## 🎯 Project Management

### Creating a New Project
1. Create a note in `Efforts/Projects/Active/` (or Simmering/Sleeping)
2. Use the **Project Template** for structure
3. Set the `rank` in frontmatter (higher = more important)
4. Set the `area` to link to an Area of Effort

### Changing Project Priority
- Edit the `rank` number in frontmatter
- The [[Projects Dashboard]] auto-sorts by rank

### Changing Project Status
- Move the file between `Active/`, `Simmering/`, `Sleeping/` folders
- Right-click → "Move file to..." → type destination

### Projects Dashboard Sections
The [[Projects Dashboard]] shows four views:
- **🔥 Active** — with Rank, Area of Effort, and Created date
- **♨️ Simmering** — same columns
- **💤 Sleeping** — same columns
- **📊 All Projects Overview** — every project across all statuses in one table

---

## 📖 Reading Tracker

### Overview
Each book or article gets its own note in `Atlas/Reading/`. The [[Reading Dashboard]] shows everything at a glance — what you're currently reading, your backlog, finished items, and stats.

### Adding a New Book or Article
1. Click **📖 New Reading Note** on Home Base or the Reading Dashboard
2. Fill in the frontmatter: `type` (book/article/paper), `author`, `total-pages`, `source`
3. Change `status` from `to-read` to `reading` when you start

### Reading Note Frontmatter
| Property | Values | Purpose |
|----------|--------|---------|
| `type` | `book`, `article`, `paper` | Categorizes the item |
| `author` | text | Author name |
| `status` | `to-read`, `reading`, `finished`, `abandoned` | Drives all dashboard views |
| `rating` | 1–5 | Optional rating when finished |
| `start-date` / `finish-date` | `YYYY-MM-DD` | Reading timeline |
| `current-page` / `total-pages` | number | Progress tracking |
| `source` | text or URL | Where you found it |

### Reading Note Sections
- **Description** — what it's about and why you're reading it
- **Reading Log** — add a dated bullet each session: `- **2026-03-08** — Read pp. 45–72. Key idea here…`
- **Key Takeaways** — main learnings
- **Highlights & Quotes** — specific passages worth keeping
- **Connections** — links to related vault notes

### Reading Dashboard Sections
The [[Reading Dashboard]] shows:
- **📖 Currently Reading** — `status: reading`, with author, type, and page progress
- **📋 To Read** — `status: to-read` backlog
- **✅ Recently Finished** — `status: finished`, with rating and finish date
- **🚫 Abandoned** — `status: abandoned`
- **📊 Reading Stats** — counts by status and by type

---

## 🎬 Video Tracker

### Overview
YouTube videos live in `Atlas/Videos/`. There are two kinds of notes here:
- **Auto-summarized** — generated by your external summarizer tool, tagged `#autosummarizer`
- **Manual** — created with the Video Note template for videos you find yourself

The [[Video Dashboard]] tracks both in one place.

### Adding a Video Manually
1. Click **🎬 New Video Note** on Home Base or the Video Dashboard
2. Fill in `channel`, `video_url`, `published`, `video_type`
3. After watching, change `status` to `watched` and fill in your reflections

### Auto-Summarized Videos
Auto-summarized videos from your external workflow live in `Atlas/Videos/YT Summaries/`. Upload them directly to that folder. For them to integrate with the dashboard, each file's frontmatter must include:
1. `status: watched` (or `unwatched`)
2. `- autosummarizer` under `tags:`
3. `- video` under `tags:`

All Dataview queries use `FROM "Atlas/Videos"` which **includes subfolders**, so files in `YT Summaries/` appear in every dashboard table automatically. The auto-summarized notes also appear in their own dedicated **🤖 Auto-Summarized** table on the Video Dashboard.

### Video Note Frontmatter
| Property | Values | Purpose |
|----------|--------|---------|
| `title` | text | Video title |
| `channel` | text | Channel name (use underscores for spaces) |
| `video_url` | URL | Link to the video |
| `published` | `YYYY-MM-DD` | Video publish date |
| `video_type` | `informational`, `instructional`, etc. | Content type |
| `status` | `unwatched`, `watched` | Drives dashboard views |
| `rating` | 1–5 | Optional quality rating |

### Video Note Sections
- **Why Watch This** *(manual notes)* — what drew you to it
- **Key Takeaways** — main things learned
- **Highlights & Quotes** — specific moments or quotes
- **My Reflections** — your own thoughts and reactions
- **Connections** — links to related vault notes, projects, or other videos

### Video Dashboard Sections
The [[Video Dashboard]] shows:
- **📺 Recently Added** — last 10 videos by creation date
- **👀 Unwatched / To Watch** — `status: unwatched`
- **✅ Watched** — `status: watched`, with rating
- **🤖 Auto-Summarized** — all notes tagged `#autosummarizer`
- **📊 Video Stats** — counts by channel and by type

---

## 📝 Templates Reference

### Daily Note Template
Requires **Templater** plugin. Auto-generates:
- Prev/Next day navigation links (top and bottom)
- `## 🌅 Morning Intentions` — focus prompt
- `## 📝 Notes & Thoughts` — freeform capture
- `## ✅ Tasks` — checkbox task list
- `## 🌙 Evening Reflection` — end-of-day review
- `## 🕰️ On This Day` — Dataview query showing notes created on this date in previous years

### Project Template
Frontmatter: `rank`, `area`, `status`, `tags: [project]`
Sections: Description, Next Actions (tasks), Key Resources & Links, Progress Log, Notes

### Meeting Note Template
Frontmatter: `date`, `attendees`, `tags: [meeting]`
Sections: Agenda, Notes, Action Items (tasks), Follow-ups

### Quote Template
Frontmatter: `by`, `source`, `tags: [quote]`
Sections: Formatted quote callout, Source, Why This Matters, Related Ideas
> Notes tagged `#quote` automatically appear in the **Quotes Collection** on [[Atlas Dashboard]].

### Area of Effort Template
Frontmatter: `tags: [area]`
Includes a live Dataview query showing all projects linked to this area.

### Reading Note Template
Frontmatter: `type`, `author`, `status`, `rating`, `start-date`, `finish-date`, `current-page`, `total-pages`, `source`, `tags: [reading]`
Sections: Description, Reading Log, Key Takeaways, Highlights & Quotes, Connections
> See **Reading Tracker** section above for full workflow details.

### Video Note Template
Frontmatter: `title`, `channel`, `video_url`, `published`, `video_type`, `status`, `rating`, `tags: [video]`
Sections: Why Watch This, Key Takeaways, Highlights & Quotes, My Reflections, Connections
> See **Video Tracker** section above for full workflow details.

---

## 🗺️ Atlas Dashboard Features

The [[Atlas Dashboard]] shows:
- **📚 All Atlas Notes** — every note in Atlas sorted by last modified
- **📖 Reading** — active/to-read items from `Atlas/Reading/`, links to [[Reading Dashboard]]
- **🎬 Videos** — recent video notes from `Atlas/Videos/`, links to [[Video Dashboard]]
- **💬 Quotes Collection** — all notes tagged `#quote`, showing author and source
- **🏷️ Browse by Tag** — guidance on using Obsidian's tag pane

---

## 📅 Calendar Dashboard Features

The [[Calendar Dashboard]] shows:
- **📝 Recent Daily Notes** — last 14 daily notes
- **🤝 Recent Meetings** — last 10 meeting notes (with date and attendees)
- **📆 Daily Notes by Month** — all daily notes grouped by month with count
- **🕰️ On This Day — Across All Years** — notes created on today's date in any past year

---

## 💡 Tips & Best Practices

1. **Always start from Home Base** — it's your compass
2. **Capture first, organize later** — use Plus liberally
3. **Rank honestly** — if everything is rank 9, nothing is
4. **Link generously** — connections are where insights emerge
5. **Review regularly** — the system works best when maintained
6. **Don't over-organize** — good enough structure beats perfect structure
7. **Use Recents to resume** — it's the fastest way to pick up where you left off
8. **Tag quotes consistently** — `#quote` feeds the Atlas Quotes Collection automatically
9. **Log reading sessions** — even one line in the Reading Log keeps piecemeal reading on track
10. **Enrich video notes after watching** — fill in My Reflections and Connections while it's fresh

---

## ⚙️ Plugin Setup Guide

This vault uses **4 community plugins** and **2 core plugins**. Below is every setting needed to make each one work correctly.

---

### Community Plugins

To install any community plugin: **Settings → Community plugins → Browse** → search by name → Install → Enable.

---

#### 1. Dataview

| | |
|--|--|
| **Plugin ID** | `dataview` |
| **Purpose** | Powers every dynamic table, list, and task query in all dashboards |

**Setup:** No configuration needed. Install and enable — all `dataview` code blocks will render automatically.

> [!warning] If dashboards show raw code instead of tables
> Make sure Dataview is **enabled** under Settings → Community plugins.

---

#### 2. Templater

| | |
|--|--|
| **Plugin ID** | `templater-obsidian` |
| **Purpose** | Powers the Daily Note Template — generates prev/next day links, date headings, and the "On This Day" section |

**Setup:** Go to **Settings → Templater** and configure the following:

| Setting | Value |
|---------|-------|
| Template folder location | `Templates` |
| Trigger Templater on new file creation | **ON** ✅ |
| Enable Folder Templates | **ON** ✅ |

**Folder Templates** — click **Add** and enter:

| Folder | Template |
|--------|----------|
| `Calendar/Daily Notes` | `Templates/Daily Note Template.md` |

> [!info] Why this matters
> With "Trigger on file creation" and the folder template set, any new note created inside `Calendar/Daily Notes` (including via `Cmd+D`) will **automatically** run the Daily Note Template and populate the date, navigation links, and sections. Without this, the template renders as raw `<% %>` syntax.

---

#### 3. QuickAdd

| | |
|--|--|
| **Plugin ID** | `quickadd` |
| **Purpose** | Powers the action buttons on Home Base (📝 New Atlas Note, 🚀 New Project, 📖 New Reading Note, 🎬 New Video Note, etc.) |

**Setup:** Go to **Settings → QuickAdd**. Each choice below must be created and have **"Add to command palette"** turned ON — this is what allows the Buttons plugin to trigger them.

---

##### Choice 1 — New Daily Note

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Daily Note Template.md` |
| File name format | `{{DATE:YYYY-MM-DD}}` |
| Folder | `Calendar/Daily Notes` |
| Open file | ON, in new tab |
| Add to command palette | **ON** ✅ |

---

##### Choice 2 — New Project

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Project Template.md` |
| File name format | `Reading Note ({{DATE:YYYY-MM-DD}})` |
| Folder | `Efforts/Projects/Active` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 3 — New Meeting Note

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Meeting Note Template.md` |
| File name format | `Meeting Note ({{DATE:YYYY-MM-DD}})` |
| Folder | `Calendar/Meetings` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 4 — New Atlas Note

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Atlas Note Template.md` |
| File name format | `Atlas Note ({{DATE:YYYY-MM-DD}})` |
| Folder | `Atlas` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 5 — New Area of Effort

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Area of Effort Template.md` |
| File name format | *(leave blank — type the area name when prompted)* |
| Folder | `Efforts/Areas` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 6 — New Capture

| Setting | Value |
|---------|-------|
| Type | Capture |
| Capture to | `Plus/Plus Inbox.md` |
| Prepend to file | ON (adds to top of Plus Inbox) |
| Add to command palette | **ON** ✅ |

---

##### Choice 7 — New Reading Note

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Reading Note Template.md` |
| File name format | `Reading Note ({{DATE:YYYY-MM-DD}})` |
| Folder | `Atlas/Reading` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 8 — New Video Note

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Video Note Template.md` |
| File name format | `Video Note ({{DATE:YYYY-MM-DD}})` |
| Folder | `Atlas/Videos` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

> [!warning] Buttons on Home Base won't work until these are set up
> The `action QuickAdd: <name>` field in each button block must **exactly match** the choice name in QuickAdd — including capitalization and spacing.

---

#### 4. Buttons

| | |
|--|--|
| **Plugin ID** | `buttons` |
| **Purpose** | Renders the clickable action buttons on Home Base |

**Setup:** No configuration needed. Install and enable. Buttons are defined inline using code blocks in notes:

~~~
```button
name 🚀 New Project
type command
action QuickAdd: New Project
color purple
```
~~~

Available colors: `blue`, `purple`, `green`, `yellow`, `red`, `default`

---

### Core Plugins

Core plugins ship with Obsidian. Enable them under **Settings → Core plugins**.

---

#### Daily Notes (Core)

**Purpose:** `Cmd+D` / `Ctrl+D` opens or creates today's daily note.

Go to **Settings → Daily notes**:

| Setting | Value |
|---------|-------|
| Date format | `YYYY-MM-DD` |
| New file location | `Calendar/Daily Notes` |
| Template file location | `Templates/Daily Note Template` |
| Open daily note on startup | OFF (recommended) |

> [!info] Templater takes over from here
> The Daily Notes plugin creates the file; Templater's folder template then immediately processes it and fills in all the dynamic content.

---

#### Templates (Core)

**Purpose:** Allows manually inserting any template into an open note via the command palette.

Go to **Settings → Templates**:

| Setting | Value |
|---------|-------|
| Template folder location | `Templates` |

---

### Obsidian App Settings

A few vault-level settings are already configured and should remain as-is:

| Setting | Location | Value | Why |
|---------|----------|-------|-----|
| Default location for new notes | Settings → Files & Links | Current folder | New notes go wherever you are; navigate to Plus first to capture there |
| Default attachment folder | Settings → Files & Links | `Plus/Extras` | Images/files drop into Plus/Extras automatically |
| Always update internal links | Settings → Files & Links | **ON** ✅ | Links stay valid when you rename or move files |
| Default view mode | Settings → Editor | Preview | Notes open in reading mode by default |
| Show line numbers | Settings → Editor | ON | Visible line numbers in edit mode |

---

### CSS Snippets

The vault includes three custom CSS snippets (already installed in `.obsidian/snippets/`). Enable them under **Settings → Appearance → CSS snippets**:

| File | Effect |
|------|--------|
| `compact-dataview.css` | Tightens spacing in Dataview tables |
| `dashboard.css` | Styles the Home Base and dashboard layouts |
| `dataview-table-columns.css` | Improves Dataview table column widths |

---

## 📚 Source

This system is based on Nick Milo's **Linking Your Thinking** methodology and the **Ideaverse** system.
- Video: [The Biggest Obsidian Upgrade I've Made in Years](https://youtube.com/watch?v=KekL4cLtpuc)
- Learn more: [Linking Your Thinking](https://www.linkingyourthinking.com/)

---

[[Atlas Dashboard]] ← Back to Atlas | [[Home Base]] ← Back to Home
