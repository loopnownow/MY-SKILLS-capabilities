# Preprocessing to IBSI standard

Every preprocessing choice changes the features. Fix them a priori, apply uniformly, and report
to IBSI so the features are reproducible. Lab-locked `PREPROC` blocks live in A personal.

## Resampling (voxel size)

- **Target spacing:** typically isotropic 1×1×1 mm unless the user locked another grid.
- **Image interpolator:** B-spline (order 3–5). **Mask interpolator:** nearest-neighbour.
- **Default pad:** 0 (not a pixel-type enum accidentally used as a fill value).

## Intensity normalisation

| Modality | Typical handling (state what you actually did) |
|---|---|
| CT | Often no N4; clip to a pre-specified HU window then scale |
| MRI | N4 + z-score (or a named alternative) |
| ADC | Already quantitative — do not silently z-score |
| PET | SUV; state the normalisation |

Normalisation is fit **per-image / per-mask**, never from test-cohort statistics.

## Gray-level discretisation

Report FBN and/or FBS settings (`feature-extraction.md`). Complementary configs are fine;
collapsing to one undocumented binning is not.

## Mandatory IBSI reporting

- Interpolation + resampled spacing; image vs mask interpolators; pad value
- Intensity normalisation / re-segmentation range
- Discretisation (FBN and/or FBS)
- Filters + parameters
- Feature aggregation (3D, ROI/habitat masks)
- Software + version + an honest IBSI statement (compliant / not tested)

## Reporting sentence

*"Images were resampled to [spacing] (B-spline; masks nearest-neighbour). [Modality-specific
normalisation]. Features used [discretisation]. Software [name vX]."*
