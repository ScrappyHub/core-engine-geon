# GEON — Coupled Geophysical Orchestration Engine

GEON is a governed coupling/orchestration engine that fuses *declared* outputs from multiple CORE engines into composite geophysical measurements.

---

## Engine Role

**Engine Type:** FUSION_ENGINE  
**Domain:** multi-domain coupling + provenance-preserving fusion

---

## What GEON Computes (Deterministic)

- alignment of timebases and coordinate frames across engine outputs
- composite derived fields (e.g., coupled stress/thermal/flow indicators) **only from declared inputs**
- uncertainty propagation / tolerance aggregation (numeric only)
- provenance graphs linking every fused value to upstream run hashes + manifests

---

## Prohibitions

GEON does NOT:
- solve physics independently unless explicitly authorized by CORE law
- invent data or fill missing upstream values
- infer meaning, intent, attribution, or identity
- bypass engine registry capability/manifest constraints

---

## Governance

GEON is governed by CORE law and FUSION_ENGINE_BASE_GOVERNANCE.md.
