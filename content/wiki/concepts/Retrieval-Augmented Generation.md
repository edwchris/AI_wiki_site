---
title: "Retrieval-Augmented Generation"
aliases: ["Retrieval-Augmented Generation", "RAG"]
type: concept
tags: [rag, llm, architecture, information-retrieval]
created: 2026-06-22
updated: 2026-06-22
sources: [2026-06-22-karpathy-llm-wiki]
---

# Retrieval-Augmented Generation

## Definition
A technique where an LLM's response is grounded by first retrieving relevant chunks from a document corpus (typically via vector search), then generating an answer conditioned on those chunks. Combines parametric knowledge (model weights) with non-parametric, updatable external knowledge.

## How it works
1. Query is embedded into a vector
2. Nearest-neighbor search over a pre-indexed vector store returns top-k chunks
3. Retrieved chunks are inserted into the LLM's context
4. LLM generates a response conditioned on those chunks

## Key properties
- **Updatable** — add new documents without retraining
- **Citable** — can attribute claims to source chunks
- **Stateless** — no accumulation; each query re-derives from scratch
- **Chunk-level** — retrieval unit is a chunk, not a synthesized concept

## Limitations (relative to [[LLM Wiki Pattern]])
- Re-derives knowledge from scratch on every query
- Multi-hop questions require the right chunks to co-occur in the retrieved set
- No pre-built cross-references or contradiction detection
- Knowledge doesn't compound — asking the same question 100 times yields the same starting point
- The synthesis burden falls on the LLM at query time, not at ingest time

## Common implementations
- **[[NotebookLM]]** — Google's RAG-based document Q&A
- **[[ChatGPT]]** file uploads — ad-hoc RAG over uploaded files
- **[[LangChain]]** / **[[LlamaIndex]]** — RAG frameworks
- **[[Perplexity]]** — RAG over live web results

## When RAG is preferred over [[LLM Wiki Pattern]]
- Need to search verbatim passages in large immutable corpora
- Sources are too numerous or too frequently updated to maintain a wiki
- The query pattern is lookup-style ("find the section that says X") rather than synthesis-style
- Infrastructure for a persistent wiki is unavailable

## Open questions
- Can hybrid approaches combine RAG (for recall) with a wiki layer (for synthesis)?
- At what corpus size does the wiki pattern's index-file navigation break down relative to vector search?

## Where it appears
- [[LLM Wiki Pattern — Karpathy]] — used as the contrasting baseline
