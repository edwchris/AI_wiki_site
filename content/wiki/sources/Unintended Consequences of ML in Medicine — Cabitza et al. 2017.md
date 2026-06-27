---
title: "Unintended Consequences of ML in Medicine — Cabitza et al. 2017"
aliases: ["Unintended Consequences of ML in Medicine — Cabitza et al. 2017"]
type: source
tags: [deskilling, automation-bias, unintended-consequences, clinical-ai, machine-learning, decision-support, context-blindness]
created: 2026-06-27
updated: 2026-06-27
sources: [2017-cabitza-unintended-consequences-ml]
---

# Unintended Consequences of ML in Medicine — Cabitza et al. 2017

**Full citation:** Cabitza F, Rasoini R, Gensini GF. Unintended consequences of machine learning in medicine. *JAMA*. 2017;318(5):517–518.

**DOI:** 10.1001/jama.2017.7797

---

## What it is

A short Viewpoint piece in *JAMA* identifying four categories of unintended consequence that arise from deploying ML in clinical settings. Focused on risks from adoption of ML systems without appropriate critical appraisal. Highly cited as an early warning about clinical AI.

## Four risks

### 1. Deskilling

ML tools that automate tasks previously requiring clinician skill can reduce proficiency over time:

- Computer-aided detection (CAD) for mammography: one study found radiologists' sensitivity **decreased 14%** when using CAD compared to reading without it — they became over-reliant on what the algorithm highlighted and stopped seeking lesions independently
- ECG analysis: when an inaccurate AI annotation was available, physician accuracy dropped from **57% → 48%** — the presence of a wrong AI opinion was worse than having no AI at all

> [!important] The deskilling effect means that AI tools can reduce diagnostic accuracy even when the AI is nominally "assistive." Degraded clinician skill may become permanent if the tool is used extensively during training.

### 2. Focus on text / demise of context

ML trained on structured EHR data learns patterns in the documented record, not in the physical patient. This creates category errors when the recorded variable is a *proxy* for the actual phenomenon:

**Canonical example: Asthma and pneumonia**
- An ML model trained to predict pneumonia mortality found that asthma appeared *protective* — asthma patients had lower mortality risk after pneumonia diagnosis
- This was statistically accurate: asthma patients with pneumonia were directly admitted to ICU and received aggressive early treatment
- The algorithm **correctly** identified the pattern in the data, but the pattern was an artifact of clinical practice, not biology
- If the model had been used to triage patients, it would have recommended lower-risk management for asthmatic patients — potentially fatal

> [!important] This is an "accurately fit confounder" — the model learned a real statistical regularity that would be dangerous to act on. Context (clinical practice variation) was embedded in the data but not accessible to the algorithm.

### 3. Intrinsic uncertainty

Medical observations themselves have inherent uncertainty that gets obscured when encoded as training labels:

- Inter-rater variability in radiology reading is well-documented (even experts disagree 20–30% of the time on subtle findings)
- ML models trained on one radiologist's labels inherit that radiologist's idiosyncrasies as if they were ground truth
- "Gold standard" labels are often a single expert opinion or majority vote — not genuinely verified truth

### 4. Black box opacity

Without understanding why an algorithm makes a decision, clinicians cannot detect when a decision is based on a dangerous confounder (e.g., the asthma example):

- Post-hoc explanations (saliency maps, LIME) may not reflect actual computation
- Opaque models make it impossible to catch context-free reasoning before deployment
- Unlike rule-based systems, ML errors may not be systematic or detectable via audit

## Connections

- [[Automation Bias]] — deskilling is related but distinct: automation bias is error in the moment; deskilling is degradation of the underlying skill over time
- [[Stop Explaining Black Box ML — Rudin 2019]] — Rudin's proposal for interpretable models directly addresses the black box opacity problem raised here
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — cites the asthma example; frames confounder fitting as a key technical challenge
- [[Ironies of Automation]] — Bainbridge predicted: automation reduces skill; reduced skill increases automation dependence
- [[Deliberate Practice in Medicine — Ericsson 2004]] — deliberate practice requires challenge and feedback; AI removing challenge accelerates skill atrophy
- [[AI in Sonography Research]] — directly relevant to concerns about AI in ultrasound assessment

## Significance

Short paper (2 pages) but conceptually rich. The asthma/pneumonia example is one of the most cited in clinical AI literature because it illustrates that an algorithm can be statistically correct and clinically dangerous simultaneously. Directly relevant to any deployment of AI in high-stakes diagnostic settings.
