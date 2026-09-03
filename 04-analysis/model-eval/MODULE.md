---
name: "model-eval"
domain: "04_analysis"
trigger: ["校准", "DCA", "外验证", "模型评价"]
outputs: ["eval_report"]
owner: "04-analysis/model-eval/MODULE.md"
---

# Model evaluation (calibration / DCA / external validation)

Not test selection (`04-stats-guide`) and not model fitting (`04-stats-models`).
Lab 0RAD / DeLong / Cox policy stays in A `04_analysis/personal/`.

## Workflow

1. **Confirm the split is locked** — patient-level; test untouched during fitting.
2. **Discrimination** — AUC (or C-index) with 95% CI on each named set. Do not invent CIs.
3. **Calibration** — plot + slope/intercept or a named calibration metric when supplied.
4. **Clinical utility** — decision-curve analysis **only** if the paper claims decision support.
5. **External / temporal / geographic** validation when generalisability is claimed; otherwise bound the claim.
6. **Plots** → `04-fig-plot`. Reporting checklists → `05-write-reporting`.

Backup: MedSci `model-evaluation` / `model-validation`.
