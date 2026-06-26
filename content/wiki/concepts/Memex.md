---
title: "Memex"
aliases: ["Memex"]
type: concept
tags: [historical, knowledge-management, hypertext, vannevar-bush]
created: 2026-06-22
updated: 2026-06-22
sources: [2026-06-22-karpathy-llm-wiki]
---

# Memex

## Definition
A hypothetical personal knowledge device proposed by [[Vannevar Bush]] in his 1945 essay "As We May Think." A desk-like machine using microfilm storage that would let a person store, retrieve, and traverse their personal library of documents via "associative trails" — manually created links between related items.

## How it works (as envisioned)
- Microfilm-based storage of books, records, communications
- User creates **associative trails** — named, reusable link paths between related documents
- Trails can be shared with others ("memex to memex")
- Index tabs and levers for rapid navigation between items in a trail

## Key properties
- **Private** — personal device, not a shared public network
- **Actively curated** — user builds and maintains the trails
- **Associative** — links by conceptual relevance, not hierarchical taxonomy
- **Persistent** — trails accumulate over time; the value compounds

## Why it never got built
Bush's vision was pre-digital and never realized in the form he described. The web eventually emerged but went in a different direction: public, hierarchical (URLs), search-indexed, and largely non-personal. The **maintenance problem** — who creates and keeps the associative links current — was never solved for individuals.

## Connection to [[LLM Wiki Pattern]]
[[Andrej Karpathy]] explicitly positions the LLM Wiki Pattern as the realized form of the Memex:

> "Bush's vision was closer to this than to what the web became: private, actively curated, with the connections between documents as valuable as the documents themselves. The part he couldn't solve was who does the maintenance. The LLM handles that."

| Memex element | LLM Wiki equivalent |
|--------------|-------------------|
| Associative trails | Wikilinks in [[Obsidian]] |
| Personal device | Local markdown files |
| Active curation | Human curates sources; LLM maintains links |
| Maintenance problem | Solved — LLM does all bookkeeping |

## Historical significance
- Cited as a conceptual precursor to hypertext (Ted Nelson, Doug Engelbart)
- Influenced the early web (Tim Berners-Lee cited Bush)
- Predated the internet by ~40 years
- The web solved the "public knowledge" version; the Memex solved the "personal knowledge" version — and LLMs are now making that feasible

## Where it appears
- [[LLM Wiki Pattern — Karpathy]] — cited as historical precedent
- [[Vannevar Bush]] — the entity page for its inventor
- [[LLM Wiki Pattern]] — historical context section
