# Wiki Log

Append-only chronological record. Each entry starts with `## [YYYY-MM-DD] operation | Title`.

Parse last 5 entries: `grep "^## \[" log.md | tail -5`

---

## [2026-06-22] init | Wiki initialized

- Created directory structure: `raw/`, `raw/assets/`, `wiki/concepts/`, `wiki/entities/`, `wiki/sources/`, `wiki/analyses/`, `templates/`
- Created `CLAUDE.md` schema
- Created `index.md`
- Created `log.md`
- Created templates: source, concept, entity, analysis

## [2026-06-22] lint | First lint pass

Findings:
- **No orphan pages** — all 6 pages have inbound links
- **No contradictions** detected across 6 wiki pages
- **1 missing concept page** created: `wiki/concepts/memex.md` (referenced 4× without a page)
- **13 unresolved wikilinks** added (stubs to create): OpenAI, Tesla, Eureka Labs, nanoGPT, micrograd, NotebookLM, ChatGPT, LangChain, LlamaIndex, Perplexity, qmd, Marp, Dataview
- **Missing cross-references fixed**: added `[[Memex]]` links in vannevar-bush.md, llm-wiki-pattern.md, llm-wiki-pattern-karpathy.md; added entity links in andrej-karpathy.md and retrieval-augmented-generation.md
- **index.md** updated with Stubs needed, Orphan Watch, and Suggested sources sections
- **Minor inconsistency noted**: lint description in `llm-wiki-pattern.md` omits "data gaps fillable by web search" listed in CLAUDE.md — acceptable divergence, not corrected

## [2026-06-22] ingest | When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024

Source: `raw/2024-12-vaccaro-human-ai-meta-analysis.pdf`
Pages created:
- `wiki/sources/2024-12-vaccaro-human-ai-meta-analysis.md` (new)
- `wiki/concepts/human-ai-synergy.md` (new)
- `wiki/entities/michelle-vaccaro.md` (new)
- `wiki/entities/thomas-malone.md` (new)
- `wiki/entities/mit-center-for-collective-intelligence.md` (new)
- `index.md` (updated)

## [2026-06-27] lint | Second lint pass

Findings:
- **No orphan pages** — all 17 pages have inbound links ✓
- **No contradictions** detected across all pages ✓
- **3 bugs fixed**:
  - `index.md`: ground truth source wikilink still had `?` — corrected
  - `Human-AI Synergy.md`: `[[Human Augmentation]]` was a wikilink to itself (concept defined inline) — removed brackets
  - `index.md`: added `[[Abdullah Almaatouq]]` stub (co-author of Vaccaro 2024, no entity page)
- **14 stubs remain** (unchanged + Abdullah Almaatouq added): OpenAI, Tesla, Eureka Labs, nanoGPT, micrograd, NotebookLM, ChatGPT, LangChain, LlamaIndex, Perplexity, qmd, Marp, Dataview, Abdullah Almaatouq
- **Floating citation**: `Donahue et al. 2022` cited in `Human-AI Synergy.md` (conditions for synergy) — no source page; flag for future ingest
- **Partial source coverage**: `Is AI Ground Truth Really True` ingested from web summaries only (PDF unreadable); page may be missing detail from full paper

## [2026-06-27] ingest | Is AI Ground Truth Really True? — Lebovitz, Levina & Lifshitz-Assaf 2021

Source: `raw/Lebovitz, Levina, Lifshitz-Assaf, MISQ, 2021.pdf`
Note: PDF not directly readable (no pdftoppm); content sourced from web (SSRN abstract, AIS eLibrary, Warwick repository).
Pages created:
- `wiki/sources/2021-lebovitz-levina-lifshitz-assaf-ai-ground-truth.md` (new)
- `wiki/concepts/ai-ground-truth.md` (new)
- `wiki/entities/sarah-lebovitz.md` (new)
- `wiki/entities/natalia-levina.md` (new)
- `wiki/entities/hila-lifshitz-assaf.md` (new)
- `wiki/concepts/human-ai-synergy.md` (updated — added cross-reference)
- `index.md` (updated)

## [2026-06-22] ingest | LLM Wiki — Andrej Karpathy

Source: `raw/2026-06-22-karpathy-llm-wiki.md`
Pages created/updated:
- `wiki/sources/llm-wiki-pattern-karpathy.md` (new)
- `wiki/concepts/llm-wiki-pattern.md` (new)
- `wiki/concepts/retrieval-augmented-generation.md` (new)
- `wiki/concepts/obsidian.md` (new)
- `wiki/entities/andrej-karpathy.md` (new)
- `wiki/entities/vannevar-bush.md` (new)
- `index.md` (updated)
