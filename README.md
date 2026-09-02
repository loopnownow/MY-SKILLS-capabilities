# MY-SKILLS-capabilities

Mountable **generic** capability package for [loopnownow/MY-SKILLS](https://github.com/loopnownow/MY-SKILLS) (framework A).

A = orchestrator + personal lab layer. **B = reusable skills only.**
Nothing in this repo is auto-mounted. Framework A `registry.yaml` stays `mounts: []` until the user explicitly approves a mount.

## How A mounts B

1. In MY-SKILLS, `01_skill-discovery-integration` evaluates a candidate and writes an `interface.yaml` contract.
2. The user explicitly approves (silence is not approval).
3. A records the id in `core/01_skill-discovery-integration/registry.yaml` `mounts:` as `MOUNTED` and lists it in `core/MOUNTED_SKILLS.md`.
4. Domain skills call **ids** below, not old `bundles/` paths.

Until step 3, A keeps local generic copies marked in `EXTERNALIZATION_CANDIDATES.md`.

## Mount points (ids)

| Id | Use |
|---|---|
| `02-xlsx` | Excel/CSV automation |
| `02-imaging-qc` | Imaging preprocessing QC (no personal MATLAB scripts) |
| `02-radiomics-habitat` | Radiomics/habitat **preparation** (paper modelling → A `04_analysis`) |
| `02-impute` | Missing/outlier processing |
| `02-generic-docs` | Generic imaging/data notes |
| `03-literature` | Literature / sources / journals / public datasets |
| `03-design` | Study design / validation / blueprints |
| `03-frontier` | Frontier themes / idea-to-question |
| `04-stats-generic` | Generic statistics encyclopaedia |
| `04-figure-engine` | Figure generation (including journal-family visual style / Nature figure spec) |
| `05-writing-generic` | Generic writing, reporting, citation, ethics, journal house style |
| `06-review-generic` | Generic prereview / response machinery |

This package does **not** contain personal Aitor-format, de-AI, personal review/response style, 0RAD pipeline rules, radiology-stats lab policy, or MATLAB preprocess scripts.

## Safety

- No PHI, no patient tables, no unpublished manuscripts.
- No ethics scans, phone numbers, or grant full texts.
- Do not treat this pack as a mounted Skill until A’s registry says so.

Default *external* candidates (not this repo): `Imbad0202/academic-research-skills` (default), `Aperivue/medsci-skills` (backup). Both remain PROPOSED in A until approved.
