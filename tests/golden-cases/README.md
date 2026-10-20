---
title: Golden Cases
type: test-guide
description: Illustrative regression cases for future health analyst behavior testing.
tags: [golden-cases, regression-testing, llm]
status: draft
version: 0.1.0
created: 2026-09-21
updated: 2026-09-21
related: [../../methods/percentage-point-change.md, ../../reporting/claim-boundaries.md]
---

# Golden Cases

Golden cases will provide small, reviewable evidence-and-expectation fixtures. They are intended to test whether different LLMs reliably apply this shared knowledge and a future Health Analyst Protocol. They are not clinical guidelines, real-world findings, or application data.

## Case: BMI-001

**Status:** Illustrative synthetic regression case.

### Evidence

- 2025 abnormal prevalence = 37.2%
- 2026 abnormal prevalence = 36.8%

### Required interpretation

The prevalence decreased by 0.4 percentage points.

### Potentially acceptable wording

- decreased slightly
- remained broadly similar while decreasing by 0.4 percentage points

### Forbidden unsupported interpretations

- increased
- worsened
- risk increased
- improved significantly

The case checks direction, percentage-point arithmetic, and claim boundaries. “Worsened,” “risk,” and “improved significantly” require clinical or statistical evidence not supplied here.

Future cases should identify their evidence, required facts, acceptable variation, forbidden claims, rationale, and reviewer status. Executable test infrastructure is intentionally out of scope for this repository stage.
