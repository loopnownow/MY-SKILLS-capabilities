> **Mount split:** in-pipeline filter/selection for habitat/delta **preparation** stays here.
> Paper-level modelling, nomogram, and locked formulas belong in `04-stats-models` /
> `04-model-eval` (lab stats policy stays in A). Do not treat this file as lab pipeline rules.

# Feature selection, modelling and the signature

**Every data-dependent step is fit inside training only.** Selection on the whole cohort is
the most common radiomics leak.

## Two stacks (do not mix)

| Stack | What it is |
|---|---|
| **In-pipeline filter** | After radiomics flatten: near-zero variance → redundancy → penalised selector on **train** |
| **Paper model** | Clinical+radiomics modelling, curves, nomogram, lock/apply → `04-analysis` / A personal |

## In-pipeline selection (training split after scaler.fit(train))

1. Near-zero variance (pre-specified threshold).
2. Pearson redundancy (pre-specified `|r|`); keep the member more correlated with `y`.
3. Supervised selector (commonly LassoCV). Name the method actually used.

There is **no ICC step here**. If ICC is required, run it before this stack on
training/reproducibility scans only (`02-imaging-qc`).

> Wrong: rank features on the full dataset, then cross-validate the chosen set.
> Right: re-run selection inside each training fold; report selection stability.

## Paper modelling

Rad-score, nomogram, ROC/DCA/calibration, NRI, or a locked formula belong with analysis
packs — not this preparation skill. Match the model to n/EPV: penalised regression for
small n; tree ensembles when justified and sample size allows.
