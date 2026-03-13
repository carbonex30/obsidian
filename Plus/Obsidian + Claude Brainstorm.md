* prompted Claude on ways obsidian have been integrated with claude
* https://claude.ai/chat/0760b41f-2709-4b6f-beca-cf90dd53be78

## Question
* what are the most popular implementation of using claude code alongside obsidian as a assistant of sorts. what were the ways in which claude code was integrated into obsidian, where there specific patterns and skills that were utilized within this union?

## Answer
* This is a rich and rapidly evolving space. Here's a comprehensive breakdown of what the community has converged on:

---

## The Core Insight: Why This Pairing Works

An Obsidian vault is essentially a codebase of markdown files stored in the filesystem and accessible to other applications — and Claude Code is already excellent at navigating file structures and making surgical edits. The tasks people avoid in Obsidian — organization, consistency, following procedures, grunt work — are exactly what AI excels at.

---

## The 5 Main Integration Patterns

**Pattern A — Direct Access (Zero Setup)** The simplest approach. Claude Code can already read and edit your vault with no configuration needed. You just navigate to your vault directory and launch Claude, then ask things like "Read my daily note from today" or "Find all notes mentioning project X."

**Pattern B — CLAUDE.md (The Most Universal Pattern)** This is the cornerstone of almost every serious workflow. Claude is brilliant but forgetful — every conversation starts fresh. The fix is a file called CLAUDE.md. It's not documentation; it's an instruction manual for your personal assistant. When Claude makes a mistake, you teach it and add a rule.

The key insight is that CLAUDE.md is not about telling the agent what it _is_ — it's about telling the agent how your world works: project structure, naming conventions, where things live, what to never touch.

At the root of the vault sits a CLAUDE.md roughly 200 lines long. It tells Claude Code what the vault is, how it is organized, what conventions to follow, and what not to do. A well-structured frontmatter schema — using fields like `type`, `role`, `status`, and `themes` — creates an interface that both a human mind and an AI collaborator can navigate.

**Pattern C — MCP Plugin (Real-Time Bidirectional)** The `obsidian-claude-code-mcp` plugin implements a dual-transport MCP server supporting both WebSocket for Claude Code and HTTP/SSE for Claude Desktop. Claude Code automatically discovers and connects to Obsidian vaults through WebSocket on port 22360. This provides file read/write operations, workspace context (active file and vault structure), and support for multiple simultaneous vaults on unique ports.

**Pattern D — Claudesidian (Semantic Search + Agent Mode)** Claudesidian MCP is an Obsidian plugin that goes further, implementing atomic vault operations and a structured memory system. It uses an agent-mode architecture organized into logical domains with specific operation modes, and adds semantic search via Ollama embeddings.

**Pattern E — Claudian (Full IDE-in-Obsidian)** Claudian embeds Claude Code directly as an AI collaborator inside Obsidian itself, with features like an @-mention dropdown for MCP servers and vault files, inline text editing with word-level diff preview, slash commands for custom prompt templates, plan mode (Shift+Tab) where Claude explores before implementing, and custom agent management. Skills are loaded from `~/.claude/skills/` or `{vault}/.claude/skills/`.

---

## The Official Skills Layer (Kepano/Obsidian CEO)

In January 2026, Kepano (Steph Ango, Obsidian's CEO) released an official set of Claude Code skills via the `kepano/obsidian-skills` repo. It contains 44 skills — `obsidian-markdown` covers rules for `.md` files including correct wikilink and frontmatter syntax; `obsidian-bases` handles Obsidian's database layer; `json-canvas` handles `.canvas` spatial note maps; and `/defuddle` strips web pages to clean markdown before saving, cutting token cost by removing ads and navigation before content reaches Claude.

---

## The Most Popular Use Cases

Common automation workflows include: asking Claude to "read my journal entry from today and add backlinks to all people, places, and books mentioned" (Claude searches the vault for existing entity notes, creates new ones if needed, and adds wiki-links throughout — what would take 10–15 minutes of manual work happens in seconds); converting rough brain-dump notes into properly formatted book reviews with sections; and applying mental model checklists to decision-making by walking through each model systematically.

Advanced setups teach Claude to search through everything in the vault including PDFs — using macOS Spotlight (`mdfind`) to search not just markdown notes but research papers, scanned documents, and random PDFs accumulated over years. With `textutil`, Claude can extract text from practically any document format.

---

## The Community's #1 Rule

The most-cited guideline from the community: your vault should contain your authentic thinking. Claude reads it for context but shouldn't pollute it with generated content. Keep Claude's outputs (plans, memory) in `~/.claude/` and your knowledge in the vault proper.

---

## The Experimental Frontier

Some community members have pushed into multi-agent territory — one example being a `/deep-recon` skill where four agents (Explorer, Associator, Critic, Synthesizer) run in parallel rounds. The Explorer casts a wide net across the web and your notes while the Associator finds structural parallels. The caveat: it can burn tokens fast.

The **COG pattern** (mentioned in the skills marketplace) represents the self-evolving end of the spectrum — combining Git versioning, automation hooks, and self-healing wikilink references so the vault can maintain its own integrity over time.

---

Given your existing familiarity with Claude Code, CLAUDE.md workflows, and custom slash commands, you'd likely get the most mileage starting with the official `kepano/obsidian-skills` drop-in and the `obsidian-claude-code-mcp` plugin — those two together cover 80% of what the community is doing without a lot of overhead.*