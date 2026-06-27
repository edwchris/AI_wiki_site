---
title: "Distributed Cognition"
aliases: ["Distributed Cognition"]
type: concept
tags: [distributed-cognition, cognitive-systems, HCI, sociotechnical, human-factors, artifacts]
created: 2026-06-27
updated: 2026-06-27
sources: [1995-hutchins-cockpit-distributed-cognition, 2000-hollan-hutchins-kirsh-distributed-cognition]
---

# Distributed Cognition

The theoretical framework proposing that cognitive processes extend beyond the individual mind to encompass artifacts, other people, and environmental structures. Developed primarily by Edwin Hutchins and colleagues.

---

## Core Claim

Cognition is not confined to skulls. The relevant unit of analysis for understanding how people think and act in complex environments is the **functional system** — the ensemble of people, tools, representations, and environmental affordances through which a cognitive task is accomplished.

---

## Three Modes of Distribution

| Mode | Description | Clinical example |
|------|-------------|-----------------|
| **Across people** | Tasks and knowledge distributed across team members | Radiologist + technician + reporting system |
| **Across artifacts** | Representations stored and transformed in tools | PACS + prior reports + AI output |
| **Across time** | Past cognitive work encoded in structures that persist | Protocols, checklists, training labels |

---

## Key Mechanism: Propagation of Representations

Cognition proceeds by transforming information from one representational form to another. Each transformation is a step in the cognitive process:

1. Image data → AI feature extraction → probability score → display
2. Display → radiologist interpretation → report → clinical action

Breakdowns occur at **transformation boundaries** — where information changes form and fidelity may be lost or distorted.

---

## AI as Cognitive Artifact

When AI enters a clinical workflow, it becomes a node in the distributed cognitive system:
- It receives representations (images, data)
- Transforms them (classification, measurement)
- Outputs new representations (flags, scores, annotations)

A DC analysis asks: does the AI's output improve or degrade the quality of representation available to subsequent cognitive steps? What happens when it fails silently?

---

## Implications for Evaluation

Evaluating AI only on benchmark accuracy ignores its role in the distributed system. A DC-aware evaluation asks:
- Does AI output integrate well with clinician mental models?
- Are AI failures visible or silent?
- Does AI change the division of cognitive labour in harmful ways?

See [[Human-Centered AI Evaluation]] for the applied evaluation framework.

---

## Related Pages
- [[Edwin Hutchins]] — primary theorist of distributed cognition
- [[How a Cockpit Remembers Its Speeds — Hutchins 1995]]
- [[Distributed Cognition — Hollan et al. 2000]]
- [[Situation Awareness]]
- [[Tacit and Explicit Knowledge]]
- [[Human-Centered AI Evaluation]]
- [[AI Ground Truth]]
