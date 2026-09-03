# Clinical + radiomics ML pipeline (generic)

## Separator

| Job | Where |
|---|---|
| Habitat / delta **in-pipeline** selection | This pack (`selection-modelling.md`) |
| Paper LASSO, nomogram, ROC/DCA/calibration, NRI, ICC | `04-stats-models` / `04-model-eval` / A personal |

Do not treat a sketchy utility LASSO as the paper stats library.

## Reference module set (shape, not a vendored tree)

When building a clinical+radiomics prediction pipeline, keep modules independently runnable:

| Module | Purpose |
|---|---|
| config | Paths, column names, split, seeds, plot style |
| clin_select | Clinical variable selection |
| correlation | Feature correlation |
| impute / outlier | Missing values / outliers (`02-tables/impute`) |
| icc | Feature reproducibility |
| radiomics | Feature handling / selection |
| curves (ROC / DCA / calibration) | Evaluation plots → also `04-fig-plot` |
| nomogram / NRI | Paper model outputs |
| results report | Aggregate tables/figures |

Lab-locked pipeline rules and workspace conventions stay in **A personal**. Do not fork them
into this pack.

## Port caveats (R → Python)

Flag indexing (1 vs 0), factor handling, `rms`/`glmnet` vs Python equivalents, RNG
non-portability, and DCA/calibration library differences. Do not claim numerical identity
across languages from a shared seed.
