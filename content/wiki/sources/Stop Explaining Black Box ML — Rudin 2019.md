---
title: "Stop Explaining Black Box ML — Rudin 2019"
aliases: ["Stop Explaining Black Box ML — Rudin 2019"]
type: source
tags: [interpretable-ml, explainable-ai, xai, black-box, transparency, high-stakes-decisions, algorithmic-fairness]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-rudin-stop-explaining-black-boxes]
---

# Stop Explaining Black Box ML — Rudin 2019

**Full citation:** Rudin C. Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead. *Nat Mach Intell*. 2019;1:206–215.

**DOI:** 10.1038/s42256-019-0048-x

---

## What it is

A strongly argued Perspective piece by Cynthia Rudin (Duke University) challenging the dominant paradigm in "explainable AI" (XAI). Published in *Nature Machine Intelligence*, 2019. Among the most-cited critiques of post-hoc explainability in high-stakes ML.

## Core thesis

> Stop trying to explain black box models. Build inherently interpretable models instead.

Rudin distinguishes two fundamentally different approaches:
- **Explainable ML** — use a black box, then create a second model to explain the first
- **Interpretable ML** — design the model itself so its decisions are understandable

She argues that XAI/explainable ML methods are fundamentally flawed and potentially dangerous for high-stakes decisions (healthcare, criminal justice, finance).

## Four problems with explainable ML

1. **Explanations are unfaithful** — a post-hoc explanation model cannot have perfect fidelity with the original model; if it did, you wouldn't need the original. Explanations are wrong some fraction of the time, and you can never know when.

2. **Explanations can be misleading** — e.g., an explanation model for a recidivism predictor might use race to predict outcomes even though the original model doesn't use race directly (because race correlates with criminal history). The explanation may not reflect the model's actual computation.

3. **Explanations are incomplete** — saliency maps show *where* a network looks, not *what* it does with what it sees. Same saliency map could apply to multiple wrong classifications.

4. **Black boxes cause errors** — COMPAS recidivism tool (130+ factors, proprietary) has documented typographical errors that change bail decisions. A simple 3-rule model (CORELS) matches COMPAS accuracy.

## The accuracy–interpretability trade-off is a myth

> [!important] For structured data with meaningful features, there is often no significant performance difference between complex classifiers (deep networks, boosted trees) and simple interpretable models (logistic regression, decision lists) after proper preprocessing.

The DARPA XAI diagram (implying smooth trade-off) is fictional — no data generated it. Rudin argues that:
- The Rashomon set (set of near-optimal models for a dataset) is often large
- Large Rashomon sets are likely to contain at least one interpretable model
- Therefore, interpretable models often exist with equal accuracy — we just don't look for them

![[RsetDefinition-31757979670372.png]]

## Key example: COMPAS vs CORELS

| Property | COMPAS | CORELS model |
|----------|--------|-------------|
| Variables | 130+ factors | 3 (age, prior arrests) |
| Accuracy | ~65% | ~65% |
| Transparency | Proprietary/black box | Published 3-rule list |
| Errors possible | Typographical data entry | Minimal |

CORELS model: IF age < 21 THEN high risk / ELSE IF age > 45 THEN low risk / ELSE IF 2+ prior arrests THEN high risk / ELSE low risk.

## Regulatory implications

- EU GDPR's "right to explanation" only requires an *explanation*, not an *interpretable model*
- Less-than-satisfactory explanations can legally satisfy GDPR while being misleading
- Rudin proposes a mandate: for high-stakes decisions, no black box should be deployed when an equally accurate interpretable model exists

## Connections

- [[Explainable AI]] — XAI concept page needed; Rudin is the foundational critique
- [[Automation Bias]] — black box models increase likelihood of blind over-reliance
- [[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]] — same concern about opaque clinical systems
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — notes accuracy-explainability trade-off exists (Kelly's group takes less radical position than Rudin)
- [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]] — interpretable model of health needs would expose label bias, whereas black box conceals it

## Significance for this wiki

This paper fills the XAI gap identified in the wiki audit. It is the entry point for the Explainable AI / Interpretable ML concept area. It also provides the strongest counterargument to the "accuracy vs explainability trade-off" framing common in clinical AI literature.
