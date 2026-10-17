## 2026-10-17 -- A/B symmetry 07-response

- Moved `revise` / `tighten-response` / `response-tone-polisher` bodies from `06-review/` to `07-response/`.
- Fine IDs unchanged. A07 remains personal top layer in MY-SKILLS.

﻿## 2026-10-17 鈥?Absorb three fine ids into B domain folders

## 2026-10-17 — rename to MY-SKILLS-base

Repo / display / SKILL.md name: `MY-SKILLS-capabilities` → `MY-SKILLS-base` (source id `my-skills-base`). Local folder + GitHub remote renamed. Cache alias under mounts-cap remains `b/`.

Author: Aitor. Branch: `feat/absorb-three-to-b-20261017`. Does not merge to main until owner asks.

- **humanize** 鈫?`05-manuscript/humanize/` (from MedSci `skills/humanize/`; MIT). Personal A de-AI untouched.
- **retraction-watcher** 鈫?`03-research/retraction-watcher/` (from AIPOCH; MIT). Removed `cross-pack/aipoch/retraction-watcher/` pointer stub.
- **response-tone-polisher** 鈫?`06-review/response-tone-polisher/` (from AIPOCH; MIT). Removed `cross-pack/aipoch/response-tone-polisher/` pointer stub.
- README: `05-humanize` now in B; path-label rows added; AIPOCH stub wording revised.
- Companion A change: registry retarget `source: my-skills-base` (same fine ids stay MOUNTED).

## 2026-10-17 鈥?Fine-ID round 3: absorb three + model-eval synthesize

Author: Aitor. Branch: `feat/absorb-three-to-b-20261017`. Does not merge to main until owner asks.

- **verify-refs** 鈫?`03-research/verify-refs/` (from Scientific `skills/citation-management/`; MIT).
- **simulate-reviewers** 鈫?`06-review/simulate-reviewers/` (from Nature `skills/nature-reviewer/`; Apache-2.0).
- **tighten-response** 鈫?`06-review/tighten-response/` (from Nature `skills/nature-response/`; Apache-2.0).
- **model-evaluation** umbrella: `model-validation` archived鈫抈model-evaluation`; same folder `04-analysis/model-eval/` expanded for leakage gates.
- README path-label rows updated. Companion A: registry retarget + PROPOSED archives (`check-grant-proposal`, `scientific-critical-thinking`).

## 2026-09-14 鈥?clinic-research-design removed; Nature LICENSE note; Lee checklist

## 2026-09-22 鈥?Architecture Batch 1 (de-entity cross-pack)

- Pointerize all `cross-pack/{scientific,nature,aipoch}/*` folders: thin `SKILL.md` + `MODULE.md` pointing at A `mounts-cap/<pack>/鈥 SSOT. Removed duplicated MODULE bodies.
- Added `cross-pack/README.md`. Did **not** touch MedSci-native domain skills under `02`鈥揱06`.
- Companion A change: `feat/arch-batch1-cache-pointer-priority` (load_priority, 52 ceiling, journal data/rules split, Cache鈮燤ount鈮燗ctive docs).


## 2026-09-19 鈥?Align Intro v3 + 閫夊垔 list pointers

- `write-manuscript/radiology-writing/introduction.md`: six-element generic contract
- `write-manuscript` Hard rules: guideline definition, 10鈥?0 words, no TRIPOD in Intro, synthesize related studies
- `write-polish`: Introduction/Discussion lint table
- `lit-review`: Introduction evidence pack row contract
- `write-venue`: pointer to A blacklist / graylist (Frontiers) / whitelist-submitted


- Removed `cross-pack/aipoch/clinic-research-design/` (declined: documented scripts absent; eval reports untrusted).
- Nature cross-pack `LICENSE_NOTE.txt` 鈫?Apache-2.0 verified 2026-09-14 (third-party Yuan1z0825; not Springer Nature official).
- Added `06-review/review-peer/references/ai-public-data-imaging-checklist.md` (Lee WHE harvest C).


## 2026-09-13 鈥?CHG-20260913-001 (A registry v4 companion)

- Add MedSci new mounts: `03-research/intake-project`, `design-ai-benchmarking`, `architecture-zoo`, `fill-protocol`
- Add `cross-pack/{scientific,aipoch,nature}/` stubs for hybrid fine ids (not default B mounts; Nature license 闇€鏍稿疄)
- Append `external-principles.md` to `fig-plot`, `review-peer`, `review-response`
- OpenClaw intentionally absent from cross-pack

# Changelog

## 2026-09-03 鈥?clinical tables front (paired A change CHG-20260903-015)

Author: Aitor. Branch: `fix/audit-p1-20260903` (extends PR #6). Does not merge to main.

- `02-tables` **front** (`MODULE.md` + `SKILL.md`) is clinical Excel/CSV: headers, missingness, ID integrity, cohort columns (`training`/`test`; validation = external only; never Development set). Modelling 鈫?04. HIS login never here.
- Anthropic office/xlsx skill (financial models, 10-K sources, blue-input color conventions, `scripts/office`, `recalc.py`) moved to nested `02-data-processing/tables/xlsx-office/` with its own MODULE.md + thin SKILL.md. `LICENSE.txt` stays with that nested pack.
- Nested `impute/` kept. Env-only soft-coding from CHG-20260903-014 not undone. Links only: parent clinical QC; `xlsx-office/` for XML packing.
- Imaging data-availability `data.md` moved to `02-data-processing/imaging-io/data.md`; imaging-io MODULE points at it. Dealbreaker availability pointer follows. Dropped misplaced reporting `tables/checklists.md` (CLAIM/TRIPOD live in `05-write-reporting`).
- README `02-tables` mount blurb updated. Front MODULE has no financial-model color section.


## 2026-09-03 鈥?leftover P1 (paired A change CHG-20260903-014)

Author: Aitor. Branch: `fix/audit-p1-20260903`. Does not merge to main.

- `02-tables` nested `impute/`: CONFIG-on-top soft-coding in `export_u_impute.py` / `u_outlier_detection.py` (`os.environ` + `path/to/鈥 placeholders; no `F:\Paper\鈥 paths). Dropped leftover `python -m modules.u_impute` 0RAD layout docs; generic CLI kept. Anthropic `02-tables` MODULE body not rewritten.
- `02-imaging-qc`: deleted `notes/` (璇昏鏂?notes, not ROI QC). MODULE no longer links into `notes/`. Reader/mask QC refs under `references/` kept.
- `04-fig-plot`: leftover local STROBE / patient-flow / `draw_strobe_flow` pointers hand off to `04-fig-flow`. Live `radiology-stats` mentions replaced with `04-stats-guide` / `04-stats-models` / `04-model-eval` or A personal.
- Live old umbrella identities (`radiology-stats`, `radiology-deep-learning`, `radiology-radiogenomics`, `radiology-translation`, `radiology-data`, `radiology-writing`, `radiology-reporting`, `06_review` handoff, `manuscript-core/references/merged/鈥) swept to the 28 B ids or 鈥淎 personal鈥?
- Broken `nature-family-shape.md` links: write-manuscript `article-architecture.md` and fig-plot `nature-figure-spec.md` now point at `05-write-venue` `radiology-writing/nature-family-shape.md`.
- `05-write-venue`: venue templates / house style for writing, **not** 閫夊垔 (paired A: 閫夊垔 is 03 not 05). 閫夊垔 / where to submit 鈫?A `03_research` (journal-selection) / B `03-lit-search`. Folder kept.


## 2026-09-03 鈥?audit-fix (paired A change CHG-20260903-013)

Author: Aitor. Branch: `fix/audit-20260903`. Merged as PR #5 (`c9efb8d`).

### P0

- `02-imaging-qc`: rewritten as ROI / reader / mask QC. Bilingual paper-reader (trigger 璇昏鏂?/ 涓嫳瀵圭収) removed so this id cannot launch a translator.
- `05-write-manuscript`: generic IMRAD only. Stripped personal house format, de-AI lists, lab author/IRB defaults, and missing de-AI paths. Polish 鈫?`05-write-polish`; venue 鈫?`05-write-venue`.
- `02-radiomics-habitat`: kept IBSI / leakage / ROI guidance. Dropped vendor extractor API, lab Windows habitat/delta trees, and pipeline-rules "do not fork". Lab engine stays in A personal.
- `04-fig-plot`: renamed from figure-engine; domain `04_analysis`. STROBE / patient-flow (including `style.md`) moved to `04-fig-flow`. Broken STROBE links fixed.
- `06-review-peer` = other-paper only. `06-review-critique` = self-audit (dropped 鍥炲瀹＄浜?trigger). `06-review-response` keeps point-by-point; peer MODULE does not own mode-3. Personal review voice stripped.
- `02-tables` / nested `impute/`: nested OK. Removed lab imputer path coupling and `domain: 04_analysis`. Generic impute CLI/docs kept. `LICENSE.txt` Anthropic attribution kept.

### P1

- Thin per-id `SKILL.md` front-matters to existing `MODULE.md` (bodies not duplicated). True stubs labelled `status: stub`.
- Silent stubs `02-imaging-io`, `02-pictures`, `04-model-eval`: one-page workflows (not stubs).
- True stubs: `02-fmri`, `03-lit-fulltext`, `03-design-protocol`, `03-design-grant`.
- YAML `name` / `domain` / `owner` aligned with folder ids.
- `04-stats-guide` no longer teaches power / Bayesian / `assumption_checks.py` (those packs exist).
- `03-frontier-ideate` no longer points at hypothesize files or missing grant files.
- `03-design-experiment`: no Voice B 绔嬮」 / grant skeleton.
- `03-lit-search` trigger: dropped 鍏ㄦ枃 (that is `03-lit-fulltext`).
- Jinshan lab ethics defaults removed from write-manuscript ethics.
- `write-polish/style-guardrails.md` no longer points at a missing A corpus phrase bank.
- Root README ascii tree and `03-research/README.md` aligned with the 28-id table.
- Empty leftover `05-manuscript/write-manuscript/radiology-polishing/` removed.
- Live strings `figure-engine`, `05-writing-generic`, `02-generic-docs`, `04-stats-generic`, `04-figure-engine` swept as live mounts.

### P2

- This changelog cites CHG-20260903-013.
- Root `SKILL.md` / `README.md` still list 28 ids and still exclude `04-explainability` / `05-humanize`.
