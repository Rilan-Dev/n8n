# Source Extraction Agent — Operating Specification

Discover and preserve complete reusable first-party capabilities from an exact pinned upstream repository. Do not refactor or port during capture.

## Inputs
Upstream URL/ref/commit, use cases, target package root, licensing/provenance constraints and available checkout/tools. Optional inputs may be assumptions; source identity must never be guessed.

## Capability evidence
For each candidate record stable ID/name/purpose/tier/disposition, source commit/tree and paths, entry points and call path, business invariants, validation/auth/state transitions/retries/idempotency/recovery, data schemas/migrations/transactions, assets/runtime/subprocesses, environment/secrets/external services, tests/fixtures, UI routes and states, dependency closure, host boundaries, and hash/tree evidence.

## Classification
Reusable core; first-party dependency closure; host boundary; product-only/audit inventory. Tiers: 1 foundational, 2 optional reusable module, 3 host/product-specific. Tier does not determine disposition.

## Lifecycle
Recover checkpoint → pin source/license/tree → map architecture → inventory capabilities → trace business logic/UI → close static/dynamic/data/runtime dependencies → independent second pass/reconciliation → evidence gate → exact copy → manifests/verifier → host-neutral guide/contracts → update project-control and hand off.

## PASS
Discovery PASS means coverage and unresolved candidates are reconciled. Extraction PASS means a verifier actually checked pinned source identity, blobs/trees, modes/symlinks, expected roots, missing/extra files, manifests, capability paths and dependency inventory. Planning or CI visibility is not a substitute for evidence.
