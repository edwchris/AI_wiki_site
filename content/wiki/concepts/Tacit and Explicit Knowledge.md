---
title: "Tacit and Explicit Knowledge"
aliases: ["Tacit and Explicit Knowledge"]
type: concept
tags: [knowledge-management, tacit-knowledge, explicit-knowledge, nonaka, seci-model, epistemology, ai-limits]
created: 2026-06-27
updated: 2026-06-27
sources: [1994-nonaka-organizational-knowledge-creation]
---

Epistemological distinction between knowledge that can be articulated and transmitted formally (explicit) versus knowledge embedded in practice, judgment, and embodied experience (tacit). Central to understanding both the capabilities and limits of AI.

## Definitions
- **Tacit knowledge**: personal, context-specific, hard to formalize — "we know more than we can tell" (Polanyi). Examples: expert intuition, manual skill, aesthetic judgment, situational awareness, clinical gestalt
- **Explicit knowledge**: codifiable, transmissible in language, symbols, or numbers. Examples: textbooks, protocols, databases, decision rules

## Nonaka's SECI Model
Four modes of knowledge conversion, described in [[Dynamic Theory of Organizational Knowledge Creation — Nonaka 1994]]:

| Mode | Direction | Process |
|------|-----------|---------|
| **Socialization** | T → T | Sharing tacit knowledge through shared experience (apprenticeship, observation) |
| **Externalization** | T → E | Articulating tacit knowledge as explicit concepts (protocols, case studies, metaphors) |
| **Combination** | E → E | Recombining explicit knowledge (databases, synthesis, analysis) |
| **Internalization** | E → T | Making explicit knowledge tacit through practice (learning by doing → competence) |

## AI's Position in the SECI Model

| SECI Mode | AI Capability | Notes |
|-----------|--------------|-------|
| Combination (E→E) | **Strong** | AI excels at pattern-matching over explicit data |
| Externalization (narrow) | **Partial** | AI can learn to detect specific patterns, but cannot fully articulate its own reasoning |
| Socialization (T→T) | **Absent** | AI cannot share experience the way humans do |
| Internalization (E→T) | **Absent** | AI does not develop tacit competence through embodied practice |

## The Ground Truth Gap
Training labels are an **Externalization** of expert tacit judgment — a conversion that is inherently lossy. The know-how that surrounds the label (clinical context, uncertainty, competing interpretations) is stripped away. This is the structural root of the [[AI Ground Truth]] problem identified in [[Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021]].

## Deliberate Practice as Internalization
[[Deliberate Practice]] is a structured Internalization cycle: explicit feedback from a supervisor is absorbed, through effortful repetition, into tacit competence. AI automation that removes deliberate practice opportunities disrupts this cycle → see [[AI in Sonography]] deskilling concern.

## Implications for AI Design
- AI can process explicit records but will systematically miss the tacit dimensions of expert reasoning
- High-stakes domains (clinical medicine, law, strategic judgment) have large tacit components — the gap between AI benchmark performance and real-world performance is larger in these domains
- Human oversight remains necessary not just for accountability but because humans supply tacit judgment AI cannot encode

## Cross-references
- [[AI Ground Truth]]
- [[Deliberate Practice]]
- [[Human-AI Synergy]]
- [[Dynamic Theory of Organizational Knowledge Creation — Nonaka 1994]]
- [[Ikujiro Nonaka]]
