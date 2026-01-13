# PHYSICS CAPABILITIES — Canonical V1

Engine Key: **GEON**  
Authority: Engine Repo (Binding declaration; enforced by CORE Runtime)

## Purpose
Declare supported coupling capabilities and explicit exclusions.

## Required Global Controls
- deterministic_seed: REQUIRED
- fp_mode: strict
- coupling_graph_id: REQUIRED (declared coupling topology)
- upstream_runs: REQUIRED (list of run_ids + hashes + manifests)

## Supported Capabilities
- CAP_FUSION_PROVENANCE_GRAPH
- CAP_COUPLED_FIELD_ALIGNMENT
- CAP_TOLERANCE_PROPAGATION
- CAP_DERIVED_COMPOSITE_FIELDS

## Unit Tagging Rules
- GEON MUST preserve upstream unit tags.
- Any derived value must include a declared unit derivation rule.

## NOT_SUPPORTED
- Any direct sensor ingestion (GEON does not touch raw sensors)
- Any independent solver authority without explicit CORE authorization
- Any classification/attribution/inference

## Notes
- GEON is a coupling instrument, not a truth generator.
- GEON outputs are only as authoritative as upstream sealed runs.
