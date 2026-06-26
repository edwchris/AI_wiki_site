---
title: "Wiki Index"
type: index
updated: 2026-06-22
---

# Wiki Index

Content catalog. The LLM reads this first when answering queries to identify relevant pages. Updated on every ingest or page creation.

---

## Sources
One page per raw source ingested.

| Page | Summary | Date |
|------|---------|------|
| [[LLM Wiki Pattern — Karpathy]] | Karpathy's pattern for building personal knowledge bases using LLMs as wiki maintainers | 2026-06-22 |
| [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]] | Meta-analysis of 106 experiments: human–AI synergy is negative on average; creation tasks and human-dominant tasks are exceptions | 2026-06-22 |
| [[Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021]] | Field study: 5 high-accuracy ML tools failed in clinical practice because models capture know-what but not know-how | 2026-06-27 |

---

## Concepts
Topic pages covering techniques, ideas, and architectures.

| Page | Summary |
|------|---------|
| [[LLM Wiki Pattern]] | The core pattern: persistent, compounding wiki maintained by LLMs instead of RAG re-derivation |
| [[Retrieval-Augmented Generation]] | Standard RAG pattern — contrasted with the wiki pattern |
| [[Obsidian]] | Markdown-based personal knowledge management tool used as the wiki IDE |
| [[Memex]] | Vannevar Bush's 1945 vision for a personal knowledge device; spiritual precursor to the wiki pattern |
| [[Human-AI Synergy]] | When human–AI combinations outperform either alone; key moderators: task type, relative performance |
| [[AI Ground Truth]] | The reliability problem with ML training labels: ground truth captures know-what but not the know-how experts use to handle uncertainty |

---

## Entities
Named things: models, people, organizations, papers.

| Page | Summary |
|------|---------|
| [[Andrej Karpathy]] | AI researcher, former OpenAI/Tesla, author of the LLM Wiki pattern |
| [[Vannevar Bush]] | Author of "As We May Think" (1945); Memex concept precursor to the wiki pattern |
| [[Michelle Vaccaro]] | MIT researcher; lead author of 2024 human–AI synergy meta-analysis |
| [[Thomas Malone]] | MIT CCI founding director; co-author of 2024 human–AI synergy meta-analysis |
| [[MIT Center for Collective Intelligence]] | MIT research center on human–computer collective intelligence |
| [[Sarah Lebovitz]] | UVA McIntire researcher; lead author of 2021 MISQ AI ground truth study |
| [[Natalia Levina]] | NYU Stern researcher; co-author of 2021 MISQ AI ground truth study |
| [[Hila Lifshitz-Assaf]] | Warwick Business School researcher; co-author of 2021 MISQ AI ground truth study |

---

## Analyses
Comparisons, syntheses, and Q&A outputs worth preserving.

| Page | Summary |
|------|---------|

---

## Stubs needed
Pages linked in wiki but not yet created (unresolved links — visible in Obsidian graph):
- `[[OpenAI]]` — major entity; referenced in Karpathy affiliations
- `[[Tesla]]` — referenced in Karpathy affiliations
- `[[Eureka Labs]]` — Karpathy's AI education company (2024–)
- `[[nanoGPT]]` — Karpathy's minimal GPT implementation
- `[[micrograd]]` — Karpathy's tiny autograd engine
- `[[NotebookLM]]` — Google's RAG-based Q&A product
- `[[ChatGPT]]` — OpenAI's consumer product
- `[[LangChain]]` — popular RAG/agent framework
- `[[LlamaIndex]]` — RAG framework
- `[[Perplexity]]` — AI search engine using RAG over web
- `[[qmd]]` — local markdown search engine (BM25+vector)
- `[[Marp]]` — markdown slide deck format
- `[[Dataview]]` — Obsidian plugin for frontmatter queries
- `[[Abdullah Almaatouq]]` — MIT co-author of Vaccaro et al. 2024; no entity page yet

## Orphan Watch
Pages with no inbound links (flag during lint):
- *(none detected — 2026-06-22 lint pass)*

## Suggested sources to ingest
- "As We May Think" — Vannevar Bush (1945, The Atlantic) — foundational text behind the Memex
- Karpathy's nanoGPT README — would enrich entity pages for nanoGPT, micrograd
- qmd documentation — to fill the qmd stub
