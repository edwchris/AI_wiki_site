---
title: "Obsidian"
aliases: ["Obsidian"]
type: concept
tags: [tooling, knowledge-management, markdown, obsidian]
created: 2026-06-22
updated: 2026-06-22
sources: [2026-06-22-karpathy-llm-wiki]
---

# Obsidian

## Definition
A local-first, markdown-based personal knowledge management (PKM) tool. Files are plain `.md` stored on disk; Obsidian provides linking, graph visualization, plugins, and a rich editing experience on top.

## Role in the [[LLM Wiki Pattern]]
In the [[LLM Wiki Pattern]], Obsidian serves as the **IDE** — the interface through which the human browses and navigates the LLM-maintained wiki. The LLM edits markdown files; Obsidian renders them with backlinks, graph view, and plugin features.

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase." — [[Andrej Karpathy]]

## Key features relevant to wiki work
| Feature | Use |
|---------|-----|
| Graph view | See connectivity; identify hubs and orphan pages |
| Backlinks panel | See all pages that link to the current page |
| `\[\[wikilinks\]\]` | Navigate between pages; foundation of the link graph |
| [[Dataview]] plugin | Query YAML frontmatter for dynamic tables and lists |
| [[Marp]] plugin | Render wiki content as slide decks |
| Obsidian Web Clipper | Browser extension — converts web articles to markdown |
| Canvas | Visual boards linking wiki pages |
| Hotkeys | Bind "Download attachments" to Ctrl+Shift+D for local image caching |

## Setup tips for LLM Wiki Pattern
- **Attachment folder:** Settings → Files and links → Attachment folder path = `raw/assets/`
- **Download hotkey:** Settings → Hotkeys → search "Download" → bind "Download attachments for current file"
- **Templates:** Point Obsidian's Templates plugin to the `templates/` directory

## Limitations
- LLMs can't read markdown with inline images in one pass; workaround: LLM reads text first, then views images separately
- Not collaborative by default (no live co-editing); use Git for version control and async collaboration

## Where it appears
- [[LLM Wiki Pattern — Karpathy]] — recommended as the wiki browsing environment
