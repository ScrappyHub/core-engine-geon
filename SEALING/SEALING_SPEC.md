# ENGINE SEALING SPEC (CANONICAL)

## Purpose
GEON must emit deterministic Earth-frame computations that CORE can seal and verify.

## Canonical Output Rules
1. Output MUST be valid UTF-8 JSON.
2. Output MUST be deterministic under identical inputs + parameters + engine version.
3. Output MUST NOT include:
   - user identity
   - governance state (roles, tiers, feature flags)
   - billing/monetization signals
   - attribution or intent language
   - forecasts, warnings, or alerts
4. Output MUST include:
   - run_id
   - engine_code + engine_version
   - inputs_hash (sha256 of canonical input JSON text)
   - outputs_hash (sha256 of canonical output JSON text)

## Hashing
- Hash algorithm: SHA-256
- Canonicalization: RFC 8785 JSON Canonicalization Scheme (JCS).

## What CORE seals
CORE seals:
- manifest + schemas
- run input/output payloads
- run metadata

GEON does not modify sealed artifacts after emission.
