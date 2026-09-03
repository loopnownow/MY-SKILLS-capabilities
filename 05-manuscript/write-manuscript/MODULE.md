---
name: "write-manuscript"
domain: "05_manuscript"
trigger: ["SCI写作", "写引言", "写讨论", "IMRAD", "起草全文"]
inputs: ["results_tables", "draft"]
outputs: ["imrad_draft"]
quality_control: "numbers only from supplied results; no invented n/AUC/ethics IDs"
owner: "05-manuscript/write-manuscript/MODULE.md"
---

# trigger is documentation only; not independently discoverable.

# Generic IMRAD manuscript draft

Draft and revise **scientific prose** (Title / Abstract / Introduction / Methods / Results /
Discussion). This pack is **generic IMRAD only**.

**Not in this pack (stay in A personal, or other B ids):**

- Personal house format / title-page defaults
- de-AI forbidden lists and detectors
- Lab ethics IRB wording and author-line defaults
- Language polish → [`05-write-polish`](../write-polish/MODULE.md)
- Journal selection / house style → [`05-write-venue`](../write-venue/MODULE.md)
- TRIPOD / CLAIM / CLEAR checklists → [`05-write-reporting`](../write-reporting/MODULE.md)
- Self-audit → `06-review-critique`; other-paper review → `06-review-peer`; response → `06-review-response`

## When to use

- Draft or rewrite IMRAD sections from supplied facts
- Keep observational language (`associated with`) unless the design supports causation
- Export a Methods skeleton from `methods_template_export.md`

**Do not use this module** for polish-only passes, 选刊, or 回复审稿人.

## Hard rules

1. Numbers stick to assertions (n, AUC, CI, *P*); no empty claims
2. Problem → gap → approach in the Introduction
3. Observational designs: *associated with*, not causal verbs
4. Consistent terms; expand abbreviations at first use
5. Short sentences; do not invent results, citations, ethics numbers, or unrun experiments
6. Missing facts → comments / open questions, never fabricated body text
7. Patient-level split language when the study is predictive
8. Dual-set reporting when the user supplied both training and test metrics

## Modes

| Mode | Open |
|------|------|
| `draft-section` | this file + [section-templates.md](section-templates.md) + [radiology-writing/](radiology-writing/) |
| `full-imrad` | [mode-1-sci.md](mode-1-sci.md) + [pipeline-stages.md](pipeline-stages.md) (prediction papers) |
| `methods-skeleton` | [methods_template_export.md](methods_template_export.md) + [radiology-writing/methods.md](radiology-writing/methods.md) |
| `ethics-sentence` | [radiology-ethics/approval-consent.md](radiology-ethics/approval-consent.md) — placeholders only; no lab default IRB |
| `outline` | [mode-academic-pipeline.md](mode-academic-pipeline.md) |
| `polish` | **handoff** → `05-write-polish` |
| `venue-shape` | **handoff** → `05-write-venue` |
| `reporting` | **handoff** → `05-write-reporting` |

## IMRAD map

| Section | File |
|---------|------|
| Abstract | [radiology-writing/structured-abstract.md](radiology-writing/structured-abstract.md) |
| Architecture | [radiology-writing/article-architecture.md](radiology-writing/article-architecture.md) |
| Methods | [radiology-writing/methods.md](radiology-writing/methods.md) |
| Results | [radiology-writing/results.md](radiology-writing/results.md) |
| Discussion | [radiology-writing/discussion.md](radiology-writing/discussion.md) |
| Citation gate | [radiology-citation/claim-verification-gate.md](radiology-citation/claim-verification-gate.md) |
| Figures | patient-flow → `04-fig-flow`; plots → `04-fig-plot` |

## Envelope

```text
Skill: 05-write-manuscript
Subtask: draft-section | full-imrad | methods-skeleton | outline
Venue: (unknown unless user named one)

[Draft]

Missing inputs:
- ...

Next: 05-write-polish (language) · 05-write-venue (shape) · 06-review-critique (self-audit)
```
