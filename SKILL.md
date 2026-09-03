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
- personal statistical policies (A personal stats / 0RAD pipeline rules)

Mount-point table (id → classified path; unlimited depth inside each pack):

| Id | Path |
|---|---|
| `02-tables` | `02-data-processing/tables/` |
| `02-imaging-io` | `02-data-processing/imaging-io/` |
| `02-imaging-qc` | `02-data-processing/imaging-qc/` |
| `02-pictures` | `02-data-processing/pictures/` |
| `02-fmri` | `02-data-processing/fmri/` |
| `02-radiomics-habitat` | `02-data-processing/radiomics-habitat/` |
| `03-lit-search` | `03-research/lit-search/` |
| `03-lit-fulltext` | `03-research/lit-fulltext/` |
| `03-lit-review` | `03-research/lit-review/` |
| `03-lit-cite` | `03-research/lit-cite/` |
| `03-design-experiment` | `03-research/design-experiment/` |
| `03-design-protocol` | `03-research/design-protocol/` |
| `03-design-grant` | `03-research/design-grant/` |
| `03-frontier-ideate` | `03-research/frontier-ideate/` |
| `03-frontier-hypothesize` | `03-research/frontier-hypothesize/` |
| `04-stats-guide` | `04-analysis/stats-guide/` |
| `04-stats-power` | `04-analysis/stats-power/` |
| `04-stats-models` | `04-analysis/stats-models/` |
| `04-model-eval` | `04-analysis/model-eval/` |
| `04-fig-flow` | `04-analysis/fig-flow/` |
| `04-fig-plot` | `04-analysis/fig-plot/` |
| `05-write-manuscript` | `05-manuscript/write-manuscript/` |
| `05-write-reporting` | `05-manuscript/write-reporting/` |
| `05-write-venue` | `05-manuscript/write-venue/` |
| `05-write-polish` | `05-manuscript/write-polish/` |
| `06-review-peer` | `06-review/review-peer/` |
| `06-review-critique` | `06-review/review-critique/` |
| `06-review-response` | `06-review/review-response/` |

`04-explainability` and `05-humanize` are not in this package.

No external Skill is mounted here. Academic Research Skills / MedSci Skills are future candidates for **A**, not contents of this package.
