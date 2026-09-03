---
name: "imaging-io"
domain: "02_data-processing"
trigger: ["DICOM", "NIfTI", "nii", "读图", "格式转换"]
outputs: ["volume_or_series"]
---

# CT/MRI I/O (DICOM / NIfTI / NII)

Read, convert, and organise volumetric series. QC / ROI / reader protocol lives in `imaging-qc/`.

Personal MATLAB preprocess stays in A. Backup: Scientific `pydicom` / `bids` / `imaging-data-commons`; MedSci `preprocess-imaging`.
