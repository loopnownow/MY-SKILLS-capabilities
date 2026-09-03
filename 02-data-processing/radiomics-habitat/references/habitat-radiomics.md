# Multi-parametric habitat radiomics (generic)

Two **mutually exclusive** paradigms. Do not blend single-timepoint fusion with longitudinal
delta clustering. Lab extractor / locked CLIs live in **A personal** — this file is the
scientific contract, not a vendor API.

| Paradigm | Role |
|---|---|
| Single timepoint, multi-sequence | Cluster voxels/superpixels in aligned sequence space; extract per-habitat × sequence features |
| Longitudinal delta | Cluster **baseline only**; propagate habitat masks to post; never re-cluster post |

Habitat IDs and downstream columns are **not** comparable across the two paradigms.

## Shared rules

- Align / register non-reference series onto the reference (ROI lives in reference space).
- Prefer a **cohort-level** habitat model so IDs are comparable across patients. Per-patient K
  makes IDs incomparable.
- Feature extraction is **IBSI-documented** (software + version + discretisation). Do not
  describe an undocumented engine as PyRadiomics or as a named commercial API unless the user
  supplied that engine.
- In-pipeline selection is train-only (near-zero variance → redundancy → penalised selector).
  Paper LASSO / nomogram / locked formula → `04-stats-models` / A personal modelling stack.

## Delta / longitudinal

- Cluster baseline image + baseline ROI only.
- Post habitats come from **mask propagation** (forward transform of baseline habitat masks).
- **Never re-cluster post.** Comments that say "delete propagation and reuse t1 masks" are wrong.
- Delta features: absolute and relative change (optional per-day rate). **No Z-score at the
  delta step** — scale later, train-only (`leakage-audit.md`).

## K selection

Combine elbow, silhouette, and a stability metric (e.g. consensus ARI). Pre-specify the rule
and the ARI floor. Do not pick K to maximise downstream AUC.

## Registration QC

- Multi-sequence, no ROI on moving series: soft mutual information is typical.
- Pre/post with ROIs: Dice + Hausdorff on the propagated mask is the honest gate.
