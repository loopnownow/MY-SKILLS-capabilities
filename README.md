# MY-SKILLS-capabilities

Mountable **generic** capability package for [loopnownow/MY-SKILLS](https://github.com/loopnownow/MY-SKILLS) (framework A).

A = orchestrator + personal lab layer. **B = reusable skills only.**
Nothing in this repo is auto-mounted. Framework A `registry.yaml` stays `mounts: []` until the user explicitly approves a mount.

Layout is classified by A domain (unlimited depth inside each pack):

```
02-data-processing/   xlsx, imaging-qc, radiomics-habitat, impute, generic-docs
03-research/          literature, design, frontier
04-analysis/          stats-generic, figure-engine
05-manuscript/        writing-generic
06-review/            review-generic
```

## How A mounts B

1. In MY-SKILLS, `01_skill-discovery-integration` evaluates a candidate and writes an `interface.yaml` contract.
2. The user explicitly approves (silence is not approval).
3. A records the id in `01_skill-discovery-integration/registry.yaml` `mounts:` as `MOUNTED` and lists it in `MOUNTED_SKILLS.md`.
4. Domain skills call **ids** below, not old `bundles/` paths.

Until step 3, A may keep local generic copies marked in `EXTERNALIZATION_CANDIDATES.md`. 05 writing-generic and 06 review-generic are B-only. de-AI returned to A `05_manuscript/personal/` (2026-09-02).

## Mount points (ids → paths)

| Id | Path | Use |
|---|---|---|
| `02-xlsx` | `02-data-processing/xlsx/` | Excel/CSV automation |
| `02-imaging-qc` | `02-data-processing/imaging-qc/` | Imaging preprocessing QC (no personal MATLAB scripts) |
| `02-radiomics-habitat` | `02-data-processing/radiomics-habitat/` | Radiomics/habitat **preparation** (paper modelling → A `04_analysis`) |
| `02-impute` | `02-data-processing/impute/` | Missing/outlier processing |
| `02-generic-docs` | `02-data-processing/generic-docs/` | Generic imaging/data notes |
| `03-literature` | `03-research/literature/` | Literature / sources / journals / public datasets |
| `03-design` | `03-research/design/` | Study design / validation / blueprints |
| `03-frontier` | `03-research/frontier/` | Frontier themes / idea-to-question |
| `04-stats-generic` | `04-analysis/stats-generic/` | Generic statistics encyclopaedia |
| `04-figure-engine` | `04-analysis/figure-engine/` | Figure generation (including journal-family visual style / Nature figure spec) |
| `05-writing-generic` | `05-manuscript/writing-generic/` | Generic writing, reporting, citation, ethics, journal house style |
| `06-review-generic` | `06-review/review-generic/` | Generic prereview / response machinery |

Translational / reader-study **design** mounts (when approved) belong under `03-research/` — A personal `clinical-translation` stays in MY-SKILLS; do not copy it here.

This package does **not** contain personal Aitor-format, de-AI, personal review/response style, 0RAD pipeline rules, radiology-stats lab policy, ethics form packs, or MATLAB preprocess scripts.

## Safety

- No PHI, no patient tables, no unpublished manuscripts.
- No ethics scans, phone numbers, or grant full texts.
- Do not treat this pack as a mounted Skill until A’s registry says so.

Default *external* candidates (not this repo): `Imbad0202/academic-research-skills` (default), `Aperivue/medsci-skills` (backup). Both remain PROPOSED in A until approved.
