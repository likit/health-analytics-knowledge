---
title: Health Analytics Knowledge Repository
type: repository-guide
description: Application-independent, versioned knowledge for health analytics.
tags: [health-analytics, knowledge-base, okf]
status: draft
version: 0.1.0
created: 2026-09-21
updated: 2026-09-21
---

# Health Analytics Knowledge Repository

This repository stores small, linked Markdown knowledge objects for health analytics. It follows a lightweight Open Knowledge Format (OKF) convention: YAML frontmatter provides machine-readable identity and lifecycle metadata, while Markdown remains the canonical human-readable content.

It is deliberately application-independent. Applications may supply evidence to an analyst, but their datasets, results, identifiers, and implementation details do not belong in the general knowledge objects here.

## Architecture

```text
Health Analytics Knowledge Repository   (what the health analyst knows)
                    ↓
Health Analyst Protocol / Skill          (how the analyst reasons)
                    ↓
LLM / Agent
                    ↕
Application evidence/data                (what the current data says;
                                          e.g. Health Dynamics MCP/application)
                    ↓
Validation & Guardrails                  (whether generated claims are supported)
```

The repository supplies reusable semantics, definitions, analytical methods, interpretation constraints, and reporting guidance. A future Health Analyst Protocol will describe reasoning behavior. Health Dynamics or another application will provide current evidence. Separate validation and guardrails will test whether claims remain within that evidence.

## Contents

- [Knowledge index](index.md)
- [Concepts](concepts/index.md): meanings of measures and terms
- [Indicators](indicators/index.md): defined analytical quantities
- [Methods](methods/index.md): calculation and comparison procedures
- [Interpretation](interpretation/index.md): rules for reading analytical results
- [Reporting](reporting/index.md): rules for communicating results
- [Templates](templates/): starting points for new knowledge objects
- [Golden cases](tests/golden-cases/README.md): future regression examples

## Metadata convention

Every knowledge object begins with YAML frontmatter. Use only fields meaningful to the object:

- `title`: concise human-readable name.
- `type`: stable category such as `concept`, `indicator`, `method`, `interpretation`, or `reporting`.
- `description`: one-sentence scope statement.
- `tags`: short discovery terms.
- `status`: lifecycle state; initial content uses `draft`.
- `version`: semantic version for the object, initially `0.1.0`.
- `created` and `updated`: ISO 8601 dates (`YYYY-MM-DD`).
- `sources`: verified provenance links or citations; use an empty list when none have been verified.
- `related`: repository-relative links to closely related objects.

Future objects may add `jurisdiction`, `population`, `evidence_type`, `reviewer`, `verification_date`, `review_due_date`, or `superseded_by`. Their absence currently means “not recorded,” not “not applicable.”

## Editorial rules

Keep objects atomic, link instead of copying, and distinguish definitions from methods and interpretations. Important clinical or analytical claims require traceable sources. Unverified examples must be labeled, and placeholders must never be presented as authoritative guidance. Do not add application results to general objects.

See [CHANGELOG.md](CHANGELOG.md) for repository-level changes.
