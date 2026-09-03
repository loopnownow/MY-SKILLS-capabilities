---
name: "pictures"
domain: "02_data-processing"
trigger: ["tiff", "tif", "png", "jpg", "jpeg", "pdf图", "切片图"]
outputs: ["analysis_ready_pictures"]
---

# Pictures (TIFF / PNG / JPG / PDF-as-image)

Generic 2D picture handling: pathology slides, screenshots, scanned figures, PDF pages as images.

Not CT/MRI volumes (`imaging/`) and not fMRI (`fmri/`). Personal MATLAB preprocess stays in A.
