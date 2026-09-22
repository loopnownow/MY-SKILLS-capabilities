---
name: "nature-academic-search"
label_cn: "严格他引审计(基金/职称场景)"
mount_status: "cross_package_pointer"
source_package: "Nature"
description: "POINTER only — entity lives in A mounts-cap cache (mounts-cap/nature/skills/nature-academic-search/). Do not duplicate."
owner: "cross-pack/nature/nature-academic-search/ — pointer stub"
---

# 严格他引审计(基金/职称场景)

**POINTER — do not duplicate the skill body here.**

| | |
|---|---|
| Entity (SSOT) | A's local cache: `mounts-cap/nature/skills/nature-academic-search/` |
| Fetch | `python mounts-cap/fetch.py ensure --id <fine-id>` in MY-SKILLS |
| Registry | A `01_skill-discovery-integration/registry.yaml` (`stub_in_b: cross-pack/nature/nature-academic-search/`) |
| This folder | Thin stub only (`SKILL.md` + `MODULE.md` note) |

Capability bytes belong in the external package cache, not in B `cross-pack/`.
