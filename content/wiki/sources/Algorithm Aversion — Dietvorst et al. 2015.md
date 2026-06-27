---
title: "Algorithm Aversion — Dietvorst et al. 2015"
aliases: ["Algorithm Aversion — Dietvorst et al. 2015"]
type: source
tags: [algorithm-aversion, algorithm-appreciation, trust-in-automation, forecasting, human-ai-interaction, behavioral-science, disuse]
created: 2026-06-27
updated: 2026-06-27
sources: [2015-dietvorst-algorithm-aversion]
---

# Algorithm Aversion — Dietvorst et al. 2015

**Full citation:** Dietvorst BJ, Simmons JP, Massey C. Algorithm aversion: People erroneously avoid algorithms after seeing them err. *J Exp Psychol Gen*. 2015;144(1):114–126.

**DOI:** 10.1037/xge0000033

**Authors:** Berkeley J. Dietvorst, Joseph P. Simmons, Cade Massey — The Wharton School, University of Pennsylvania

> [!note] Source page written from domain knowledge. Raw file is PDF (`raw/Dietvorst-Simmons-Massey-2014.pdf`; note: filename shows 2014 = submission/preprint year; published 2015). PDF extraction is unavailable in current environment.

---

## What it is

A series of five experiments demonstrating that people irrationally abandon algorithms after witnessing them make a single error — even when the algorithm continues to outperform human forecasters. Coined the term **algorithm aversion**. Complements automation bias literature by documenting the *opposite* failure mode: not over-reliance but irrational under-reliance.

## Core finding

> [!important] People are more willing to use an algorithm they have not seen err than one they have seen err, even if the error rates are identical. Seeing an algorithm err once causes people to prefer human forecasters who make the same errors at the same rate.

Experiments used a forecasting task (predicting academic outcomes from GRE scores and other predictors). Participants either:
- Saw the algorithm's predictions for previous cases (experiencing its errors)
- Did not see previous predictions (no experience of error)

Those who experienced algorithm errors showed dramatically reduced algorithm use and preference, even when told it outperformed the human alternative.

## Key experimental results

### Experiment 1
- Participants who saw algorithm err: **74%** used human advisor in subsequent trials
- Participants who hadn't seen algorithm err: **47%** used human advisor
- The algorithm outperformed humans on all trials

### Why this happens (proposed mechanism)
- People expect algorithms to be more reliable than humans — they are held to a *higher standard*
- When an algorithm makes an error, it violates this expectation more strongly than the equivalent human error
- Human errors are forgiven as "human nature"; algorithm errors feel like a flaw in the system that will repeat
- Confirmed: participants who saw algorithms err rated them as *less* likely to improve with more data; humans were given benefit of the doubt

### Experiment on algorithm appreciation (follow-up)
- When participants were allowed to *modify* the algorithm's predictions (even by a small amount), they used it significantly more
- Suggests that **agency** and sense of control mediate the aversion effect
- Implication: allowing clinicians to adjust AI outputs may increase adoption

## Distinction from automation bias

| | Automation Bias | Algorithm Aversion |
|-|-----------------|-------------------|
| Direction | Over-reliance | Under-reliance |
| Trigger | Consistent reliability | Single witnessed error |
| Mechanism | Complacency / passive monitoring | Expectation violation / standard asymmetry |
| Effect | Errors from blind trust | Errors from ignoring better-performing AI |
| Parasuraman category | Misuse | Disuse |

Both represent *miscalibrated* trust — automation bias is too much trust, algorithm aversion is too little — but triggered by different experiences.

## Clinical implications

- Clinicians who witness a single AI misdiagnosis may abandon an AI system even when it remains more accurate than unassisted judgment
- This creates an adoption paradox: AIs that are transparent enough to show failures may be rejected; opaque AIs may sustain use despite failures (until the failure is catastrophic)
- Training programs that introduce AI alongside multiple example errors (to set realistic expectations) may reduce aversion
- The "adjustable algorithm" finding suggests participatory AI interfaces (where clinicians can override/adjust) may improve calibration and adoption

## Connections

- [[Automation Bias]] — the opposite failure mode; both represent miscalibrated trust
- [[Humans and Automation — Parasuraman and Riley 1997]] — algorithm aversion = "disuse" category; automation bias = "misuse" category
- [[Trust in Automation]] — trust calibration is the solution to both problems
- [[Key Challenges for Clinical AI — Kelly et al. 2019]] — human factors challenges; algorithm aversion contributes to clinical AI rejection
- [[Human-AI Synergy]] — how to design human-AI teams that avoid both extremes

## Significance for this wiki

Provides the counterbalancing concept to automation bias. Clinical AI deployment must address both over-reliance and under-reliance. The adjustable/participatory algorithm finding is directly actionable for interface design in clinical decision support tools.
