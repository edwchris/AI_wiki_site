# AI Wiki — Schema & Operating Instructions

## Purpose
This is a personal knowledge base about AI, built using the Karpathy LLM Wiki Pattern. The LLM maintains the wiki; the human curates sources and asks questions. Knowledge compounds over time rather than being re-derived on every query.

## Directory Structure

```
AI_wiki/
├── CLAUDE.md          ← this file; schema and instructions
├── index.md           ← content catalog of all wiki pages
├── log.md             ← append-only chronological record
├── raw/               ← immutable source documents (never modify)
│   └── assets/        ← downloaded images and attachments
├── wiki/              ← LLM-generated and maintained pages
│   ├── concepts/      ← topic pages (techniques, ideas, architectures)
│   ├── entities/      ← named things (models, people, orgs, papers)
│   ├── sources/       ← one summary page per raw source
│   └── analyses/      ← comparison tables, synthesis, Q&A output
├── projects/          ← project index pages (connector layer — not knowledge)
└── templates/         ← page templates (do not use directly)
```

## Page Conventions

### Frontmatter (YAML)
Every wiki page must have frontmatter:
```yaml
---
title: "Page Title"
aliases: ["Page Title"]
type: concept | entity | source | analysis
tags: [tag1, tag2]
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [source-slug-1, source-slug-2]   # which raw sources informed this page
---
```

> **Why `aliases`?** Obsidian resolves wikilinks by filename, not by the `title` field. Since files use `kebab-case.md` but wikilinks use `[[Page Title]]`, every page needs `aliases: ["Page Title"]` so Obsidian can match them. Always set `aliases` to the same value as `title`.

### Naming
- Files: `Display Name.md` — match the page title exactly (e.g. `Andrej Karpathy.md`, `LLM Wiki Pattern.md`)
- Exception: source files may use a date-slug prefix when the title contains characters illegal on Windows (`?`, `:`) — in that case, drop the illegal character from both the filename and the wikilink
- Wikilinks: `[[Page Title]]` — resolves directly to the matching filename; no alias tricks needed
- Source slugs: `YYYY-MM-DD-author-short-title` (e.g. `2026-06-22-karpathy-llm-wiki`)

### Cross-references
- Link liberally between pages using `[[wikilinks]]`
- Every entity and concept mentioned in a source summary should link to its own page
- Orphan pages (no inbound links) should be flagged during lint

## Projects Layer

The `projects/` folder contains **connector pages**, not knowledge pages. Each project page links the wiki's knowledge to a real-world deliverable (paper, course, grant, portfolio). The LLM maintains the wiki; the human maintains the project workspace.

### What a project page contains
- **Goal** — one sentence stating the deliverable
- **Key wiki connections** — links to the concepts, sources, and analyses most relevant to this project
- **Wiki gaps** — `> [!question]` callouts listing what the wiki *lacks* that this project needs; these are the ingest priorities for next sessions
- **External workspace** — a pointer to where the actual project work lives (Overleaf, Teams, personal vault)

### What a project page does NOT contain
- Knowledge (that belongs in `wiki/`)
- Tasks, drafts, or in-progress writing (that belongs in the external workspace)
- Personal career management detail (belongs in a separate personal vault)

### Project page frontmatter
```yaml
---
title: "Project Name"
type: project
status: active | planning | on-hold | complete
tags: [project, ...]
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

### How to work with a project
- **"Update project X"** — re-read index.md, re-read the project page, refresh the key connections and gaps sections
- **"What does project X need from the wiki?"** — read the project's Wiki gaps section and report the `[!question]` items
- **"Ingest for project X"** — treat the project's wiki gaps as the ingest priority list
- **"New project: [name and goal]"** — create a new project page, populate connections from existing wiki, flag gaps

Project pages are listed in `index.md` under a Projects section. Update the Projects section of index.md whenever a project page is created or its status changes. Append to log.md with format: `## [YYYY-MM-DD] project | Project Name`

## Operations

### Ingest a new source
1. Read the source file in `raw/`
2. Discuss key takeaways with the user
3. Write a summary page in `wiki/sources/` using the source template
4. Create or update concept pages in `wiki/concepts/` for each major idea
5. Create or update entity pages in `wiki/entities/` for each named thing (model, person, org, paper)
6. Update `index.md` with the new source page and any new wiki pages
7. Append an entry to `log.md` with format: `## [YYYY-MM-DD] ingest | Source Title`

### Answer a query
1. Read `index.md` to identify relevant pages
2. Read those pages
3. Synthesize an answer with inline citations (e.g. `[[page-title]]`)
4. If the answer is substantial (a comparison, analysis, or synthesis), save it as a new page in `wiki/analyses/`
5. Update `index.md` and `log.md` if a new page was created

### Lint the wiki
Check for and report:
- Contradictions between pages (flag with `> [!warning] Contradiction`)
- Stale claims superseded by newer sources
- Orphan pages (no inbound links)
- Concepts mentioned but lacking their own page
- Missing cross-references between related pages
- Data gaps that a web search could fill

## Callout Conventions (Obsidian)
- `> [!note]` — supplementary context
- `> [!important]` — key insight worth emphasizing
- `> [!warning]` — contradiction, uncertainty, or stale claim
- `> [!question]` — open question or gap to investigate

## Domain Focus
This wiki covers **AI and machine learning** — models, architectures, training techniques, inference, tooling, research papers, people, organizations, and industry trends. Secondary focus on AI epistemics: how to evaluate claims, track progress, and understand limitations.

## Scale Expectations
- Sources: hundreds over time
- Wiki pages: potentially thousands
- At ~100 sources, the index file is sufficient for navigation
- Beyond that, consider `qmd` or a search script

## Style
- Pages should be dense with information, not padded
- Prefer bullet points and tables over prose paragraphs
- Use headers (##, ###) to organize long pages
- Avoid repeating information that lives on another page — link instead
- Keep source summary pages factual; save opinions/synthesis for concept and analysis pages
