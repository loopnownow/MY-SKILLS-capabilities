---
name: "exploratory-data-analysis"
label_cn: "EDA(fail-closed安全设计)"
mount_status: "cross_package_pointer"
source_package: "Scientific"
description: "POINTER only — entity lives in A mounts-cap cache (mounts-cap/scientific/skills/exploratory-data-analysis/). Do not duplicate."
owner: "cross-pack/scientific/exploratory-data-analysis/ — pointer stub"
---

# EDA(fail-closed安全设计)

**POINTER — do not duplicate the skill body here.**

| | |
|---|---|
| Entity (SSOT) | A's local cache: `mounts-cap/scientific/skills/exploratory-data-analysis/` |
| Fetch | `python mounts-cap/fetch.py ensure --id <fine-id>` in MY-SKILLS |
| Registry | A `01_skill-discovery-integration/registry.yaml` (`stub_in_b: cross-pack/scientific/exploratory-data-analysis/`) |
| This folder | Thin stub only (`SKILL.md` + `MODULE.md` note) |

Capability bytes belong in the external package cache, not in B `cross-pack/`.
