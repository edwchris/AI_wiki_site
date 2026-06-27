---
title: "Algorithmic Fairness and Bias"
aliases: ["Algorithmic Fairness and Bias"]
type: concept
tags: [algorithmic-bias, algorithmic-fairness, health-equity, racial-bias, label-choice, proxy-variables, ai-ethics]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-obermeyer-racial-bias-algorithm, 2018-char-ml-ethics-healthcare, 2019-kelly-clinical-ai-challenges]
---

# Algorithmic Fairness and Bias

The field of AI bias and fairness addresses how ML systems can produce discriminatory or inequitable outputs even when no explicit discriminatory intent exists. In healthcare, this is particularly consequential because biased algorithms can compound existing health disparities at scale.

## Taxonomy of bias sources

| Source | Description | Example |
|--------|-------------|---------|
| **Label choice bias** | Training label is a biased proxy for the intended target | Predicting healthcare costs as proxy for health needs (Obermeyer 2019) |
| **Historical bias** | Training data reflects historical inequalities in care access | Framingham equations trained on predominantly White cohort (Char 2018) |
| **Outcome noise** | Ground truth labels are themselves unreliable or biased | Inter-rater disagreement; proxy outcomes differ by demographic group |
| **Selection bias** | Training population unrepresentative of deployment population | Models trained on academic hospitals fail in community settings |
| **Measurement bias** | Features measured differently across groups | Pain scores rated systematically differently for Black vs. White patients |

## Empirical anchor: Obermeyer et al. 2019

[[Racial Bias in Health Algorithm — Obermeyer et al. 2019]] provides the most rigorous published dissection of a live commercial algorithm:

- Algorithm predicted future healthcare cost as proxy for health needs
- At the same risk score, Black patients had **26.3% more chronic conditions** than White patients
- Mechanism: Black patients generate $1,801 less per year in healthcare costs for the same health status due to access barriers
- Fix: change label from cost → health prediction → 84% bias reduction

> [!important] The algorithm was not "broken" — it correctly predicted what it was trained to predict. The bias arose from a reasonable-seeming label choice that embedded structural inequality.

## Fairness criteria (competing definitions)

Technical fairness criteria are mathematically incompatible — no single metric satisfies all simultaneously:

- **Demographic parity**: equal prediction rates across groups
- **Equalized odds**: equal true positive and false positive rates across groups
- **Calibration**: predictions mean the same thing across groups (a 70% risk = 70% probability regardless of race/sex)
- **Individual fairness**: similar individuals treated similarly

Choosing a fairness criterion is a value judgment, not a technical one.

## Why healthcare AI is especially vulnerable

1. **Proxy labels are unavoidable**: Direct measurement of health is expensive; proxies (cost, test results, diagnoses) embed access inequalities
2. **Scale**: A biased algorithm used in population health management affects millions without individual clinical oversight
3. **Opacity**: Black box models make bias harder to detect (Rudin 2019 argument — see [[Stop Explaining Black Box ML — Rudin 2019]])
4. **Proprietary barriers**: Most commercial clinical AI is proprietary; external audit requires special access

## Mitigation strategies

1. **Audit before deployment**: test for differential performance across demographic groups
2. **Retrain on representative data**: ensure training population matches deployment population
3. **Change the label**: if the label is biased, replace it with a less-biased alternative
4. **Ongoing monitoring**: bias can emerge after deployment as populations shift
5. **Interpretable models**: easier to detect bias in transparent models

## Connections

- [[Ziad Obermeyer]] — lead author of the foundational bias dissection study
- [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]] — empirical anchor; label choice bias mechanism
- [[Implementing ML in Healthcare Ethical Challenges — Char et al. 2018]] — ethical framing; Framingham example
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — three-source model of bias (model bias, variance, outcome noise)
- [[Stop Explaining Black Box ML — Rudin 2019]] — interpretable models surface bias; black boxes conceal it
- [[AI Ethics in Radiology]] — governance and oversight in radiology-specific context
- [[Human-Centered AI Evaluation]] — bias detection requires human-centered evaluation frameworks
