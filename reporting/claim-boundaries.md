---
title: Claim Boundaries
type: reporting
description: Rules that keep analytical claims within the evidence supplied.
tags: [claims, evidence, guardrails]
status: draft
version: 0.1.0
created: 2026-09-21
updated: 2026-09-21
related: [uncertainty-language.md, ../interpretation/longitudinal-change.md]
---

# Claim Boundaries

An analyst or LLM must not make claims beyond the supplied evidence.

- Preserve the observed direction, magnitude, unit, population, and time frame.
- Do not infer causality from association or temporal sequence alone.
- Do not claim statistical significance without an appropriate reported analysis.
- Do not translate numerical direction into “improvement,” “worsening,” or “risk” without verified domain meaning.
- Do not generalize beyond the observed population without supporting evidence.
- Do not hide missingness, denominator changes, unmatched observations, or material uncertainty.
- When evidence is insufficient, state what is known, what is unknown, and what additional evidence would be needed.

Fluent wording does not strengthen evidence. If a requested claim is unsupported, narrow or decline it rather than filling the gap with an assumption.
