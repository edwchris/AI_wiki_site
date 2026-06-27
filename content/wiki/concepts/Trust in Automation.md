---
title: "Trust in Automation"
aliases: ["Trust in Automation"]
type: concept
tags: [trust-in-automation, human-factors, automation, calibration, reliance, complacency, algorithm-aversion]
created: 2026-06-27
updated: 2026-06-27
sources: [1997-parasuraman-riley-humans-automation, 2004-lee-see-trust-automation, 2014-hoff-bashir-trust-automation, 2010-parasuraman-manzey-complacency-bias, 2015-dietvorst-algorithm-aversion]
---

# Trust in Automation

The degree to which an operator relies on automated systems in ways that are calibrated to the automation's actual reliability. Appropriate trust — neither over- nor under-reliance — is the design target.

---

## Calibration Is the Goal

| Trust State | Reliance | Outcome |
|------------|---------|---------|
| Over-trust (miscalibrated high) | Over-reliance | [[Automation Bias]] — commission and omission errors |
| Appropriate trust (calibrated) | Appropriate reliance | Best outcomes |
| Under-trust (miscalibrated low) | Algorithm aversion | AI benefits unused; operator ignores valid recommendations |

Both miscalibrations are costly in medicine. Over-trust misses errors; under-trust wastes AI capability. Neither extreme is inherently safer.

---

## Three Bases of Trust (Lee & See 2004)

- **Performance**: Does the system work reliably? (Built from experience)
- **Process**: Do I understand how/why it works? (Built from transparency)
- **Purpose**: Is it designed with my goals in mind? (Built from context and institutional trust)

---

## Three Layers of Trust (Hoff & Bashir 2014)

- **Dispositional**: stable individual tendency to trust in general (personality trait)
- **Situational**: context-modulated trust shaped by task, environment, specific experience
- **Learned**: accumulated from interactions with this specific system over time

---

## Factors That Shape Trust

| Factor | Effect |
|--------|--------|
| System reliability (high) | Increases trust → risk of over-trust |
| Observed failures | Decreases trust (negative > positive asymmetry) |
| Transparency | Increases process-based trust; may reduce blind over-trust |
| High workload | Increases over-reliance (cognitive shortcut) |
| Time pressure | Increases over-reliance |
| Domain expertise | Better calibration but not immunity |

---

## Calibration Mechanisms

From [[Automation Bias Systematic Review — Goddard et al. 2012]] and [[Trust in Automation — Lee and See 2004]]:
- **Display uncertainty explicitly** — confidence intervals, not just point estimates
- **Show failure modes** in training and introduction
- **Provide ongoing performance feedback** — operators need to see when AI is wrong
- **Frame as information, not command** — status display > recommendation display
- **Embed accountability explicitly** — make clear the clinician owns the decision

---

## Algorithm Aversion

The flip side of automation bias. Users who observe AI errors sometimes over-discount AI performance relative to equivalent human errors. [[Algorithm Aversion — Dietvorst et al. 2015]] showed that seeing an algorithm err once causes people to prefer human forecasters who make the same errors at the same rate — a violation of calibration in the direction of under-trust.

Remedy: allow users to modify algorithm outputs (agency restores use). See [[Algorithm Aversion]] for full treatment.

---

## Foundational Framework

[[Humans and Automation — Parasuraman and Riley 1997]] provides the stage × level taxonomy that underlies all trust and reliance concepts:
- **Misuse** = automation bias (over-reliance)
- **Disuse** = algorithm aversion (under-reliance)
- **Use** = calibrated appropriate reliance
- **Abuse** = poorly designed automation

---

## Related Pages
- [[Humans and Automation — Parasuraman and Riley 1997]] — foundational taxonomy
- [[Trust in Automation — Lee and See 2004]]
- [[Trust in Automation — Hoff and Bashir 2014]]
- [[Complacency and Bias in Human Use of Automation — Parasuraman and Manzey 2010]]
- [[Automation Bias]]
- [[Automation Bias Systematic Review — Goddard et al. 2012]]
- [[Algorithm Aversion]]
- [[Algorithm Aversion — Dietvorst et al. 2015]]
- [[Situation Awareness]]
- [[Ironies of Automation]]
- [[AI-Human Role Separation]]
- [[Human-Centered AI Evaluation]]
