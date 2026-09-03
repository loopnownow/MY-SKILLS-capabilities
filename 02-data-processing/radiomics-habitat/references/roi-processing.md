# ROI expansion and image–ROI matching (generic)

## Delta habitats: 1 pre + 1 post, both with ROI

Each patient has exactly **one pre and one post**, and **both** timepoints need an ROI.

- Cluster **baseline only** (pre image + pre ROI).
- Post habitat masks come from **propagation** (forward transform of baseline habitat masks
  onto registered post space).
- **Never re-cluster post.**

A minimum-voxel floor before extraction should be a config value, not a magic number in a
function body.

## Propagation is the source of truth

Post habitat identity must stay anatomically corresponding to baseline IDs. Reusing t1 masks
as t2 without a transform is wrong. Delta features assume pre/post habitat indices match
because of propagation.

## ROI expansion (dilation)

Expand in **physical millimetres**, not a fixed voxel count, so spacing differences do not
silently change the margin.

Config at the top of the script:

- Expansion margin in mm
- Clip to image bounds and/or an anatomical mask
- Spacing-aware structuring element
- Output name that does not overwrite the original ROI

## Image–ROI file matching

Heterogeneous folders need an explicit matching rule (id in filename, sidecar CSV, DICOM
references). Log unmatched pairs; do not silently drop them. Lab matchers stay in A personal.
