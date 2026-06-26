---
title: "LLM Wiki Pattern"
aliases: ["LLM Wiki Pattern"]
type: concept
tags: [knowledge-management, llm, workflow, meta]
created: 2026-06-22
updated: 2026-06-22
sources: [2026-06-22-karpathy-llm-wiki]
---

# LLM Wiki Pattern

## Definition
A methodology for building personal (or team) knowledge bases where an LLM incrementally writes and maintains a structured wiki from curated raw sources — rather than performing retrieval at query time. Knowledge is compiled once and kept current; synthesis compounds over time.

> [!important] Core insight
> The bottleneck in traditional wikis is human maintenance. LLMs eliminate this bottleneck, making persistent, richly cross-referenced knowledge bases economically viable for individuals.

## How it works

### Three-layer architecture
| Layer | Owner | Contents |
|-------|-------|---------|
| Raw sources | Human (immutable) | Articles, papers, transcripts, images |
| Wiki | LLM | Summaries, entity/concept pages, analyses, cross-references |
| Schema | Human + LLM | Operating instructions (CLAUDE.md) |

### Three operations
**Ingest** — when a new raw source is added:
1. LLM reads source
2. Discusses key takeaways with human
3. Writes summary page (`wiki/sources/`)
4. Creates/updates concept pages (`wiki/concepts/`)
5. Creates/updates entity pages (`wiki/entities/`)
6. Updates `index.md`
7. Appends to `log.md`
A single source typically touches 10–15 pages.

**Query** — when the human asks a question:
1. LLM reads `index.md` to find relevant pages
2. Reads those pages
3. Synthesizes answer with inline citations
4. Files substantial answers back as `wiki/analyses/` pages

**Lint** — periodic health check:
- Find contradictions between pages
- Flag stale claims superseded by newer sources
- Identify orphan pages (no inbound links)
- Note concepts mentioned but lacking their own page
- Suggest new sources or questions to investigate

## Key properties
- **Compounding** — each source enriches all related existing pages, not just its own summary
- **Pre-synthesized** — cross-references and contradictions resolved at ingest time, not query time
- **LLM-maintained** — human never writes wiki content; LLM handles all bookkeeping
- **Observable** — wiki is just markdown files; human can browse graph view, read pages, catch errors
- **Evolvable** — schema (CLAUDE.md) co-evolved as the domain grows

## Comparison with related approaches

| | LLM Wiki Pattern | Standard RAG | NotebookLM |
|-|-----------------|-------------|-----------|
| Knowledge accumulation | Yes — compounding | No — re-derived each time | No |
| Pre-built cross-references | Yes | No | No |
| Human maintenance required | No — LLM does it | Minimal | Minimal |
| Infrastructure needed | Just markdown files | Vector DB, embeddings | Proprietary |
| Browsable by human | Yes (Obsidian) | No | Limited |
| Works offline | Yes | Depends | No |
| Compounds over queries | Yes (file analyses back) | No | No |

## Comparison with [[Retrieval-Augmented Generation]]
RAG retrieves chunks of raw source at query time. The wiki pattern compiles knowledge ahead of time. RAG is good for "find me the passage that says X"; the wiki pattern is good for "what does everything I've read say about X, synthesized."

## Recommended tooling
- **[[Obsidian]]** — markdown wiki browser; graph view shows connectivity
- **Obsidian Web Clipper** — converts web pages to markdown for raw/
- **[[qmd]]** — BM25+vector search for large wikis (CLI + MCP)
- **[[Marp]]** — generate slide decks from wiki content
- **[[Dataview]]** — query frontmatter for dynamic tables in Obsidian
- **Git** — version history and branching

## Scale considerations
- < ~100 sources: `index.md` sufficient for navigation
- 100–500 sources: consider adding qmd or a search script
- 500+: full search infrastructure warranted

## Where it appears
- [[LLM Wiki Pattern — Karpathy]] — original document defining this pattern

## Historical context
Spiritually related to [[Vannevar Bush]]'s **[[Memex]]** (1945): a personal, actively curated knowledge store with associative trails between documents. Bush's vision was more like this than what the web became. The unsolved problem — who does the maintenance — is what LLMs now handle.

## Open questions
- How do contradictions get resolved when sources are approximately equally authoritative?
- What's the optimal ingest unit size (per-article vs. per-chapter vs. per-paragraph)?
- For team wikis: how to handle concurrent LLM edits without conflicts?

> [!question] Research gap
> No public benchmarks exist for comparing wiki-pattern knowledge retention vs. RAG on multi-hop questions over large corpora.
