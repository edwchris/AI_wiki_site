---
title: "AI Ground Truth"
aliases: ["AI Ground Truth"]
type: concept
tags: [ground-truth, machine-learning, evaluation, data-labeling, know-what, know-how, knowledge-work]
created: 2026-06-27
updated: 2026-06-27
sources: [2021-lebovitz-levina-lifshitz-assaf-ai-ground-truth]
---

# AI Ground Truth

**Ground truth** in machine learning refers to the labeled data used to train and evaluate models — the authoritative answer a model is supposed to learn to predict.

---

## The Standard Assumption

Ground truth labels are typically treated as objective facts: a radiologist labels an X-ray as "tumor" or "no tumor," and the model learns to replicate that judgment. Model quality is measured by how well it matches labels on held-out test sets.

---

## The Know-What Problem

[[Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021]] challenges this assumption. Ground truth labels capture only experts' *know-what* — the explicit, codifiable judgment — not their *know-how* — the tacit practices used to navigate uncertainty.

### Know-What vs. Know-How

| | Know-What | Know-How |
|---|-----------|----------|
| **Nature** | Explicit, codifiable | Tacit, practice-based |
| **Example** | "This scan is positive" | How the radiologist resolved ambiguity given patient history, scan quality, prior probability |
| **In ground truth?** | Yes — it's the label | No — invisible in the dataset |
| **Under uncertainty** | Collapses to a forced binary | Rich contextual practices apply |

> [!important]
> When experts operate under uncertainty, they don't just guess — they draw on contextual, experiential know-how to manage that uncertainty. ML models trained on labels inherit the uncertainty but not the coping mechanisms.

---

## Why This Matters for Evaluation

The standard ML evaluation pipeline:
1. Experts label data (know-what only)
2. Model trains on labels
3. Model evaluated against held-out labels → **looks good**
4. Model deployed in real context → **performance collapses**

High benchmark accuracy is not evidence of real-world utility in knowledge work domains. The held-out test set has the same epistemic structure as the training set — both lack know-how. Only deployment surfaces the gap.

---

## When Is This Most Dangerous?

The problem is most acute when:
- The domain has **irreducible uncertainty** (medicine, law, finance)
- Experts exercise significant **judgment** in labeling (not mechanical annotation)
- The model is evaluated only on **benchmark accuracy** before deployment
- Deployment exposes the model to **the same uncertainty** the labelers faced

It is less severe when:
- Ground truth is genuinely objective (e.g., chess moves, math problems)
- Annotation tasks are unambiguous and well-specified
- Domain experts are highly calibrated and consistent

---

## Implications for Practice

- **Curation**: Capture expert rationale alongside labels, not just the label itself
- **Evaluation**: Supplement accuracy metrics with real-world pilots or uncertainty-aware tests
- **Procurement**: Demand evidence of performance under uncertainty, not just benchmark scores
- **Research**: Study the know-how practices experts use — these are the missing layer in current ML pipelines

---

## Related Pages

- [[Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021]] — source
- [[Human-AI Synergy]] — related evidence on human–AI performance gaps
- [[Sarah Lebovitz]], [[Natalia Levina]], [[Hila Lifshitz-Assaf]] — authors
