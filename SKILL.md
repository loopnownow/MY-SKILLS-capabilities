---
name: my-skills-base
description: >
  Mountable generic capability package for data processing, research, analysis,
  manuscript writing, and review. Designed to be mounted by MY-SKILLS (framework A).
  Does not contain the orchestrator, Skill-discovery policy, harvest governance,
  or personal final-authority layer.
---

# MY-SKILLS-base (capability package)

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
| `03-fill-protocol` | `03-research/fill-protocol/` |
| `03-find-journal` | `03-research/find-journal/` |
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
| `07-review-response` | `07-response/review-response/` |

`02-tables` is clinical Excel/CSV (headers, missingness, ID, cohort). Nested `xlsx-office/` is the Anthropic office/xlsx skill; nested `impute/` is fill/outlier implementation.

`04-explainability` is not in this package. `humanize` lives under `05-manuscript/humanize/`. Cross-pack stubs pruned 2026-10-17.

External cross-pack stubs were pruned 2026-10-17 (archived under `D:\0del\b-prune-findjournal-fill-20261017\`). MedSci fill-protocol body is native under `03-research/fill-protocol/`.
