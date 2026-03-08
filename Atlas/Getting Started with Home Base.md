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
│   ├── ACE Framework.md
│   ├── Home Base System.md
│   ├── Getting Started with Home Base.md
│   └── YT Summaries/         ← Processed YouTube video notes
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
│   └── Plus Inbox.md
├── 📦 Extras/                ← The Overflow
│   └── Extras.md
└── 📋 Templates/             ← Note Templates
    ├── Daily Note Template.md
    ├── Project Template.md
    ├── Quote Template.md
    ├── Area of Effort Template.md
    └── Meeting Note Template.md
```

---

## 🏠 Home Base — What's On It

Home Base is your command center. It shows live Dataview queries so you always have a current snapshot:

| Section | What It Shows |
|---------|---------------|
| 🕐 **Recently Modified** | Last 10 modified notes across the entire vault (links to [[Recents]] for full list) |
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

---

## 🗺️ Atlas Dashboard Features

The [[Atlas Dashboard]] shows:
- **📚 All Atlas Notes** — every note in Atlas sorted by last modified
- **💬 Quotes Collection** — all notes tagged `#quote`, showing author and source
- **🏷️ Browse by Tag** — guidance on using Obsidian's tag pane

### YT Summaries
Notes processed from YouTube videos live in `Atlas/YT Summaries/`. Each file is named with the video title, YouTube ID, date, and a review status (`NEEDS_REVIEW`, `VALIDATED`, etc.).

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
| **Purpose** | Powers the action buttons on Home Base (📝 New Atlas Note, 🚀 New Project, etc.) |

**Setup:** Go to **Settings → QuickAdd**. Each choice below must be created and have **"Add to command palette"** turned ON — this is what allows the Buttons plugin to trigger them.

---

##### Choice 1 — New Daily Note *(already configured)*

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Daily Note Template.md` |
| File name format | `{{DATE:YYYY-MM-DD}}` |
| Folder | `Calendar/Daily Notes` |
| Open file | ON, in new tab |
| Add to command palette | **ON** ✅ |

---

##### Choice 2 — New Project *(needs to be created)*

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Project Template.md` |
| File name format | *(leave blank — you'll be prompted to type the name)* |
| Folder | `Efforts/Projects/Active` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 3 — New Meeting Note *(needs to be created)*

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Meeting Note Template.md` |
| File name format | *(leave blank — type the meeting name when prompted)* |
| Folder | `Calendar/Meetings` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 4 — New Atlas Note *(needs to be created)*

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | *(leave blank, or create an Atlas note template)* |
| File name format | *(leave blank — type the note name when prompted)* |
| Folder | `Atlas` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 5 — New Area of Effort *(needs to be created)*

| Setting | Value |
|---------|-------|
| Type | Template |
| Template path | `Templates/Area of Effort Template.md` |
| File name format | *(leave blank — type the area name when prompted)* |
| Folder | `Efforts/Areas` |
| Open file | ON |
| Add to command palette | **ON** ✅ |

---

##### Choice 6 — New Capture *(needs to be created)*

| Setting | Value |
|---------|-------|
| Type | Capture |
| Capture to | `Plus/Plus Inbox.md` |
| Prepend to file | ON (adds to top of Plus Inbox) |
| Add to command palette | **ON** ✅ |

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
| Default attachment folder | Settings → Files & Links | `Extras` | Images/files drop into Extras automatically |
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
