---
title: "Racial Bias in Health Algorithm — Obermeyer et al. 2019"
aliases: ["Racial Bias in Health Algorithm — Obermeyer et al. 2019"]
type: source
tags: [algorithmic-bias, racial-bias, health-equity, ai-ethics, label-choice, healthcare-algorithms, proxy-variables]
created: 2026-06-27
updated: 2026-06-27
sources: [2019-obermeyer-racial-bias-algorithm]
---

# Racial Bias in Health Algorithm — Obermeyer et al. 2019

**Full citation:** Obermeyer Z, Powers B, Vogeli C, Mullainathan S. Dissecting racial bias in an algorithm used to manage the health of populations. *Science*. 2019;366(6464):447–453.

**DOI:** 10.1126/science.aax2342

---

## What it is

An empirical dissection of racial bias in a commercial population health management algorithm used by approximately 200 million people per year in the US. Rare study in that the authors had access to the algorithm's inputs, outputs, and objective function — enabling them to identify the precise mechanism of bias.

## Key finding

> [!important] At the same risk score, Black patients are considerably sicker than White patients. Fixing this would increase Black patients receiving additional care from 17.7% to 46.5%.

The algorithm exhibits racial bias **not** because of design intent, but because of **label choice**: it predicts future healthcare costs rather than future health needs. Because Black patients receive less care for the same health needs (structural inequality), cost is a biased proxy.

## Study design

- N = 49,618 patients (43,539 White, 6,079 Black) across 2013–2015
- Primary care patients enrolled in risk-based contracts at a large academic hospital
- Outcome measures: algorithmic risk scores + actual health outcomes (chronic conditions, biomarkers) + costs

## Quantitative evidence of bias

- At the 97th risk percentile (auto-enrollment threshold): Black patients have **26.3% more chronic conditions** than White patients (4.8 vs 3.8)
- Black patients show worse biomarkers for hypertension, diabetes, renal failure, and anemia at every risk score level
- Key differences at equal risk: hypertension +5.7 mmHg systolic (7.6% mortality difference), HbA1c +0.6% (30% mortality difference)

## Mechanism

1. Algorithm trained on **total healthcare costs** as label (proxy for health needs)
2. Black patients generate **$1,801 less** per year in healthcare costs than White patients with the same number of chronic conditions
3. Therefore: algorithm correctly predicts costs, but costs do not reflect health needs equally by race
4. Algorithm "correctly" concludes Black patients are healthier — because they use less care — but this reflects access barriers, not actual health status

## Fix

Changing the label from "predicted cost" to a health-based measure (combining cost + active chronic conditions) reduced excess chronic conditions in Black patients at same risk from 48,772 to 7,758 — an **84% reduction in bias** — with the same algorithmic infrastructure.

## Broader implications

- "Label choice bias" — the single most important decision in algorithm development is often made without awareness of its equity implications
- Same mechanism operates in criminal justice (measuring crime = measuring policing), employment (predicting supervisor ratings), and retail (uniform pricing penalizes poor areas)
- Proprietary algorithms at scale cannot be audited; this study was possible only because researchers had unusual access

> [!important] The algorithm manufacturer independently replicated the findings on their national dataset of 3.7 million patients, confirming the results were not an artifact of the academic setting.

## Connections

- [[Algorithmic Fairness and Bias]] — concept page needed; this is the empirical anchor for that concept
- [[Stop Explaining Black Box ML — Rudin 2019]] — interpretable model would have surfaced this bias; black box concealed it
- [[Implementing ML in Healthcare Ethical Challenges — Char et al. 2018]] — ethical framing of algorithm bias
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — mentions algorithmic bias as a key challenge
- [[AI Ethics in Radiology]] — this is the empirical paper that grounds abstract ethical principles

## Significance

Provides the concrete, quantitative empirical demonstration that algorithmic bias in healthcare is real, measurable, and fixable. Essential citation for any discussion of AI fairness in health contexts. Also demonstrates that bias can arise from "reasonable" label choices rather than malicious intent.
