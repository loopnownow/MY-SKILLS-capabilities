# Radiomics leakage audit

The checklist reviewers (and METRICS/RQS) use. Each item is pass/fail with a fix.

## Fit-on-training-only (required behaviour)

- Split **patient-level** rows first.
- Scaler **fit on train only**, transform test.
- Feature selection **train only**. Test columns are sliced with the selected names afterwards.
- Delta absolute/relative change is computed **without** Z-score; scaling happens later on train.

Persist the fitted scaler if a frozen apply-on-new-cohort path is required. Do not refit on
validation/test.

ICC filtering is **not** implied by LASSO. Run a dedicated ICC step on the training
reproducibility subset (`02-imaging-qc`) before selection.

## Partition hygiene

- [ ] Split at the **patient** level (not slice/lesion/habitat row).
- [ ] No patient's lesions/slices/sequences/phases/timepoints span train and test.
- [ ] Test set untouched until final evaluation.

## Fit-on-training-only

- [ ] Feature selection inside CV/training folds, not on the full cohort.
- [ ] Normalisation / standardisation fit on training, applied to test.
- [ ] Missing-value imputation fit on training.
- [ ] Harmonisation (ComBat) fit on training, applied to test.
- [ ] Augmentation never crosses the split.

## Tuning hygiene

- [ ] Hyperparameters tuned by nested CV or a separate validation set, not on test.
- [ ] Operating point chosen on training/derivation, not on test.
- [ ] No early stopping / model selection on the test set.

## Reproducibility / stability

- [ ] Low-ICC features removed before modelling, training subset only.
- [ ] Discretisation fixed and reported (IBSI).
- [ ] Software + version recorded.

## Evaluation honesty

- [ ] Real prevalence reported.
- [ ] Discrimination **and** calibration **and** decision-curve when clinical utility is claimed.
- [ ] CIs everywhere; external/temporal validation stated honestly.

## Output

```
Leakage audit:
  Partition:        PASS / FAIL — [detail + fix]
  Fit-on-training:  PASS / FAIL — [detail + fix]
  Tuning:           PASS / FAIL — [detail + fix]
  Reproducibility:  PASS / FAIL — [detail + fix]
  Evaluation:       PASS / FAIL — [detail + fix]
Overall: [Blocker(s) / Should-fix / Clean]
```

Paper-level modelling → `04-stats-models` / `04-model-eval` / A personal stats policy.
Reporting-guideline mapping → `05-write-reporting`.
