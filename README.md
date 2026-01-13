# RUN BUNDLE (Engine View) — Canonical V1

This folder documents what CORE produces per run for this engine.

## Engine Responsibilities
- Emit schema-valid RUN_OUTPUT.json only
- Emit any additional domain artifacts referenced by ARTIFACT_INDEX.json
- Never modify sealed artifacts after emission
- Never accept peer delivery; inputs are delivered by CORE only

## CORE Responsibilities
CORE produces the run bundle per the platform RUN_BUNDLE_SPEC:
- validates RUN_INPUT against INPUT_SCHEMA
- strips forbidden context keys
- canonicalizes JSON via RFC 8785 (JCS)
- hashes all artifacts and writes SHA256SUMS
- rejects non-compliant outputs

- Authoritative spec: ScrappyHub/Core-platform/GOVERNANCE/RUN_BUNDLE_SPEC.md

## Required Minimum Artifacts
- RUN_INPUT.json
- RUN_OUTPUT.json
- ARTIFACT_INDEX.json
- SHA256SUMS.txt
- RUN_META.json
- engine contracts copied into bundle:
  - ENGINE_MANIFEST.json
  - INPUT_SCHEMA.json
  - OUTPUT_SCHEMA.json
  - COUPLING_RULES.json
  - SEALING_SPEC.md
