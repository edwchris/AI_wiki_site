---
title: "Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021"
aliases: ["Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021"]
type: source
tags: [ground-truth, knowledge-work, healthcare-ai, machine-learning, evaluation, know-what, know-how]
created: 2026-06-27
updated: 2026-06-27
sources: [2021-lebovitz-levina-lifshitz-assaf-ai-ground-truth]
---

# Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021

**Full title**: "Is AI Ground Truth Really True? The Dangers of Training and Evaluating AI Tools Based on Experts' Know-What"
**Authors**: [[Sarah Lebovitz]] (UVA McIntire), [[Natalia Levina]] (NYU Stern), [[Hila Lifshitz-Assaf]] (Warwick Business School)
**Venue**: MIS Quarterly, Vol. 45, Issue 3, pp. 1501–1526, September 2021
**DOI**: 10.25300/MISQ/2021/16564
**Special issue**: Managing AI

---

## Research Question

How should organizations evaluate AI tool performance in knowledge work contexts where measuring quality is inherently difficult?

---

## Methodology

Field study at a major U.S. hospital. Observed managers evaluating five machine-learning–based AI tools across clinical contexts. Combined technical metrics review with observation of practical deployment attempts.

---

## Key Findings

- All five tools reported **high accuracy** on standard ML evaluation metrics using expert-labeled ground truth
- In practice, **none met expectations** — they failed to deliver clinical value despite strong benchmarks
- Root cause: ground truth labels capture experts' *know-what* (explicit, codifiable judgment calls) but not *know-how* (tacit, contextual practices used to navigate uncertainty)
- Experts address diagnostic uncertainty through rich contextual practices invisible in labeled datasets; ML models trained on labels inherit the uncertainty without the coping mechanisms

---

## Core Theoretical Framework

### Know-What vs. Know-How

| Type | Definition | Captured in ground truth? |
|------|-----------|--------------------------|
| **Know-what** | Explicit, factual knowledge — the label assigned to a case | Yes |
| **Know-how** | Tacit, practice-based expertise — how experts handle ambiguity and uncertainty | No |

Ground truth labels represent *know-what* snapshots, but expert performance in context draws heavily on *know-how*. Training on know-what alone creates a model that performs well on benchmark tasks but fails when deployed in the messy, uncertain real world.

### The Ground Truth Problem

> [!important]
> Ground truth labels are not objective facts — they are uncertain expert judgments treated as if they were facts. When the underlying domain has irreducible uncertainty, the labels inherit that uncertainty but strip away the coping practices.

This creates a systematic gap:
1. Experts label cases (know-what only, uncertainty embedded)
2. Model trains on labels, optimizing for accuracy against those labels
3. Model is evaluated against held-out labels — looks good
4. Model is deployed — confronts the same uncertainty without the know-how to manage it
5. Performance collapses

---

## Implications

- **For AI developers**: Ground truth curation must acknowledge domain uncertainty; consider including expert rationale (how they resolved uncertainty), not just the label
- **For organizations evaluating AI**: Standard accuracy metrics are insufficient for knowledge work — demand evidence of performance under real-world uncertainty conditions
- **For researchers**: Study the know-how practices experts use alongside the know-what labels; these are the missing layer in current ML pipelines

---

## Relation to Other Work

- Complements [[When Combinations of Humans and AI Are Useful — Vaccaro et al. 2024]]: both show human–AI gaps are larger than benchmarks suggest; Lebovitz et al. provide a mechanism (know-what/know-how split)
- Grounds the [[Human-AI Synergy]] literature in a knowledge-epistemics explanation for why AI underperforms in professional contexts
- See [[AI Ground Truth]] for the broader concept page

---

## Citation

Lebovitz, S., Levina, N., & Lifshitz-Assaf, H. (2021). Is AI ground truth really true? The dangers of training and evaluating AI tools based on experts' know-what. *MIS Quarterly*, *45*(3), 1501–1526.
