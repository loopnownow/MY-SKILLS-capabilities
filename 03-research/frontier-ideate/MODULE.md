---
name: "frontier-ideate"
domain: "03_research"
trigger: ["frontier", "选题", "前沿"]
inputs: ["topic", "year_window"]
outputs: ["evidence_gaps", "journal_fit_notes"]
tools: ["pubmed_pages"]
quality_control: "do not invent PMID/DOI"
owner: "03-research/frontier-ideate/MODULE.md"
---

# trigger is documentation only; not independently discoverable.

# Frontier Directions & Evidence Layer

Use this skill to turn "what's hot in imaging AI" into **a publishable question matched to the
user's data** — and to expose the **publication-pattern evidence** behind each recommendation.
It is the strategic front of the chain: before designing (→ `03-design-experiment`), decide *what is
worth doing and likely to be accepted at a high-impact venue*.

## Core stance

- **Frontier ≠ feasible for you.** A direction is only useful if the user's data can actually
  carry it. Always test a trend against their disease, modality, n, centers, labels, and omics.
- **Evidence over vibes.** Recommendations are grounded in *how top journals actually publish*
  — design patterns, validation expectations, and what each venue rewards — not in slogans.
- **Patterns are durable; specific papers are not.** This skill encodes **publication-pattern
  heuristics** (the kinds of studies that get into each journal and the methodological bar
  they meet). It does **not** ship a fixed citation list. Concrete recent papers must be
  retrieved and verified **live** (→ `03-lit-search`); never cite a PMID/DOI from memory.
- **Separate hot from suitable.** Name directions that are trendy but a poor fit for the data,
  and say why — steering away from a wrong direction is as valuable as suggesting a right one.
- **Bound novelty claims.** "First/novel" is a liability without a literature check. Frame
  innovation as a specific, defensible gap, not a superlative.
- **Integrity.** Never fabricate references, effect sizes, or "recent studies show…" claims.
  Mark anything that needs same-day verification.

## When to use

- "Give me frontier directions for [disease/modality] I can publish in the next 1–2 years."
- "找近三年的前沿方向和创新点" / "结合我的数据找创新点。"
- "Is [foundation models / self-supervised / VLM / multimodal / federated] right for my data?"
- "What's the evidence/publication-pattern basis for this recommendation?" / "有什么文献依据？"
- "Which top journals publish this kind of study, and what do they demand?"

## When to open extra files

| File | Open when |
|---|---|
| [references/frontier-themes.md](references/frontier-themes.md) | Surveying current themes (foundation models, SSL, VLM, multimodal fusion, longitudinal, weak/semi-supervision, domain adaptation, federated, generative, radiogenomics) and their data prerequisites |
| [references/ai-radiogenomics-frontier-map.md](references/ai-radiogenomics-frontier-map.md) | The user asks for radiology AI/radiogenomics directions over the next 12-24 months, or needs to choose among foundation models, SSL, VLM, multimodal fusion, federated learning, UQ/XAI, and radiogenomics |

## Workflow

1. **Read the data** — disease, modality, n, centers, labels, follow-up, omics availability
   (reuse the inventory from `03-design-experiment` if present).
2. **Scan themes** (frontier-themes.md) and **filter by fit** — for each candidate direction,
   state the data prerequisites and whether the user meets them. Reject poor fits explicitly.
3. **For AI/radiogenomics strategy**, open `ai-radiogenomics-frontier-map.md` and judge the
   idea against generalisability, supervision cost, multimodal fusion, trustworthy inference,
   external validation, and clinical-value evidence.
4. **Ground in evidence** (hand off to `03-frontier-hypothesize`) — for each surviving direction, state the
   publication pattern (what kind of study, what validation, which venues) and the
   methodological bar it must clear. Flag every concrete claim that needs **live verification**.
5. **Convert to questions** (hand off to `03-frontier-hypothesize`) — turn the best 2–4 directions into specific
   research questions with endpoint, comparator, and the minimum evidence to be competitive.
6. **Trigger live search** — hand the chosen direction to `03-lit-search` to retrieve and
   verify current seed papers (PMID/DOI) and confirm the gap is still open.
7. **Return** a ranked shortlist: direction → fit → evidence pattern → executable question →
   target-venue tier → what to verify now.

## Output contract

1. **`Data-fit summary`** — the inventory and the binding constraint, reused or restated.
2. **`Frontier shortlist`** — ranked directions, each with: fit (yes/conditional/no + reason),
   the publication-pattern evidence, and the methodological bar.
3. **`Executable questions`** — 2–4 concrete questions (endpoint, comparator, minimum evidence),
   each mapped to a candidate venue tier (→ `05-write-venue`).
4. **`Hot-but-unsuitable`** — trendy directions to avoid for this data, with the reason.
5. **`Verify now`** — the explicit list of claims/papers to confirm via live search today
   (handed to `03-lit-search`); nothing here is presented as already-verified.


## Quality bar

A good frontier read sounds like a mentor who reviews for these journals: it knows what each
venue keeps publishing and why, matches the trend to the user's real data, names the directions
that are fashionable but wrong for them, and never invents a citation to sound current.

## Handoffs

- Turn the chosen direction into a full design → `03-design-experiment`.
- Retrieve & verify current seed literature / confirm the gap → `03-lit-search`.
- Which journal tier the question targets → `05-write-venue`.
- Method-specific feasibility → `02-radiomics-habitat` / `03-design-experiment`.
- Citation export of verified seeds → `03-lit-cite`.
- Own funding proposal → `03-design-grant` / A personal Voice A/B. Do not copy grant files here.
- This skill advises on research strategy; specific recent claims must be verified live.
