# MY-SKILLS-capabilities

Mountable **generic** capability package for [loopnownow/MY-SKILLS](https://github.com/loopnownow/MY-SKILLS) (framework A).

A = orchestrator + personal lab layer. **B = reusable skills only.**
Nothing in this repo is auto-mounted. Framework A `registry.yaml` records the live mounts.

Layout follows A's coarse ids (CHG-20260903-008; audit-fix CHG-20260903-013). Unlimited depth inside each pack. Each id has a thin `SKILL.md` that points at `MODULE.md`.

```
02-data-processing/   tables, imaging-io, imaging-qc, pictures, fmri, radiomics-habitat
03-research/          lit-search, lit-fulltext, lit-review, lit-cite,
                      design-experiment, design-protocol, design-grant,
                      frontier-ideate, frontier-hypothesize
04-analysis/          stats-guide, stats-power, stats-models, model-eval, fig-flow, fig-plot
05-manuscript/        write-manuscript, write-reporting, write-venue, write-polish
06-review/            review-peer, review-critique, review-response
```

`04-explainability` and `05-humanize` are **not** in B (MedSci-only in A).

## How A mounts B

1. In MY-SKILLS, `01_skill-discovery-integration` evaluates a candidate.
2. The user explicitly approves (silence is not approval).
3. A records the id in `01_skill-discovery-integration/registry.yaml` as `MOUNTED`.
4. Domain skills call **ids**, not old umbrella folders (`literature/`, `writing-generic/`, …).

Until step 3, A may keep local generic copies marked in `EXTERNALIZATION_CANDIDATES.md`. de-AI is in A `05_manuscript/personal/` (2026-09-02).

## Mount points (ids → paths)

| Id | Path | Use |
|---|---|---|
| `02-tables` | `02-data-processing/tables/` | Clinical Excel/CSV + impute |
| `02-imaging-io` | `02-data-processing/imaging-io/` | CT/MRI DICOM · NIfTI I/O |
| `02-imaging-qc` | `02-data-processing/imaging-qc/` | CT/MRI ROI / reader QC |
| `02-pictures` | `02-data-processing/pictures/` | TIFF / PNG / JPG / PDF-as-image |
| `02-fmri` | `02-data-processing/fmri/` | fMRI DICOM / NIfTI |
| `02-radiomics-habitat` | `02-data-processing/radiomics-habitat/` | Radiomics/habitat **preparation** (paper modelling → A `04_analysis`) |
| `03-lit-search` | `03-research/lit-search/` | Literature search / sources / public datasets |
| `03-lit-fulltext` | `03-research/lit-fulltext/` | Full-text retrieve (stub) |
| `03-lit-review` | `03-research/lit-review/` | Evidence synthesis |
| `03-lit-cite` | `03-research/lit-cite/` | DOI→BibTeX helper (no Zotero pack) |
| `03-design-experiment` | `03-research/design-experiment/` | Study design / validation / blueprints |
| `03-design-protocol` | `03-research/design-protocol/` | Protocol write/fill (stub) |
| `03-design-grant` | `03-research/design-grant/` | Generic grant slot; A Voice A/B still wins |
| `03-frontier-ideate` | `03-research/frontier-ideate/` | Frontier themes / topic brainstorm |
| `03-frontier-hypothesize` | `03-research/frontier-hypothesize/` | Idea → question / hypothesis |
| `04-stats-guide` | `04-analysis/stats-guide/` | Test selection / assumptions / reporting |
| `04-stats-power` | `04-analysis/stats-power/` | Sample size / power |
| `04-stats-models` | `04-analysis/stats-models/` | Bayesian notes / assumption script (not 0RAD) |
| `04-model-eval` | `04-analysis/model-eval/` | Calibration / DCA / external validation |
| `04-fig-flow` | `04-analysis/fig-flow/` | STROBE / patient-flow |
| `04-fig-plot` | `04-analysis/fig-plot/` | Statistical plots / imaging panels |
| `05-write-manuscript` | `05-manuscript/write-manuscript/` | Generic writing |
| `05-write-reporting` | `05-manuscript/write-reporting/` | TRIPOD / CLAIM / CLEAR |
| `05-write-venue` | `05-manuscript/write-venue/` | Journal selection / house style |
| `05-write-polish` | `05-manuscript/write-polish/` | Generic academic English (not de-AI) |
| `06-review-peer` | `06-review/review-peer/` | Other-paper peer review |
| `06-review-critique` | `06-review/review-critique/` | Self-audit / pre-submission |
| `06-review-response` | `06-review/review-response/` | Point-by-point response |

Translational / reader-study **design** mounts (when approved) belong under `03-research/` — A personal `clinical-translation` stays in MY-SKILLS; do not copy it here.

This package does **not** contain personal Aitor-format, de-AI, personal review/response style, 0RAD pipeline rules, radiology-stats lab policy, ethics form packs, or MATLAB preprocess scripts.

## Safety

- No PHI, no patient tables, no unpublished manuscripts.
- No ethics scans, phone numbers, or grant full texts.
- Do not treat this pack as a mounted Skill until A’s registry says so.

Default *external* candidates (not this repo): `Imbad0202/academic-research-skills`, `Aperivue/medsci-skills`. Both remain PROPOSED in A until approved.
