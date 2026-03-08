---
tags:
  - concept
  - system
---

# Home Base System

> The central navigation hub for your Obsidian vault, built on the [[ACE Framework]].

## What is Home Base?

Home Base is a single note that serves as your **command center** for navigating your entire knowledge management system. Instead of relying on scattered navigation, complex plugin configurations, or remembering folder structures, you start every session from Home Base.

## How It Works

1. **Open Obsidian** → Go to [[Home Base]]
2. **Decide what you need:**
   - Manage projects → [[Projects Dashboard]]
   - Capture ideas → [[Plus Inbox]]
   - Review past work → [[Calendar Dashboard]]
   - Find knowledge → [[Atlas Dashboard]]
3. **Take action** — then return to Home Base when you need to reorient

## Key Benefits

- **Eliminates navigation friction** — one click to get anywhere
- **Provides visual overview** — see active projects, recent captures, and daily notes at a glance
- **Reduces cognitive load** — no need to remember folder structures
- **Scales gracefully** — works whether you have 10 notes or 10,000

## Design Principles

- Keep it clean and scannable
- Use Dataview queries for dynamic, always-current information
- Link to dashboards, not individual notes (dashboards handle the details)
- Review and adjust weekly

## Vault Configuration

Key settings in `.obsidian/app.json` that support this system:

| Setting | Value | Effect |
|---|---|---|
| `newFileLocation` | `folder` | New notes go to a fixed folder instead of the current one |
| `newFileFolderPath` | `Plus` | `Ctrl+N` / `Cmd+N` always creates notes in `Plus/` (the inbox) |
| `attachmentFolderPath` | `Extras` | Pasted images and files go to `Extras/` |

> [!note] QuickAdd commands (New Project, New Daily Note, etc.) have their own destination folders set independently and are unaffected by `newFileFolderPath`.

## Source

From Nick Milo's Linking Your Thinking / Ideaverse system.
- Video: [The Biggest Obsidian Upgrade I've Made in Years](https://youtube.com/watch?v=KekL4cLtpuc)

---

[[Atlas Dashboard]] ← Back to Atlas | [[Home Base]] ← Back to Home
