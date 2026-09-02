---
name: my-skills-capabilities
description: >
  Mountable generic capability package for data processing, research, analysis,
  manuscript writing, and review. Designed to be mounted by MY-SKILLS (framework A).
  Does not contain the orchestrator, Skill-discovery policy, harvest governance,
  or personal final-authority layer (except de-ai, which the user moved here).
---

# MY-SKILLS Capability Package

Reusable professional modules extracted from MY-SKILLS. Independent of:

- orchestration (`00_orchestrator`)
- Skill discovery/integration policy (`01_skill-discovery-integration`)
- Skill Harvest / evolution governance
- personal writing style (Aitor-format, corpus)
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
| `03-literature` | `03-research/literature/` |
| `03-design` | `03-research/design/` |
| `03-frontier` | `03-research/frontier/` |
| `04-stats-generic` | `04-analysis/stats-generic/` |
| `04-figure-engine` | `04-analysis/figure-engine/` |
| `05-writing-generic` | `05-manuscript/writing-generic/` |
| `05-de-ai` | `05-manuscript/de-ai/` |
| `06-review-generic` | `06-review/review-generic/` |

No external Skill is mounted here. Academic Research Skills / MedSci Skills are future candidates for **A**, not contents of this package.
