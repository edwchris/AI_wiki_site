---
title: "Explainable AI"
aliases: ["Explainable AI", "XAI", "Interpretable ML"]
type: concept
tags: [explainable-ai, xai, interpretable-ml, black-box, transparency, post-hoc-explanation, saliency-maps, gdpr]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-rudin-stop-explaining-black-boxes, 2019-kelly-clinical-ai-challenges, 2017-cabitza-unintended-consequences-ml]
---

# Explainable AI

A field and set of techniques aiming to make ML model decisions understandable to humans. Often used as an umbrella term for two fundamentally different approaches that Rudin (2019) argues should be sharply distinguished.

## Rudin's critical distinction

From [[Stop Explaining Black Box ML — Rudin 2019]] — the foundational critique:

| Approach | Method | Problem |
|---------|--------|---------|
| **Explainable ML (XAI)** | Build a second model to explain the first (post-hoc) | Explanations are approximations; may be unfaithful or misleading |
| **Interpretable ML** | Design the model itself to be transparent | Predictions derivable directly from inputs; no approximation needed |

> [!important] Rudin's thesis: for high-stakes decisions, stop using post-hoc explanations of black boxes. Build inherently interpretable models instead. The accuracy–interpretability trade-off is largely a myth for structured tabular data.

## Common XAI techniques (post-hoc)

| Technique | What it provides | Limitation |
|-----------|-----------------|-----------|
| **LIME** | Local linear approximation around a prediction | Approximation; sensitive to perturbation choices |
| **SHAP** | Shapley-value attribution of feature contributions | Computationally expensive; doesn't capture interactions well |
| **Saliency maps / Grad-CAM** | Pixels that most influenced CNN predictions | Shows *where* network looks, not *what* it does with what it sees |
| **Counterfactuals** | "What would need to change to get a different prediction?" | Doesn't explain why the model made its decision |

## Why XAI matters in healthcare

1. **Clinical trust**: clinicians more likely to accept recommendations they can interrogate
2. **Regulatory**: EU GDPR gives patients "right to explanation" for automated decisions; US FDA guidance increasingly requires explanations for medical AI
3. **Safety**: when AI fails, explanation helps determine whether error was systematic or random
4. **Bias detection**: interpretable models allow auditors to check whether protected attributes drive decisions

## The accuracy–interpretability trade-off debate

**Claim (common in clinical AI literature):** More complex models (neural nets, gradient boosting) outperform interpretable models (logistic regression, decision trees); therefore transparency has a cost.

**Counter (Rudin 2019):** For structured data with meaningful features, this trade-off is largely mythological:
- The Rashomon set (set of near-optimal models) is often large for clinical tabular data
- Within a large Rashomon set, interpretable models with equivalent accuracy almost always exist
- The trade-off is real for perceptual tasks (image/language) but not for tabular clinical data

![[RsetDefinition-31757979670372.png]]

> [!warning] Contradiction: Kelly et al. (2019) state an accuracy-interpretability trade-off exists in medical imaging. Rudin (2019) says the trade-off is a myth for structured data. Both may be correct in their respective domains — the tension is at the boundary between imaging AI and clinical tabular AI.

## Interpretable model types

- **Logistic regression with meaningful features** — directly interpretable coefficients
- **Decision trees** — rules readable as flowchart
- **Rule lists / decision lists** (e.g., CORELS) — ordered IF-THEN rules; proven to match complex models for tabular data
- **Scoring systems** — integer weights allow mental calculation (APACHE-II, CURB-65 are examples of domain-expert-designed scoring systems)

## Connections

- [[Stop Explaining Black Box ML — Rudin 2019]] — foundational critique; Rashomon set argument; CORELS example
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — accuracy-interpretability trade-off framing (contrasting position)
- [[Automation Bias]] — black box models increase automation bias by preventing critical engagement with reasoning
- [[Algorithmic Fairness and Bias]] — interpretable models surface bias; black boxes conceal it
- [[Unintended Consequences of ML in Medicine — Cabitza et al. 2017]] — black box opacity = inability to detect context-free reasoning
- [[AI Ethics in Radiology]] — transparency and explainability as ethical requirements
