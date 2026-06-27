---
title: "Implementing ML in Healthcare Ethical Challenges — Char et al. 2018"
aliases: ["Implementing ML in Healthcare Ethical Challenges — Char et al. 2018"]
type: source
tags: [ai-ethics, healthcare-ml, algorithmic-bias, fiduciary-responsibility, machine-learning, ethical-challenges, clinical-decision-support]
created: 2026-06-27
updated: 2026-06-27
sources: [2018-char-ml-ethics-healthcare]
---

# Implementing ML in Healthcare Ethical Challenges — Char et al. 2018

**Full citation:** Char DS, Shah NH, Magnus D. Implementing machine learning in health care — addressing ethical challenges. *N Engl J Med*. 2018;378(11):981–983.

**DOI:** 10.1056/NEJMp1714229

**Authors:** Stanford University — Departments of Anesthesiology (Char), Biomedical Ethics + Biomedical Informatics Research (Magnus + Shah)

---

## What it is

A Perspective piece in the *New England Journal of Medicine* identifying four ethical challenges specific to deploying ML in clinical medicine. Written from a combined clinical, bioethics, and informatics perspective. Short but influential; frequently cited in clinical AI ethics discussions.

## Four ethical challenges

### 1. Algorithmic bias embedded in data

ML algorithms trained on historical clinical data inherit and may amplify existing disparities:

- Framingham Heart Study cardiovascular risk equations were developed in a predominantly White cohort and known to overestimate risk in Black patients — ML models trained on similar historical datasets repeat this structural problem
- Differs from traditional guideline bias: ML operates at scale and opacity, making biased decisions for millions of patients without the transparent reasoning that allows clinicians to apply judgment
- See also [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]] for empirical demonstration

### 2. The intent behind the design

The values of algorithm developers shape clinical outcomes — often without clinician or patient awareness:

> "Just as the designers of Uber's Greyball software intended its tracking system to be used for detecting drunk driving but the company later used it to identify and deceive regulators, or Volkswagen engineers used software to manipulate emissions data, ML programmers in health care may design an algorithm for one purpose that is later used for another."

- Commercial developers may optimise for profitability, not patient benefit
- An algorithm optimised for hospital revenue may recommend expensive interventions for patients who don't clinically need them
- Analogous to pharmaceutical companies selectively reporting trial data; but more difficult to detect in ML systems

### 3. Shifts in the fiduciary relationship

Traditional medical ethics centres on a fiduciary relationship: clinicians owe patients undivided loyalty. ML introduces:

- Third parties (algorithm developers, data brokers) into the therapeutic relationship
- Risk that physician judgment becomes algorithmic: "the collective medical mind may become encoded in an algorithm"
- Clinicians who follow algorithm recommendations are partially absolved of individual moral responsibility — raising questions about accountability

> [!important] Who is responsible when an ML recommendation causes harm? The clinician who followed it? The developer who built it? The hospital who deployed it? Current legal and ethical frameworks don't clearly answer this.

### 4. Reframing confidentiality

EHR data aggregated for ML training blurs traditional confidentiality norms:

- Patients provide data during individual care episodes but may not understand that aggregate EHR data trains algorithms affecting other patients
- "Learning health systems" require ongoing data use that exceeds original consent scope
- Re-identification risk from ML models trained on supposedly anonymised data is underestimated

## Proposed safeguards

Char et al. call for:
- Transparent reporting of algorithm training data sources and known biases
- Clear disclosure when clinical decisions are algorithm-assisted
- Equity auditing before deployment and ongoing after deployment
- Maintained clinician discretion to override algorithm recommendations

## Connections

- [[Racial Bias in Health Algorithm — Obermeyer et al. 2019]] — empirical proof of point 1 (algorithmic bias)
- [[Stop Explaining Black Box ML — Rudin 2019]] — opacity makes point 2 (intent) harder to detect; interpretable models would help
- [[AI Ethics in Radiology]] — this paper provides the bioethics framework for that concept page
- [[Automation Bias]] — point 3 (fiduciary shift) is worsened when clinicians over-rely on algorithms
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — similarly notes bias and regulatory challenges but from a technical framing
