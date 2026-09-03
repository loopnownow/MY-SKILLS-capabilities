# Feature extraction (IBSI, generic)

Produce a documented, versioned feature matrix another lab could regenerate.

**Engine:** whatever the user named (open-source IBSI toolkit, in-house lab extractor in A
personal, or a commercial library). Record software + version. Do **not** invent a vendor API
or describe the engine as PyRadiomics unless that is what was used.

## Discretisation (IBSI; complementary)

Common complementary pair (report both if both were run):

- **Fixed bin number (FBN)** — e.g. 32 bins (typical MRI / already-normalised).
- **Fixed bin size (FBS)** — e.g. width = intensity range / 16 (typical HU-windowed CT).

They are complementary; do not collapse to "pick binWidth or binCount."

## Feature families (IBSI nomenclature)

| Family | Captures |
|---|---|
| First-order / intensity | Histogram statistics (mean, entropy, skewness, kurtosis) |
| Shape (2D/3D) | Volume, surface area, sphericity, elongation |
| GLCM | Gray-level co-occurrence |
| GLRLM / GLSZM / GLDM / NGTDM | Run-length, size-zone, dependence, neighbouring-tone |
| Filtered (LoG / wavelet) | Same families on transformed images |

## Aggregation and naming

- 3D extraction inside each habitat / ROI mask; skip or error below a pre-specified voxel floor.
- Rows = patients after flatten; columns = stable, documented names.
- Version the matrix; record which paradigm (single-timepoint vs delta) produced it.

## Delta / longitudinal

When the question is **change**:

- Identical discretisation at pre and post.
- Cluster baseline only; propagate masks; never re-cluster post (`habitat-radiomics.md`).
- Absolute `f_post - f_pre`, relative percent, optional per-day rate. No Z-score here.
- Selection stays inside training (`selection-modelling.md`).

## Test–retest / phantom

Drop low-repeatability features **before** selection, training subset only. Segmentation
reproducibility is `02-imaging-qc` `references/reproducibility-qc.md`. Reporting "not
performed, and why" is stronger than silence (→ `05-write-reporting`).

## Reporting sentence (fill with supplied facts)

*"For each ROI/habitat, IBSI-named features were extracted with [software vX] using [FBN /
FBS settings] after [resample]. Software version and discretisation are recorded."*
