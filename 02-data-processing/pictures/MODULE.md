---
name: "pictures"
domain: "02_data-processing"
trigger: ["tiff", "tif", "png", "jpg", "jpeg", "pdf图", "切片图"]
outputs: ["analysis_ready_pictures"]
owner: "02-data-processing/pictures/MODULE.md"
---

# Pictures (TIFF / PNG / JPG / PDF-as-image)

Generic 2D picture handling: pathology slides, screenshots, scanned figures, PDF pages as images.
Not CT/MRI volumes (`02-imaging-io`) and not fMRI (`02-fmri`). Personal MATLAB preprocess stays in A.

## Workflow

1. **Identify** type (TIFF pyramid / PNG / JPEG / PDF page raster).
2. **Load** without dropping bit depth; record colourspace and dpi.
3. **De-identify** — burn no names, dates, or accession numbers into pixels.
4. **Normalise** only if asked (dpi, crop, rotate). Do not invent scale bars.
5. **Export** an analysis-ready raster + a short QC note (size, dpi, colourspace).
6. **Hand off** publication panels to `04-fig-plot`. Volumes stay in `02-imaging-io`.
