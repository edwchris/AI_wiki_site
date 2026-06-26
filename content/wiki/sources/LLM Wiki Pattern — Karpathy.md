---
title: "LLM Wiki Pattern — Karpathy"
aliases: ["LLM Wiki Pattern — Karpathy"]
type: source
tags: [knowledge-management, llm, workflow, obsidian]
created: 2026-06-22
updated: 2026-06-22
sources: [2026-06-22-karpathy-llm-wiki]
author: "Andrej Karpathy"
url: ""
raw_file: "raw/2026-06-22-karpathy-llm-wiki.md"
---

# LLM Wiki Pattern — Karpathy

**Author:** [[Andrej Karpathy]] | **Date:** 2026-06-22 | **Type:** Idea/pattern document

## One-line summary
A pattern for using LLMs as active wiki maintainers rather than passive RAG retrievers, building a persistent, compounding knowledge base from curated sources.

## Key claims
- RAG re-derives knowledge from scratch on every query — no accumulation
- A persistent LLM-maintained wiki compiles knowledge once and keeps it current
- The wiki is a compounding artifact: cross-references pre-built, contradictions pre-flagged, synthesis pre-done
- Humans curate sources and ask questions; LLMs do all bookkeeping and maintenance
- The maintenance burden is why humans abandon wikis — LLMs eliminate that cost
- [[Obsidian]] as IDE, LLM as programmer, wiki as codebase

## Key concepts introduced or covered
- [[LLM Wiki Pattern]] — the core idea this document defines
- [[Retrieval-Augmented Generation]] — the contrasting approach being critiqued
- [[Obsidian]] — the recommended tool for browsing the wiki
- Ingest / Query / Lint — the three primary operations
- Schema file (CLAUDE.md / AGENTS.md) — configuration that disciplines the LLM

## Notable quotes
> "The LLM is rediscovering knowledge from scratch on every question. There's no accumulation."

> "Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase."

> "Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don't get bored."

> "The human's job is to curate sources, direct the analysis, ask good questions, and think about what it all means. The LLM's job is everything else."

## Historical precedent
- [[Vannevar Bush]]'s **[[Memex]]** (1945) — personal curated knowledge store with associative trails. The part Bush couldn't solve (maintenance) is what LLMs now handle.

## Architecture (three layers)
1. **Raw sources** — immutable; LLM reads, never writes
2. **Wiki** — LLM-owned markdown files; summaries, entities, concepts, analyses
3. **Schema** — CLAUDE.md/AGENTS.md; co-evolved instructions for LLM behavior

## Operations
| Operation | Trigger | Pages touched |
|-----------|---------|---------------|
| Ingest | New source added | 10-15 pages typical |
| Query | User asks question | Read index, drill into relevant pages; file good answers back |
| Lint | Periodic health check | Scan for contradictions, orphans, gaps |

## Recommended tooling
| Tool | Purpose |
|------|---------|
| [[Obsidian]] | Wiki browser and IDE |
| Obsidian Web Clipper | Convert web articles to markdown for raw/ |
| Marp | Markdown-based slide decks |
| Dataview | Query frontmatter for dynamic tables |
| qmd | Local search engine (BM25+vector) for large wikis |
| Git | Version history and collaboration |

## Use cases covered
- Personal knowledge / self-tracking
- Research over weeks/months
- Book reading companions
- Team/business internal wikis
- Competitive analysis, due diligence, hobby deep-dives

## How it connects
- This document is the **founding source** of this wiki
- Inspired by: [[Vannevar Bush]] Memex (1945)
- Contrasts with: [[Retrieval-Augmented Generation]]

## Open questions raised
- At what scale does the index file break down and search tooling become necessary?
- How do team wikis handle conflicting LLM edits from multiple agents?
- What's the right cadence for lint passes?
