# MY-SKILLS-capabilities

Mountable **generic** capability package for [loopnownow/MY-SKILLS](https://github.com/loopnownow/MY-SKILLS) (framework A).

A = orchestrator + personal lab layer. **B = reusable skills only.**
Nothing in this repo is auto-mounted. Framework A `registry.yaml` records the live mounts.

Layout follows A's coarse ids (CHG-20260903-008). Unlimited depth inside each pack:

```
02-data-processing/   tables, imaging, pictures, fmri, radiomics-habitat
03-research/          lit-search, lit-review, lit-cite, design-experiment, design-grant,
                      frontier-ideate, frontier-hypothesize
04-analysis/          stats-guide, stats-power, stats-models, figure-engine
05-manuscript/        write-manuscript, write-venue
06-review/            review-peer, review-critique
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
| `02-imaging` | `02-data-processing/imaging/` | CT/MRI DICOM · NIfTI · NII (no personal MATLAB) |
| `02-pictures` | `02-data-processing/pictures/` | TIFF / PNG / JPG / PDF-as-image |
| `02-fmri` | `02-data-processing/fmri/` | fMRI DICOM / NIfTI |
| `02-radiomics-habitat` | `02-data-processing/radiomics-habitat/` | Radiomics/habitat **preparation** (paper modelling → A `04_analysis`) |
| `03-lit-search` | `03-research/lit-search/` | Literature search / sources / public datasets |
| `03-lit-review` | `03-research/lit-review/` | Evidence synthesis |
| `03-lit-cite` | `03-research/lit-cite/` | DOI→BibTeX helper (no Zotero pack) |
| `03-design-experiment` | `03-research/design-experiment/` | Study design / validation / blueprints |
| `03-design-grant` | `03-research/design-grant/` | Generic grant slot; A Voice A/B still wins |
| `03-frontier-ideate` | `03-research/frontier-ideate/` | Frontier themes / topic brainstorm |
| `03-frontier-hypothesize` | `03-research/frontier-hypothesize/` | Idea → question / hypothesis |
| `04-stats-guide` | `04-analysis/stats-guide/` | Test selection / assumptions / reporting |
| `04-stats-power` | `04-analysis/stats-power/` | Sample size / power |
| `04-stats-models` | `04-analysis/stats-models/` | Bayesian notes / assumption script (not 0RAD) |
| `04-figure-engine` | `04-analysis/figure-engine/` | Figure generation (journal-family visual style / Nature figure spec) |
| `05-write-manuscript` | `05-manuscript/write-manuscript/` | Generic writing, reporting, citation, ethics |
| `05-write-venue` | `05-manuscript/write-venue/` | Journal selection / house style |
| `06-review-peer` | `06-review/review-peer/` | Other-paper peer review |
| `06-review-critique` | `06-review/review-critique/` | Self-audit / response machinery |

Translational / reader-study **design** mounts (when approved) belong under `03-research/` — A personal `clinical-translation` stays in MY-SKILLS; do not copy it here.

This package does **not** contain personal Aitor-format, de-AI, personal review/response style, 0RAD pipeline rules, radiology-stats lab policy, ethics form packs, or MATLAB preprocess scripts.

## Safety

- No PHI, no patient tables, no unpublished manuscripts.
- No ethics scans, phone numbers, or grant full texts.
- Do not treat this pack as a mounted Skill until A’s registry says so.

Default *external* candidates (not this repo): `Imbad0202/academic-research-skills`, `Aperivue/medsci-skills`. Both remain PROPOSED in A until approved.
