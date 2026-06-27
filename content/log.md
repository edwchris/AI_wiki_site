# Wiki Log

Append-only chronological record. Each entry starts with `## [YYYY-MM-DD] operation | Title`.

Parse last 5 entries: `grep "^## \[" log.md | tail -5`

---

## [2026-06-27] project | Projects layer created

Added `projects/` folder and four project index pages:
- [[AI in Sonography Research]] — primary research programme
- [[AI in Ultrasound Assessment]] — education research strand
- [[Professorship Portfolio]] — career/promotion connector
- [[US Physics Teaching]] — teaching materials project

Updated CLAUDE.md: added Projects Layer section documenting conventions and LLM operations.
Updated index.md: added Projects section.

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

## [2026-06-27] ingest | Human-AI Interaction in Radiology — Kocak and Cuocolo 2026

Source: `2026.263780.pdf` — identified by user as Diagnostic and Interventional Radiology 2026, DOI 10.4274/dir.2026.263780
Pages created:
- `wiki/sources/Human-AI Interaction in Radiology — Kocak and Cuocolo 2026.md` (new)
- `index.md` (updated — source row added; unprocessed files table now empty — all raw/ files resolved)

## [2026-06-27] ingest | Computer Technology and Clinical Work — Wears and Berg 2005

Source: `jed50009.pdf` — identified by user as JAMA 2005 293:1261-1263
Pages created:
- `wiki/sources/Computer Technology and Clinical Work — Wears and Berg 2005.md` (new)
- `index.md` (updated — added source row; cleaned up unprocessed files table; moved jed50009 to duplicates/resolved list)

## [2026-06-27] ingest | Three identified papers from raw/

Sources: user-identified from previously unknown files
- `PIIS0894731724003201.pdf` → [[Learning Curve for Left Atrial Strain Analysis — Edwards et al. 2024]] (JASE 37:1014-1016; Christopher Edwards co-author)
- `1-s2.0-S1939865420301612.pdf` → [[Caring Relationship Between Sonographer and Patient — Van Der Westhuizen et al. 2020]] (JMIRS 51:S53-S58; qualitative study, SA)
- `DL against health care professionals _Lin.pdf` → confirmed duplicate of [[DL vs Clinicians Systematic Review — Liu et al. 2019]] (already ingested)

index.md updated: 2 new source rows added; 1 file moved to duplicates list

## [2026-06-27] ingest | AI in Medical Ultrasonography — Kim 2021

Source: `Kim - 2021 - Artificial intelligence in medica.pdf` (= `usg-21031.pdf` — confirmed duplicate; DOI suffix 10.14366/usg.21031 matches filename)
Identified by: user confirmed citation; content fetched from e-ultrasonography.org
Pages created:
- `wiki/sources/AI in Medical Ultrasonography — Kim 2021.md` (new)
- `index.md` (updated — added source row; moved both files to duplicates list)

## [2026-06-27] ingest | Four sources — radiography professional development cluster

Sources: user-provided citations matched to new files in raw/
- `PIIS1078817426000404 (1).pdf` → [[Radiographer Research Engagement — Stewart-Lord et al. 2026]] (Radiography 32:103364)
- `PIIS1078817425000768.pdf` → [[Leadership Development in Radiography — Mills et al. 2025]] (Radiography 31:102935)
- `1-s2.0-S1939865423000504 (1).pdf` → [[Radiation Therapy Research After Graduation — Middleton and Bolderston 2023]] (JMIRS 54:328-334)
- `s41073-018-0051-5.pdf` → [[Changing Forms and Expectations of Peer Review — Horbach and Halffman 2018]] (Res Integr Peer Rev 3:8)

Thematic cluster: radiography research engagement, professional development, leadership, peer review.
Note: ScienceDirect blocked; Middleton 2023 and Stewart-Lord 2026 content based on limited web summaries. Update pages when full text accessible.

New unidentified file flagged:
- `J of Medical Radiation Sci - 2017 - Ward - Achieving success in clinically based research  the importance of mentoring.pdf` — Ward 2017, JMIRS; likely fits this cluster

index.md updated: 4 new source rows; 1 new unprocessed file added.

## [2026-06-27] analysis | Wiki–paper alignment audit — "When AI joins the task" framework draft

Source: draft manuscript provided by user (not in raw/)
Analysis performed across all 43 source pages and 26 concept pages.
Pages created:
- `wiki/analyses/AI in Real-Time Procedural Imaging — Framework Paper Analysis 2026-06-27.md` (new)
- `index.md` (updated — Analyses table now populated)

Key findings:
- Framework well-grounded in wiki human factors literature; "verification load" is genuine conceptual contribution
- Central tension: verification load as obligation vs. automation bias as demonstrated non-performance of that obligation
- Calibration bootstrapping problem identified (not in paper or wiki previously): AI-from-day-one training may preclude the independent baseline calibration requires
- Lebovitz 2021 (know-what vs. know-how) not cited in paper despite directly confirming its tacit/explicit redistribution claim
- Relational patient encounter identified as structural residual of AI delegation — undertheorised in paper
- Vaccaro 2024 negative synergy finding more corrosive to paper's collaborative vision than paper acknowledges
- Three conceptual development priorities: disaggregate verification load, substantiate task-centric vs. existing frameworks, qualify sonography uniqueness claim

## [2026-06-27] concept | Three missing concept pages created

Pages created (flagged as data gaps in third lint pass):
- `wiki/concepts/NASSS Framework.md` — 7-domain sociotechnical implementation framework; Greenhalgh et al. 2017; applied in JMIR 2026
- `wiki/concepts/POCUS.md` — Point-of-care ultrasound; professional boundary tensions; AI as enabler and deskilling risk
- `wiki/concepts/MAIRS-MS.md` — Medical AI Readiness Scale for Medical Students; 4 domains; key finding from Edwards et al. 2026

index.md updated with 3 new concept rows.

## [2026-06-27] lint | Third lint pass

**Bug fixed:**
- `wiki/concepts/Ironies of Automation.md` line 11: stray "what " before H1 heading removed (Obsidian linter artefact)

**Orphans resolved (12 pages had no inbound wiki links — all fixed):**
- `Caring Relationship Between Sonographer and Patient — Van Der Westhuizen et al. 2020` → linked from `Sonographer Professional Role.md`
- `Computer Technology and Clinical Work — Wears and Berg 2005` → linked from `AI Implementation in Radiology.md`
- `Human-AI Interaction in Radiology — Kocak and Cuocolo 2026` → linked from `AI Implementation in Radiology.md` and `Human-AI Synergy.md`
- `Implementing AI Decision Support in Radiology — JMIR 2026` → linked from `AI Implementation in Radiology.md`
- `Learning Curve for Left Atrial Strain Analysis — Edwards et al. 2024` → linked from `Christopher Edwards.md`
- `AI in Medical Ultrasonography — Kim 2021` → linked from `AI in Sonography.md`
- `Survey of Deep Learning in Ultrasound — Akkus et al. 2019` → linked from `AI in Sonography.md`
- `AI in Obstetric Ultrasound — Drukker et al. 2020` → linked from `AI in Sonography.md`
- `Sonographer Interaction with AI — Day et al. 2023` → linked from `AI in Sonography.md`
- `Application and Progress of AI in Fetal Ultrasound — Review 2023` → linked from `AI in Sonography.md`
- `Can AI Reduce Echocardiography Scan Time — Hollitt et al. 2025` → linked from `AI in Sonography.md`
- `AI-Enhanced Cardiac US Training — Karni et al. 2025` → linked from `AI Education in Medical Imaging.md` and `Deliberate Practice.md`
- `Topol Review — Health Education England 2019` → linked from `AI Education in Medical Imaging.md`
- `AI in Medicine — Buch et al. 2018` → linked from `AI in Sonography.md`

**Concept pages enriched with new cross-references:**
- `AI in Sonography.md` — added Key Sources section with 10 ultrasound source pages
- `AI Implementation in Radiology.md` — added Wears & Berg 2005, JMIR 2026, Kocak 2026 to Key Resources
- `AI Education in Medical Imaging.md` — added Topol Review and Karni 2025
- `Human-AI Synergy.md` — added Kocak 2026
- `Deliberate Practice.md` — added Karni 2025 with short-term vs. long-term skill tension note
- `Automation Bias.md` — added Kocak 2026's 80%→20% trainee accuracy finding

**Contradiction flagged:**
- `Human-AI Interaction in Radiology — Kocak and Cuocolo 2026.md` — added `[!warning]` noting tension between "diagnostic complementarity" claim and Vaccaro 2024 negative synergy data (g = −0.23)

**Floating citation (from lint 2):** still unresolved:
- `Donahue et al. 2022` in `Human-AI Synergy.md` — no source page; conditions for synergy attribution

**Stubs still needed (no change from lint 2):**
- `[[Lisanne Bainbridge]]`, `[[Jens Rasmussen]]`, `[[Mica Endsley]]`, `[[Edwin Hutchins]]`, `[[Raja Parasuraman]]`, `[[James D. Lee]]` — key human factors theorists

**Data gaps flagged (no web search done):**
> [!question] NASSS Framework — mentioned in JMIR 2026 source page; no concept page; worth creating if NASSS becomes referenced in more sources
> [!question] POCUS — referenced in 5+ pages but no concept page; candidate for creation
> [!question] MAIRS-MS tool — described in Edwards 2026 source page; no separate concept page

## [2026-06-27] ingest | Large batch — 25 sources, 7 concepts from raw/

Sources processed:
**Human factors theory:**
- `1-s2.0-0005109883900468-main.pdf` → [[Ironies of Automation — Bainbridge 1983]]
- `roniesofutomationtillnresolvedfterllheseears_4.pdf` → [[Ironies of Automation — Strauch 2017]]
- `Skills rules and knowledge - Rasmussen seg (1).pdf` → [[Skills Rules and Knowledge — Rasmussen 1983]]
- `Endsley_MR_Toward_a_Theory_of_Situation_Awaren.pdf` → [[Toward a Theory of Situation Awareness — Endsley 1995]]
- `A_model_for_types_and_levels_of_human_interact.pdf` → [[A Model for Types and Levels of Human Interaction with Automation — Parasuraman et al. 2000]]
- `lee-see-2004-trust-in-automation-designing-for.pdf` → [[Trust in Automation — Lee and See 2004]]
- `ParasuramanManzeyHF2010.pdf` → [[Complacency and Bias in Human Use of Automation — Parasuraman and Manzey 2010]]
- `hoff-bashir-2014-trust-in-automation.pdf` → [[Trust in Automation — Hoff and Bashir 2014]]
- `Cognitive Science - July 1995 - Hutchins - How.pdf` → [[How a Cockpit Remembers Its Speeds — Hutchins 1995]]
- `Hollan Distributed cognition.pdf` → [[Distributed Cognition — Hollan et al. 2000]]

**Medical AI / imaging:**
- `s41591-021-01614-0.pdf` → [[AI in Health and Medicine — Rajpurkar et al. 2022]]
- `Liu et al. - 2019 - A comparison of deep learn.pdf` → [[DL vs Clinicians Systematic Review — Liu et al. 2019]]
- `Drukker, Noble, Papageorghiou - 2020 - Introdu.pdf` → [[AI in Obstetric Ultrasound — Drukker et al. 2020]]
- `Akkus et al. - 2019 - A Survey of Deep-Learnin.pdf` → [[Survey of Deep Learning in Ultrasound — Akkus et al. 2019]]
- `Day et al. - 2023 - Sonographer interaction wi.pdf` → [[Sonographer Interaction with AI — Day et al. 2023]]
- `Dratsch-2023-Automation-bias-in-mammography-th.pdf` → [[Automation Bias in Mammography — Dratsch et al. 2023]]
- `HEE-Topol-Review-2019.pdf` → [[Topol Review — Health Education England 2019]]
- `Buch, Ahmed, Maruthappu - 2018 - Artificial in.pdf` → [[AI in Medicine — Buch et al. 2018]]
- `jmir-2026-1-e80342.pdf` → [[Implementing AI Decision Support in Radiology — JMIR 2026]]
- `jcm-12-03298.pdf` → [[Application and Progress of AI in Fetal Ultrasound — Review 2023]]
- `s44156-025-00077-0.pdf` → [[Can AI Reduce Echocardiography Scan Time — Hollitt et al. 2025]]
- `s12909-025-06905-5.pdf` → [[AI-Enhanced Cardiac US Training — Karni et al. 2025]]

**Sonography and professional role:**
- `Finberg-2004-Whither (Wither_) the Ultrasound.pdf` → [[Whither the Ultrasound Specialist — Finberg 2004]]
- `Thomas, O'Loughlin, Clarke - 2017 - The 21st c.pdf` → [[21st Century Sonographer — Thomas et al. 2017]]
- `Nicholls, Sweet, Hyett - 2014 - Psychomotor Sk.pdf` → [[Psychomotor Skills in Ultrasound — Nicholls et al. 2014]]

Skipped (duplicates):
- `s41562-024-02024-1.pdf` = Vaccaro et al. 2024 (already ingested)
- `brady-et-al-2024-developing-purchasing-impleme.pdf` = multisociety statement (already ingested)
- `dratsch-et-al-2023-automation-bias-in-mammogra.pdf` = same as Dratsch 2023 above
- `Nicholls, Sweet, Hyett - 2014 - Psychomotor S1.pdf` and `J of Ultrasound Medicine - 2014 - Nicholls - P.pdf` = same paper

Still unidentified (8 files — see index.md for details):
- `Kim - 2021 - Artificial intelligence in medica.pdf`
- `PIIS0894731724003201.pdf`
- `1-s2.0-S1939865420301612.pdf`
- `jed50009.pdf`
- `usg-21031.pdf`
- `DL against health care professionals _Lin.pdf`
- `24561742_21180655980004001.pdf`
- `2026.263780.pdf`

Concept pages created: Ironies of Automation, Situation Awareness, Trust in Automation, Distributed Cognition, Levels of Automation, Skills Rules and Knowledge, Sonographer Professional Role

Note: PDFs not readable on this system; content sourced from PMC, publisher pages, and training knowledge for the well-established theory papers.

## [2026-06-27] ingest | Automation Bias — Goddard et al. 2012

Source: `19-1-121.pdf` — identified by user as JAMIA 2012;19:121–127
Pages created:
- `wiki/sources/Automation Bias Systematic Review — Goddard et al. 2012.md` (new)
- `wiki/concepts/Automation Bias.md` (new)
- `index.md` (updated)

## [2026-06-27] ingest | Two QUT/Edwards papers — moral responsibility & AI preparedness

Sources processed:
- `EBSCO-FullText-04_09_2026.pdf` → [[Measuring AI Preparedness in Health Professions Education — Edwards et al. 2026]]
  - Identified via: published Radiography 32(5) 2026; received Feb 2026; EBSCO download date 9 Apr 2026 consistent with early online availability; Edwards is first author
  - PDF not directly readable; content sourced from Radiography Online abstract + web search
- `19-1-121.pdf` → **still unidentified** — could not be matched to any paper via web search; no pdftoppm available. Please open this file manually to identify.

Also ingested (found during identification search, highly relevant, not yet in raw/ but in QUT ePrints):
- [[The Role of Patient Outcomes in Moral Responsibility — Edwards et al. 2025]] (Radiography 31(3), 2025, DOI: 10.1016/j.radi.2025.102948) — content sourced from web

Pages created:
- `wiki/sources/Measuring AI Preparedness in Health Professions Education — Edwards et al. 2026.md` (new)
- `wiki/sources/The Role of Patient Outcomes in Moral Responsibility — Edwards et al. 2025.md` (new)
- `wiki/concepts/AI Education in Medical Imaging.md` (new)

Pages updated:
- `wiki/entities/Christopher Edwards.md` — added two new publication entries and updated sources frontmatter
- `index.md` — added 2 source rows, 1 concept row; updated unprocessed files section

## [2026-06-27] ingest | Batch ingest — 10 sources from raw/

Sources processed:
- `Nagendran et al. - 2020 - Artificial intellige.pdf` → [[AI vs. Clinicians — Nagendran et al. 2020]]
- `Edwards, Chamunyonga, Clarke - 2018 - The role.pdf` → [[Deliberate Practice in Sonography — Edwards et al. 2018]]
- `Geis et al. - 2019 - Ethics of artificial inte.pdf` + `s13244-019-0785-8.pdf` (same paper, two copies) → [[Ethics of AI in Radiology — Geis et al. 2019]]
- `Edwards et al. - 2022 - The application of art.pdf` → [[AI in the Sonography Profession — Edwards et al. 2022]]
- `Day et al. - 2025 - AI to Assist in the Fetal.pdf` → [[PROMETHEUS RCT — Day et al. 2025]]
- `10.1148_radiol.250477.pdf` → [[Role Separation in AI-Human Radiology — Rajpurkar & Topol 2025]]
- `Nonaka_1994_A dynamic thoery of organizational.pdf` → [[Dynamic Theory of Organizational Knowledge Creation — Nonaka 1994]]
- `3313831.3376718.pdf` → [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]]
- `s13244-023-01548-w.pdf` → [[Diversity of Ultrasound Practice — Sidhu et al. 2023]]
- `s13244-023-01541-3.pdf` → [[Developing and Implementing AI Tools in Radiology — Multisociety 2023]]

Skipped (not research sources):
- `wiki-update-workflow.md` — personal workflow reference document
- `19-1-121.pdf` — unidentifiable from filename; PDF not readable without pdftoppm
- `EBSCO-FullText-04_09_2026.pdf` — unidentifiable from filename; PDF not readable without pdftoppm

Pages created:
- 10 source pages in `wiki/sources/`
- 8 concept pages: Deep Learning in Medical Imaging, Deliberate Practice, AI Ethics in Radiology, AI in Sonography, AI-Human Role Separation, Tacit and Explicit Knowledge, Human-Centered AI Evaluation, AI Implementation in Radiology
- 8 entity pages: Christopher Edwards, Crispen Chamunyonga, Ikujiro Nonaka, Pranav Rajpurkar, Eric Topol, Emma Beede, Thomas Day, J. Raymond Geis
- Updated: `wiki/concepts/AI Ground Truth.md`, `wiki/concepts/Human-AI Synergy.md`, `index.md`

Note: PDFs were not directly readable (no pdftoppm on this system); content sourced from web (PubMed, publisher pages, Semantic Scholar).

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

## [2026-06-27] ingest | Images + 2 new sources — Rashomon set commentary, SERVQUAL, SA model diagram

**Images embedded:**
- `raw/assets/Endsley-SA-model.jpg` → embedded in `Situation Awareness.md` (concept) and `Toward a Theory of Situation Awareness — Endsley 1995.md` (source)
- `raw/assets/RsetDefinition-31757979670372.png` → embedded in `Explainable AI.md` (concept) and `Stop Explaining Black Box ML — Rudin 2019.md` (source)
- `raw/assets/12916_2019_1463_Fig1_HTML.png` — already embedded in NASSS pages (previous session)

**New source pages:**
- `raw/User-Guided Interpretable Models Rashomon Effect...` → [[User-Guided Interpretable Models — Liu and Rudin 2025]] (HDSR 2025;7(3); Liu & Rudin; Rashomon set paradigm; interaction bottleneck)

**New concept pages:**
- `raw/SERVQUAL.md` (Wikipedia clip) → [[SERVQUAL]] concept page (service quality tool; 5 RATER dimensions; gaps model; note: A. Parasuraman ≠ Raja Parasuraman)

index.md updated: 1 new source row, 1 new concept row.

## [2026-06-27] ingest | 10 missing papers + bonus source — human factors, clinical AI ethics, bias, ML critique

Sources processed (all .md exports from raw/ unless noted):

**NASSS / implementation science:**
- `Beyond Adoption A New Framework...` → [[Beyond Adoption — NASSS Framework — Greenhalgh et al. 2017]]

**Clinical AI — overview and translation:**
- `High-performance medicine the convergence...` → [[High-Performance Medicine — Topol 2019]]
- `Key challenges for delivering clinical impact...` → [[Key Challenges for Clinical AI — Kelly et al. 2019]] (note: all authors Google LLC)

**ML critique and interpretability:**
- `Stop explaining black box machine learning...` → [[Stop Explaining Black Box ML — Rudin 2019]]

**Algorithmic bias:**
- `Dissecting racial bias in an algorithm...` → [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]]

**Unintended consequences and ethics:**
- `Unintended Consequences of Machine Learning in Medicine.md` → [[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]]
- `Implementing Machine Learning in Health Care...` → [[Implementing ML in Healthcare Ethical Challenges — Char et al. 2018]]

**Expertise and deliberate practice:**
- `Deliberate Practice and the Acquisition...` → [[Deliberate Practice in Medicine — Ericsson 2004]]

**Human factors (PDFs — source pages written from domain knowledge):**
- `raw/parasuraman.pdf` → [[Humans and Automation — Parasuraman and Riley 1997]]
- `raw/Dietvorst-Simmons-Massey-2014.pdf` → [[Algorithm Aversion — Dietvorst et al. 2015]]

**New source (not in original 10 — found in raw/ during ingest):**
- `Artificial intelligence in radiography education...` → [[AI in Radiography Education — Meertens et al. 2026]]
  - Contains citation to Edwards as co-author on Crotty et al. 2024 (ref 12)

Total: 11 source pages created.

Verification: 3 previously failed Write calls (Stewart-Lord 2026, Mills 2025, Middleton & Bolderston 2023) confirmed to exist on disk — all OK.

index.md updated: 11 new source rows added.

Concept pages needed (not yet created — flagged for next session):
- `[[Algorithm Aversion]]` — referenced from Dietvorst source and Trust in Automation concept
- `[[Algorithmic Fairness and Bias]]` — referenced from Obermeyer source
- `[[Explainable AI]]` — referenced from Rudin source
- `[[AI Chasm]]` — referenced from Topol and Kelly sources

Entity pages still needed (from prior lint):
- `[[Raja Parasuraman]]`, `[[Lisanne Bainbridge]]`, `[[Jens Rasmussen]]`, `[[Mica Endsley]]`, `[[Edwin Hutchins]]`, `[[James D. Lee]]`

Additional uninspected raw PDFs noted in raw/ folder (candidate for future ingest sessions):
- `PIIS1078817426000404 (1).pdf` through various others — several appear relevant to sonography/radiology

## [2026-06-27] ingest + analysis | Sonographer competency framework and EPAs — Edwards et al. 2022 & 2023

Sources processed (both .md web clips from raw/):
- `Australian sonographer competency—A new framework.md` → [[Australian Sonographer Competency Framework — Edwards et al. 2022]] (*Sonography*; DOI 10.1002/sono.12309)
- `Entrustable professional activities of graduate accredited General Medical Sonographers in Australia.md` → [[Entrustable Professional Activities in Sonography — Edwards et al. 2023]] (*JMRS*; DOI 10.1002/jmrs.676)

Two PDFs arrived alongside; unreadable without pdftoppm:
- `Professional Competency Framework for Sonographers.pdf` — likely the full ASAR framework document
- `Sonographer Training pathway.pdf` — unknown; flagged in index.md

Pages created:
- `wiki/sources/Australian Sonographer Competency Framework — Edwards et al. 2022.md` (new)
- `wiki/sources/Entrustable Professional Activities in Sonography — Edwards et al. 2023.md` (new)
- `wiki/concepts/Sonographer Competency.md` (new) — SRK mapping of competency matrix; EPA-SRK integration; AI gaps; relational residual

Pages updated:
- `wiki/concepts/Sonographer Professional Role.md` — added competency framework unit map and new sources
- `wiki/analyses/AI in Real-Time Procedural Imaging — Framework Paper Analysis 2026-06-27.md` — two new sections added:
  - "The Competency Architecture as Substrate" — maps 5 units onto AI disruption; resolves open question 4 (relational residual confirmed)
  - "The EPA-SRK Gap" — emergency work consensus as K-level policy; calibration bootstrapping sharpened; atomisation critique; 5 open questions updated
- `index.md` — 2 new source rows, 1 new concept row, PDF note section added

## [2026-06-27] lint | Full lint pass — fourth pass

**Broken links fixed (5):**
- `AI in Obstetric Ultrasound — Drukker et al. 2020`: `[[Day et al. - 2023 - Sonographer interaction with AI]]` → `[[Sonographer Interaction with AI — Day et al. 2023]]`
- `Humans and Automation — Parasuraman and Riley 1997`: `[[Situational Awareness]]` → `[[Situation Awareness]]`
- `Radiographer Research Engagement — Stewart-Lord et al. 2026`: broken title link → `[[Radiation Therapy Research After Graduation — Middleton and Bolderston 2023]]`
- `Obsidian`: `[[wikilinks]]` escaped to prevent phantom link; `[[Dataview]]` and `[[Marp]]` now proper wikilinks to new concept pages
- `Sonographer Professional Role`: Unit 5 over-claim corrected — "all four elements reshaped by AI" replaced with nuanced 5.2/5.3/5.4 breakdown matching session correction

**Orphans resolved (11 pages):**
- `Berkeley Dietvorst` → linked from `Algorithm Aversion.md`
- `Edwin Hutchins` → linked from `Distributed Cognition.md`
- `K. Anders Ericsson` → linked from `Deliberate Practice.md`
- `Trisha Greenhalgh` → linked from `NASSS Framework.md`
- `Ziad Obermeyer` → linked from `Algorithmic Fairness and Bias.md`
- `User-Guided Interpretable Models — Liu and Rudin 2025` → linked from `Cynthia Rudin.md`
- `AI in Health and Medicine — Rajpurkar et al. 2022` → linked from `Pranav Rajpurkar.md`
- `Radiation Therapy Research After Graduation — Middleton and Bolderston 2023` → broken link in Stewart-Lord page fixed (above)
- `POCUS` → linked from `AI in Sonography.md` and `Sonographer Professional Role.md`
- `SERVQUAL` → linked from `Human-Centered AI Evaluation.md`
- `Leadership Development in Radiography — Mills et al. 2025` → linked from `Sonographer Professional Role.md`
- `Changing Forms and Expectations of Peer Review — Horbach and Halffman 2018` → linked from `DL vs Clinicians Systematic Review — Liu et al. 2019.md`

**New pages created:**
- `wiki/concepts/Verification Load.md` — continuous per-output cognitive burden of AI monitoring; complements Automation Bias
- `wiki/concepts/Human Augmentation.md` — AI as capability-extender; conditions for augmentation benefit vs. failure
- `wiki/concepts/Assessment Design.md` — structural vs. discursive change; TEXA principles; linked from Dawson 2025 source
- `wiki/concepts/Dataview.md` — Obsidian database plugin stub
- `wiki/concepts/Marp.md` — Obsidian presentation plugin stub
- `wiki/concepts/qmd.md` — Quarto Markdown publishing format stub
- `wiki/entities/Jessie Childs.md` — co-author on both sonography competency papers
- `wiki/entities/OpenAI.md`, `ChatGPT.md`, `Tesla.md`, `Eureka Labs.md`, `micrograd.md`, `nanoGPT.md` — Karpathy affiliation stubs
- `wiki/entities/NotebookLM.md`, `Perplexity.md`, `LangChain.md`, `LlamaIndex.md` — RAG ecosystem stubs
- `wiki/sources/AI in Medical Imaging Education — Crotty et al. 2024.md` — stub; citation TBC; referenced in Meertens 2026

**Entity updated:**
- `Christopher Edwards.md` — added two new source publications (competency framework + EPA paper); added `[[Jessie Childs]]` cross-reference

**Stub remaining:**
- `[[Abdullah Almaatouq]]` — MIT co-author of Vaccaro et al. 2024 (entity page not yet created)

## [2026-06-27] ingest | Feedback literacy and assessment design — Dawson 2023 & 2025

Sources processed (both YouTube transcript .md exports from raw/):
- `Feedback and feedback literacy.md` → [[Feedback and Feedback Literacy — Dawson 2023]] (workshop, KCL/UCL, July 2023)
- `Keynote 1 - Professor Phillip Dawson - Assessment Design for a Time of AI.md` → [[Assessment Design for a Time of AI — Dawson 2025]] (keynote, ATU DigitalEd, May 2025)

Pages created:
- `wiki/sources/Feedback and Feedback Literacy — Dawson 2023.md` (new)
- `wiki/sources/Assessment Design for a Time of AI — Dawson 2025.md` (new)
- `wiki/concepts/Feedback Literacy.md` (new) — process view of feedback; Carless & Boud 4-component model; teacher literacy; meso-level design as key leverage
- `wiki/concepts/Evaluative Judgment.md` (new) — judging quality of own work, others' work, or AI output; develops through enactment; central AI-age competency
- `wiki/entities/Phillip Dawson.md` (new) — Deakin University / CRADLE; feedback literacy + AI assessment

index.md updated: 2 new source rows, 2 new concept rows, 1 new entity row.
