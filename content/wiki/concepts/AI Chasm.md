---
title: "AI Chasm"
aliases: ["AI Chasm", "Translation Gap"]
type: concept
tags: [ai-chasm, translation-gap, clinical-ai, prospective-validation, real-world-performance, implementation]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-topol-high-performance-medicine, 2019-kelly-clinical-ai-challenges, 2020-nagendran-ai-vs-clinicians]
---

# AI Chasm

The gap between an AI algorithm demonstrating high accuracy on benchmark tasks and that algorithm demonstrably improving patient outcomes in real-world clinical practice. The term was introduced/popularised by Eric Topol ([[High-Performance Medicine — Topol 2019]]) and Pearse Keane.

> [!important] An AUC of 0.99 is worthless if the algorithm is never proven to improve clinical outcomes.

## Why the gap exists

### Study design problems
- Most clinical AI studies are **retrospective**: train on historical data, test on held-out historical data
- Retrospective performance ≠ prospective performance because:
  - Distribution shift: data characteristics change over time
  - Confounder fitting: models learn spurious patterns in historical data that don't generalise
  - No clinical integration: measuring algorithmic output, not patient decision pathway

### Validation gap
From [[AI vs. Clinicians — Nagendran et al. 2020]]:
- 75% of DL studies in medical imaging claim AI ≥ clinician
- Nearly all studies have high methodological risk of bias
- Only 6 of 81 eligible studies (7%) used prospective designs
- No RCTs existed (as of 2020)

From [[Key Challenges for Clinical AI — Kelly et al. 2019]]:
- ~6% of 516 eligible AI imaging studies performed external validation
- No clinical AI algorithm had published a prospective RCT with patient outcomes at time of writing

### Implementation gap
Even technically sound algorithms face implementation barriers:
- Workflow integration challenges
- Alert fatigue (clinicians ignore decision support)
- Trust calibration failure (algorithm aversion or automation bias)
- Organisational and legal barriers
- See [[NASSS Framework]] for the 7-domain framework explaining why technologies fail to scale

## Evidence that the chasm is real

- **Google Health DR detection (Beede et al. 2020)**: Diabetic retinopathy AI with AUC 0.97 failed in 11 Thai clinics — nurses couldn't use system as deployed; 22% images ungradeable in real settings vs. 0% in validation set. See [[Human-Centered Evaluation of AI in Diabetic Retinopathy Clinics — Beede et al. 2020]].
- **IBM Watson for Oncology**: recommended dangerous or incorrect treatment combinations in real hospitals despite strong benchmark performance.
- **Lebovitz et al. 2021**: five "high-accuracy" ML tools failed in clinical practice because they captured know-what but not the know-how clinicians use. See [[Is AI Ground Truth Really True — Lebovitz, Levina & Lifshitz-Assaf 2021]].

## The emerging bridge: prospective trials

[[PROMETHEUS RCT — Day et al. 2025]] represents the kind of study needed to cross the AI chasm:
- Randomised controlled trial
- Real-world clinical setting
- Measuring patient-relevant outcomes (diagnostic performance, scan time, cognitive load)
- Found: 42% time reduction, maintained diagnostic performance, reduced cognitive load
- This is the gold standard; most AI studies don't get here.

## Implications

- AUC/accuracy scores alone are not publishable evidence of clinical benefit
- External prospective validation on independent cohorts is the minimum standard
- RCTs with patient outcome endpoints are the gold standard
- Implementation factors (workflow, training, trust) must be studied alongside technical performance

## Connections

- [[High-Performance Medicine — Topol 2019]] — introduces AI chasm concept
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — key barriers to crossing the chasm
- [[AI vs. Clinicians — Nagendran et al. 2020]] — empirical data on validation gap
- [[Human-Centered AI Evaluation]] — evaluation methodology that addresses implementation, not just accuracy
- [[NASSS Framework]] — why health technologies fail to scale even when technically effective
- [[Deep Learning in Medical Imaging]] — the domain where most chasm evidence originates
- [[PROMETHEUS RCT — Day et al. 2025]] — example of a study that crosses the chasm
