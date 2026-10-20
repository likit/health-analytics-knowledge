---
title: Persistent Abnormality
type: indicator
description: Repeated abnormal classifications for the same analytical unit across defined observations.
tags: [longitudinal, persistence, matched-data]
status: draft
version: 0.1.0
created: 2026-09-21
updated: 2026-09-21
sources: []
related: [../methods/paired-comparison.md, ../interpretation/cross-sectional-vs-longitudinal.md]
---

# Persistent Abnormality

Persistent abnormality means that the same analytical unit meets a declared abnormality rule at each of the required observation points.

Specify the unit being followed, matching key, required time points, allowable interval, classification rule, and treatment of missing observations. A person abnormal at only one time point is not persistently abnormal under a two-time-point definition. Cross-sectional prevalence at two dates cannot by itself identify persistence in individuals.

> Verification required: The number and timing of observations and all clinical classification rules must be defined for the intended use case.
