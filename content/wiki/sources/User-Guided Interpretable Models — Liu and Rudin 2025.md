---
title: "User-Guided Interpretable Models — Liu and Rudin 2025"
aliases: ["User-Guided Interpretable Models — Liu and Rudin 2025"]
type: source
tags: [interpretable-ml, rashomon-effect, user-guided-modeling, sparsity, interaction-bottleneck, explainable-ai]
created: 2026-06-27
updated: 2026-06-27
sources: [2025-liu-rudin-user-guided-rashomon]
---

# User-Guided Interpretable Models — Liu and Rudin 2025

**Full citation:** Liu J, Rudin C. User-guided interpretable models: Rashomon effect, interaction, and computation. *Harvard Data Sci Rev*. 2025;7(3).

**URL:** hdsr.mitpress.mit.edu/pub/m3fppgon/release/1

**Published:** 2025-10-17

**Authors:** Jiachang Liu, [[Cynthia Rudin]] — Duke University

---

## What it is

A commentary on Chatterjee et al. (2025) "Univariate-guided sparse regression" (uniLasso), which Liu and Rudin use as a launch point to articulate their broader vision for user-guided interpretable ML via the Rashomon set paradigm. Published in *Harvard Data Science Review*, the piece extends the arguments in [[Stop Explaining Black Box ML — Rudin 2019]] with a more constructive, implementation-focused vision.

---

## The coefficient sign-flip problem

When adding variables to a regression model, the sign of a predictor coefficient can flip — a variable that appears protective in univariate analysis becomes harmful in the multivariate model (or vice versa). This is a Rashomon effect consequence: many models have similar accuracy but different variable relationships.

uniLasso (Chatterjee et al. 2025) addresses this by constraining multivariate coefficients to preserve univariate signs, producing sparser and more interpretable models without sacrificing accuracy.

---

## The Rashomon set paradigm

![[RsetDefinition-31757979670372.png]]

*Figure 1 from the paper: The Rashomon set is the red bar at the bottom of the loss curve — a flat basin of equally good models, not a sharp point minimum.*

> "The landscape of the loss function is not a sharp valley with a single point at the bottom, but a wide, flat basin. Within this 'Rashomon set' of well-performing models, there exist models with desirable properties — sparsity, preserved signs, fairness constraints, and even integer coefficients."

Key implication: the existence of a large Rashomon set means the data alone cannot determine which model should be used. This gives the practitioner licence to impose domain constraints (monotonicity, sparsity, sign preservation) without sacrificing accuracy — there will likely be a model in the Rashomon set that satisfies them.

---

## The interaction bottleneck

A new concept introduced in this paper:

> The *interaction bottleneck* arises when domain experts do not know in advance exactly what they are looking for, want to interact with the algorithm to improve the model, and find that they need to (painstakingly) reformulate the problem repeatedly and rerun the algorithm.

The solution is the **Rashomon set paradigm**: instead of finding one optimal model, find many good models and let the user navigate among them interactively. Tools developed by Rudin's group:
- **TimberTrek** — interactive visualisation of all sparse decision trees in the Rashomon set
- **GAM Changer** — allows users to edit generalised additive models within a browser interface
- **Riskomon** — card deck explorer for scoring system Rashomon sets

---

## Significance for this wiki

Extends [[Stop Explaining Black Box ML — Rudin 2019]] from critique to construction. Provides:
1. A positive vision for interpretable ML (not just "stop using black boxes")
2. The interaction bottleneck framing — users + domain expertise must guide model selection
3. The Rashomon set paradigm as a practical interface design approach
4. Evidence that imposing domain constraints (clinically meaningful monotonicity) doesn't hurt accuracy

Particularly relevant to clinical AI: physicians cannot reformulate optimisation problems. Interactive tools that visualise the Rashomon set and let clinicians choose the model that makes sense to them address this gap directly.

---

## Connections

- [[Stop Explaining Black Box ML — Rudin 2019]] — the 2019 paper is the critique; this 2025 commentary is the constructive vision
- [[Explainable AI]] — Rashomon set paradigm as an alternative to XAI
- [[Cynthia Rudin]] — second-author; this continues her programme
- [[Algorithmic Fairness and Bias]] — fairness constraints can be imposed within the Rashomon set without accuracy loss
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — the interaction bottleneck is a form of the human factors challenges Kelly describes
