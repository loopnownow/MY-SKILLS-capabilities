# Changelog

## 2026-09-03 — audit-fix (paired A change CHG-20260903-013)

Author: Aitor. Branch: `fix/audit-20260903`. Does not merge to main.

### P0

- `02-imaging-qc`: rewritten as ROI / reader / mask QC. Bilingual paper-reader (trigger 读论文 / 中英对照) removed so this id cannot launch a translator.
- `05-write-manuscript`: generic IMRAD only. Stripped personal house format, de-AI lists, lab author/IRB defaults, and missing de-AI paths. Polish → `05-write-polish`; venue → `05-write-venue`.
- `02-radiomics-habitat`: kept IBSI / leakage / ROI guidance. Dropped vendor extractor API, lab Windows habitat/delta trees, and pipeline-rules "do not fork". Lab engine stays in A personal.
- `04-fig-plot`: renamed from figure-engine; domain `04_analysis`. STROBE / patient-flow (including `style.md`) moved to `04-fig-flow`. Broken STROBE links fixed.
- `06-review-peer` = other-paper only. `06-review-critique` = self-audit (dropped 回复审稿人 trigger). `06-review-response` keeps point-by-point; peer MODULE does not own mode-3. Personal review voice stripped.
- `02-tables` / nested `impute/`: nested OK. Removed lab imputer path coupling and `domain: 04_analysis`. Generic impute CLI/docs kept. `LICENSE.txt` Anthropic attribution kept.

### P1

- Thin per-id `SKILL.md` front-matters to existing `MODULE.md` (bodies not duplicated). True stubs labelled `status: stub`.
- Silent stubs `02-imaging-io`, `02-pictures`, `04-model-eval`: one-page workflows (not stubs).
- True stubs: `02-fmri`, `03-lit-fulltext`, `03-design-protocol`, `03-design-grant`.
- YAML `name` / `domain` / `owner` aligned with folder ids.
- `04-stats-guide` no longer teaches power / Bayesian / `assumption_checks.py` (those packs exist).
- `03-frontier-ideate` no longer points at hypothesize files or missing grant files.
- `03-design-experiment`: no Voice B 立项 / grant skeleton.
- `03-lit-search` trigger: dropped 全文 (that is `03-lit-fulltext`).
- Jinshan lab ethics defaults removed from write-manuscript ethics.
- `write-polish/style-guardrails.md` no longer points at a missing A corpus phrase bank.
- Root README ascii tree and `03-research/README.md` aligned with the 28-id table.
- Empty leftover `05-manuscript/write-manuscript/radiology-polishing/` removed.
- Live strings `figure-engine`, `05-writing-generic`, `02-generic-docs`, `04-stats-generic`, `04-figure-engine` swept as live mounts.

### P2

- This changelog cites CHG-20260903-013.
- Root `SKILL.md` / `README.md` still list 28 ids and still exclude `04-explainability` / `05-humanize`.
