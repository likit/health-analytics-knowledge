---
title: Abnormal Prevalence
type: indicator
description: Proportion of valid observations classified as abnormal under a declared rule.
tags: [prevalence, denominator, missing-data]
status: draft
version: 0.1.0
created: 2026-09-21
updated: 2026-09-21
sources: []
related: [../methods/denominator-selection.md, ../methods/percentage-point-change.md]
---

# Abnormal Prevalence

Abnormal prevalence is the proportion of eligible, valid observations classified as abnormal under a declared classification rule.

## Components

- **Numerator:** valid observations meeting the declared abnormality rule.
- **Denominator:** eligible observations with sufficient valid data to apply that rule.
- **Valid observations:** records that pass stated inclusion and data-quality requirements.
- **Missing observations:** eligible records without sufficient data; report them separately and do not silently place them in the normal category.

```text
abnormal prevalence = abnormal valid observations / eligible valid observations
```

Always report the numerator, denominator, missing count, population, time point, and classification rule where available. Different denominator choices can change the result.

> Verification required: This object supplies analytical semantics only. It does not define clinical abnormality thresholds.
