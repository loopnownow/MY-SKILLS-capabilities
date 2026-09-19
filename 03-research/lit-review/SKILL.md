---
name: "lit-review"
domain: "03_research"
trigger: ["综述", "systematic review", "近三年证据", "Introduction evidence pack"]
outputs: ["evidence_map", "intro_evidence_pack"]
owner: "03-research/lit-review/MODULE.md"
---

# Literature review

Synthesize a seed evidence map. Not a live PubMed dump. Fresh search still required before citation lists.

## Introduction evidence pack

Used when 05 raises Introduction cards (`guideline_definition`, `missing_prior_result`, `related_work_appraisal`, `scarcity_check`). Return rows, not prose:

`Claim | Source (PMID/DOI) | Class | Design · n · effect | Strength | Weakness relevant to the study | Level (L1–L3) | Intro or Discussion | Keep?`

Class: `guideline`, `mri_accuracy` (or the modality's accuracy class), `radiomics_endpoint`, `habitat_or_nearest`, `background`.

- Guideline: the latest edition of the body that defines the endpoint or decision. Confirm no newer edition exists. Record body, year, where the definition sits, the recommendation and its level of evidence, and one open issue the guideline states. Full text (L3).
- Prior results: one source per class where it exists. Include a weaker or limited result if one exists.
- Appraisal: the strength, and the weakness relevant to the study (endpoint definition, validation type, region of interest, comparator, sample).
- Scarcity: a search log with PubMed plus one other source, query strings, dates, counts screened, and the closest studies found. Report what was found; never assert absence.
- Data boundary: send only topic terms to external services, never unpublished results.
- Candidates only; 05 decides. Never invent a PMID, DOI, or number.
