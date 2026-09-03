---
name: my-skills-capabilities
description: >
  Mountable generic capability package for data processing, research, analysis,
  manuscript writing, and review. Designed to be mounted by MY-SKILLS (framework A).
  Does not contain the orchestrator, Skill-discovery policy, harvest governance,
  or personal final-authority layer.
---

# MY-SKILLS Capability Package

Reusable professional modules extracted from MY-SKILLS. Independent of:

- orchestration (`00_orchestrator`)
- Skill discovery/integration policy (`01_skill-discovery-integration`)
- Skill Harvest / evolution governance
- personal writing style (Aitor-format, de-AI, corpus)
- personal review/response style
- personal statistical policies (`radiology-stats`, `0rad-pipeline-rules`)

Mount-point table (id → classified path; unlimited depth inside each pack):

| Id | Path |
|---|---|
| `02-xlsx` | `02-data-processing/xlsx/` |
| `02-imaging-qc` | `02-data-processing/imaging-qc/` |
| `02-radiomics-habitat` | `02-data-processing/radiomics-habitat/` |
| `02-impute` | `02-data-processing/impute/` |
| `02-generic-docs` | `02-data-processing/generic-docs/` |
| `03-lit-search` | `03-research/lit-search/` |
| `03-lit-review` | `03-research/lit-review/` |
| `03-lit-cite` | `03-research/lit-cite/` |
| `03-design-experiment` | `03-research/design-experiment/` |
| `03-design-grant` | `03-research/design-grant/` |
| `03-frontier-ideate` | `03-research/frontier-ideate/` |
| `03-frontier-hypothesize` | `03-research/frontier-hypothesize/` |
| `04-stats-guide` | `04-analysis/stats-guide/` |
| `04-stats-power` | `04-analysis/stats-power/` |
| `04-stats-models` | `04-analysis/stats-models/` |
| `04-figure-engine` | `04-analysis/figure-engine/` |
| `05-write-manuscript` | `05-manuscript/write-manuscript/` |
| `05-write-venue` | `05-manuscript/write-venue/` |
| `06-review-peer` | `06-review/review-peer/` |
| `06-review-critique` | `06-review/review-critique/` |

`04-explainability` and `05-humanize` are not in this package.

No external Skill is mounted here. Academic Research Skills / MedSci Skills are future candidates for **A**, not contents of this package.
