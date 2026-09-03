---
name: "review-critique"
domain: "06_review"
trigger: ["自审", "投稿前预审", "找洞"]
outputs: ["blocking_major_minor"]
owner: "06-review/review-critique/MODULE.md"
---

# trigger is documentation only; not independently discoverable.

# Self-audit / pre-submission

Find holes in **the user's own** manuscript before submission. Other-paper review is
`06-review-peer`. Point-by-point **response** is `06-review-response` — this pack does not
own 回复审稿人.

Personal review voice stays in A.

## When to open

| File | Open when |
|---|---|
| [pre-submission.md](pre-submission.md) | Simulated reviewer critique of own draft |
| [pre-submission-hard-gates.md](pre-submission-hard-gates.md) | Final hard-gate audit |
| [review_checklist_export.md](review_checklist_export.md) | Exportable checklist |

## Workflow

1. Confirm venue/study type. Do not fill title-page ethics/author fields here.
2. Scan leakage, split, validation, overclaim, reporting gaps.
3. Output Blocking / Major / Minor with a concrete fix each.
4. Do not invent rescue experiments. Prose rewrite → `05-write-manuscript`.
