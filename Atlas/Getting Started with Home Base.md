---
tags:
  - guide
  - reference
---

# 🚀 Getting Started with Home Base

> A quick reference for using your new Home Base + ACE system.

[[Home Base]] ← Start Here

---

## 🔑 Essential Keyboard Shortcuts

| Action                          | Mac                         | Windows/Linux                |     |
| ------------------------------- | --------------------------- | ---------------------------- | --- |
| Open today's daily note         | `Cmd+D`                     | `Ctrl+D`                     |     |
| Create new note (lands in Plus) | `Cmd+N`                     | `Ctrl+N`                     |     |
| Move file to another folder     | `Cmd+M`                     | `Ctrl+M`                     |     |
| Open quick switcher             | `Cmd+O`                     | `Ctrl+O`                     |     |
| Open command palette            | `Cmd+P`                     | `Ctrl+P`                     |     |
| Insert template                 | `Cmd+P` → "Insert template" | `Ctrl+P` → "Insert template" |     |

---

## 📁 Your Folder Structure (ACE Framework)

```
Vault Root/
├── 🏠 Home Base.md          ← START HERE
├── 🗺️ Atlas/                ← Things to Know
│   └── Atlas Dashboard.md
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

## 🔄 Daily Workflow

### Morning (5 min)
1. Open [[Home Base]]
2. Scan **Active Projects** — are priorities still right?
3. Check **Recently Added** in Plus — anything from yesterday to process?
4. Open today's daily note (`Cmd+D`) and set intentions

### Throughout the Day
- **Got an idea?** → `Cmd+N` → type it → done (auto-saves to Plus)
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
2. Use the Project Template for structure
3. Set the `rank` in frontmatter (higher = more important)
4. Set the `area` to link to an Area of Effort

### Changing Project Priority
- Edit the `rank` number in frontmatter
- The [[Projects Dashboard]] auto-sorts by rank

### Changing Project Status
- Move the file between `Active/`, `Simmering/`, `Sleeping/` folders
- Right-click → "Move file to..." → type destination

---

## 💡 Tips & Best Practices

1. **Always start from Home Base** — it's your compass
2. **Capture first, organize later** — use Plus liberally
3. **Rank honestly** — if everything is rank 9, nothing is
4. **Link generously** — connections are where insights emerge
5. **Review regularly** — the system works best when maintained
6. **Don't over-organize** — good enough structure beats perfect structure

---

## ⚙️ Required Plugins

| Plugin | Status | Purpose |
|--------|--------|---------|
| **Dataview** | Required | Powers all dynamic dashboards and queries |
| **Daily Notes** (core) | Enabled | Creates daily notes with Cmd+D |
| **Templates** (core) | Enabled | Insert note templates |

### Optional but Recommended
- **Calendar** — Visual calendar for daily notes
- **Templater** — More powerful template variables
- **Quick Add** — Custom quick-capture commands

---

## 📚 Source

This system is based on Nick Milo's **Linking Your Thinking** methodology and the **Ideaverse** system.
- Video: [The Biggest Obsidian Upgrade I've Made in Years](https://youtube.com/watch?v=KekL4cLtpuc)
- Learn more: [Linking Your Thinking](https://www.linkingyourthinking.com/)

---

[[Atlas Dashboard]] ← Back to Atlas | [[Home Base]] ← Back to Home
