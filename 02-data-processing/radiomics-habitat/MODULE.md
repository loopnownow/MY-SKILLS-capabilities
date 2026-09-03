---
name: "radiomics-habitat"
domain: "02_data-processing"
trigger: ["habitat", "radiomics", "IBSI", "ROI expansion"]
inputs: ["config", "images", "masks"]
outputs: ["feature_table", "qc_notes"]
tools: ["Python", "SimpleITK"]
quality_control: "train-only selection; never re-cluster post; IBSI discretisation reported"
owner: "02-data-processing/radiomics-habitat/MODULE.md"
---

# trigger is documentation only; not independently discoverable.

# Radiomics / habitat **preparation**

Generic guidance for IBSI-compliant feature extraction, habitat clustering, ROI handling, and
leakage control **before** paper-level modelling.

**Lab engine, vendor API, and locked pipeline trees live in A personal.** Do not vendor a lab
code tree, a private API, or Windows lab paths into this pack. Point at A when the user needs
the in-house extractor.

Paper-level LASSO / nomogram / ROC / DCA / calibration → `04-stats-models` / `04-model-eval`.
Mask / reader QC → `02-imaging-qc`.

## Non-negotiable conventions (generic)

1. **Soft-coded config at the top** — paths, margins (mm), discretisation, K range, seeds.
2. **Modular stages** — load, preprocess, register, extract, select; each runnable alone.
3. **Train-only data-dependent steps** — scaler, imputation, feature selection, habitat centroids.
4. **Never re-cluster post** in longitudinal / delta habitats; propagate baseline masks.
5. **Do not invent** IBSI compliance, ICC, or software versions the user did not supply.

## Domain references

| Domain | When | Reference |
|---|---|---|
| Habitat (single timepoint vs delta) | Multi-sequence clustering or pre/post change | [references/habitat-radiomics.md](references/habitat-radiomics.md) |
| IBSI preprocess | Resample, intensity, discretisation | [references/preprocessing-ibsi.md](references/preprocessing-ibsi.md) |
| Feature extraction | Feature families, matrix versioning | [references/feature-extraction.md](references/feature-extraction.md) |
| Leakage audit | Patient-level split; fit-on-training | [references/leakage-audit.md](references/leakage-audit.md) |
| ROI processing | Dilation in mm, image–ROI matching | [references/roi-processing.md](references/roi-processing.md) |
| Selection | Train-only filter vs paper modelling | [references/selection-modelling.md](references/selection-modelling.md) |
| Clinical ML (generic) | Table1 / curves / nomogram **shape** | [references/clinical-ml-pipeline.md](references/clinical-ml-pipeline.md) |
| Longitudinal foundation models | RECIST time series | [references/timesfm-lung.md](references/timesfm-lung.md) |

## Typical workflow

1. Confirm image/mask QC already passed (`02-imaging-qc`).
2. Choose single-timepoint habitat **or** delta — do not blend clustering schemes.
3. Lock IBSI preprocess + discretisation *a priori* and report them.
4. Extract a versioned feature matrix; drop low-ICC features on the **training** reproducibility subset.
5. Leakage audit before any paper model. Hand modelling to `04-analysis`.
