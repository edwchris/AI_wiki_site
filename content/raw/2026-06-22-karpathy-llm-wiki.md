# LLM Wiki — Andrej Karpathy

**Source:** Karpathy LLM Wiki GIST (shared by user)
**Date ingested:** 2026-06-22
**Author:** Andrej Karpathy
**Type:** Idea/pattern document

---

## Full text

A pattern for building personal knowledge bases using LLMs.

This is an idea file, it is designed to be copy pasted to your own LLM Agent (e.g. OpenAI Codex, Claude Code, OpenCode / Pi, or etc.). Its goal is to communicate the high level idea, but your agent will build out the specifics in collaboration with you.

### The core idea

Most people's experience with LLMs and documents looks like RAG: you upload a collection of files, the LLM retrieves relevant chunks at query time, and generates an answer. This works, but the LLM is rediscovering knowledge from scratch on every question. There's no accumulation. Ask a subtle question that requires synthesizing five documents, and the LLM has to find and piece together the relevant fragments every time. Nothing is built up. NotebookLM, ChatGPT file uploads, and most RAG systems work this way.

The idea here is different. Instead of just retrieving from raw documents at query time, the LLM incrementally builds and maintains a persistent wiki — a structured, interlinked collection of markdown files that sits between you and the raw sources. When you add a new source, the LLM doesn't just index it for later retrieval. It reads it, extracts the key information, and integrates it into the existing wiki — updating entity pages, revising topic summaries, noting where new data contradicts old claims, strengthening or challenging the evolving synthesis. The knowledge is compiled once and then kept current, not re-derived on every query.

This is the key difference: the wiki is a persistent, compounding artifact. The cross-references are already there. The contradictions have already been flagged. The synthesis already reflects everything you've read. The wiki keeps getting richer with every source you add and every question you ask.

You never (or rarely) write the wiki yourself — the LLM writes and maintains all of it. You're in charge of sourcing, exploration, and asking the right questions. The LLM does all the grunt work — the summarizing, cross-referencing, filing, and bookkeeping that makes a knowledge base actually useful over time. In practice, I have the LLM agent open on one side and Obsidian open on the other. The LLM makes edits based on our conversation, and I browse the results in real time — following links, checking the graph view, reading the updated pages. Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase.

### Use cases

- **Personal:** tracking goals, health, psychology, self-improvement — filing journal entries, articles, podcast notes
- **Research:** going deep on a topic over weeks/months — reading papers, articles, building a comprehensive wiki with evolving thesis
- **Reading a book:** filing each chapter as you go, building pages for characters, themes, plot threads (like fan wikis: Tolkien Gateway)
- **Business/team:** internal wiki maintained by LLMs, fed by Slack threads, meeting transcripts, project documents, customer calls
- **Other:** competitive analysis, due diligence, trip planning, course notes, hobby deep-dives

### Architecture

Three layers:

1. **Raw sources** — immutable source documents. Articles, papers, images, data files. LLM reads but never modifies.
2. **The wiki** — directory of LLM-generated markdown files. Summaries, entity pages, concept pages, comparisons, overview, synthesis. LLM owns this entirely.
3. **The schema** — document (CLAUDE.md for Claude Code, AGENTS.md for Codex) telling the LLM how the wiki is structured, conventions, and workflows. Co-evolved by human and LLM.

### Operations

**Ingest:** Drop source into raw collection, tell LLM to process it. LLM reads source, discusses key takeaways, writes summary page, updates index, updates entity/concept pages, appends to log. A single source might touch 10-15 wiki pages.

**Query:** Ask questions against the wiki. LLM searches relevant pages, reads them, synthesizes answer with citations. Answers can be markdown pages, comparison tables, slide decks (Marp), charts (matplotlib), canvases. Good answers should be filed back into the wiki.

**Lint:** Periodically ask LLM to health-check the wiki. Look for: contradictions, stale claims, orphan pages, important concepts lacking their own page, missing cross-references, data gaps.

### Indexing and logging

**index.md** — content-oriented catalog. Each page listed with link, one-line summary, optional metadata. LLM reads this first on queries. Updated on every ingest.

**log.md** — chronological, append-only record. Format: `## [YYYY-MM-DD] ingest | Article Title`. Parseable with unix tools: `grep "^## \[" log.md | tail -5`

### Optional CLI tools

- **qmd** — local search engine for markdown files with hybrid BM25/vector search and LLM re-ranking. Has CLI and MCP server.

### Tips and tricks

- **Obsidian Web Clipper** — browser extension that converts web articles to markdown
- **Download images locally** — Obsidian Settings → Files and links → Attachment folder path = `raw/assets/`. Bind "Download attachments for current file" to hotkey (e.g. Ctrl+Shift+D)
- **Graph view** — best way to see shape of wiki, identify hubs and orphans
- **Marp** — markdown-based slide deck format, Obsidian plugin available
- **Dataview** — Obsidian plugin running queries over page frontmatter
- **Git** — wiki is just a git repo of markdown files; version history, branching, collaboration

### Why this works

Tedious part of maintaining a knowledge base: bookkeeping (updating cross-references, keeping summaries current, noting contradictions, maintaining consistency). Humans abandon wikis because maintenance burden grows faster than value. LLMs don't get bored, don't forget to update a cross-reference, can touch 15 files in one pass.

Human's job: curate sources, direct analysis, ask good questions, think about what it all means. LLM's job: everything else.

### Historical precedent

Related in spirit to Vannevar Bush's **Memex** (1945) — personal, curated knowledge store with associative trails between documents. Bush's vision was closer to this than what the web became: private, actively curated, with connections between documents as valuable as the documents themselves. The part Bush couldn't solve was maintenance. The LLM handles that.
