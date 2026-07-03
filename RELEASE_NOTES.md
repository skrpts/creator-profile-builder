# Release Notes

## v1.1.16
GH#745 — declare per-step `output: {name, type}` on every execution step (voice_patterns/text, audience_profile/text, banned_words/list, creator_profiles/text, validation_result/decision, review_feedback/text, polished_profiles/text, consistency_verdict/decision). Lights up the #744 rich flow-map. Content-only; no bindings or logic changes.

## v1.1.15
Fix-forward after Row 3b v1.1.14 publish failure. The v1.1.14 per-skrpt CI's "Register version with Hub API" step failed because the consumer's source `manifest.id` (d4387ebe…) did not match the D1 catalogue row's id (9e698b5f…) — a legacy drift from before Action 6 (`0bcc5ae0`) made publish-skrpt.mjs Step 2 INSERT use `manifest.id` for the D1 id column. v1.1.15 reconciles the source `manifest.id` to the catalogue authoritative value (Row-5-equivalent for consumers) and republishes. Per Adj-1: no re-tag of v1.1.14; the orphaned GitHub release artefact stays inert (no D1 versions row, no consumer pinned it).

## v1.1.14
GH#645 Row 3b — migrate to K-037 dep-referenced schema. Strip 5 inline shared-content files and declare 5 hub-shared deps (UUID id + slug name + version + checksum from `gen-dep-checksums.mjs`). Closes pre-Step-3 inline-vendoring for this bundle.

## v1.1.13
Wave 2: re-signed with canonical engine signing pipeline.

## v1.1.12
Tags migrated inline into manifest (GH#586). tags.yaml retired.

## v1.1.11
Bundle re-signed with canonical engine signing pipeline (Wave 2 migration).

## v1.1.10
Signature fix — RELEASE_NOTES.md now included in integrity checksum.

## v1.1.9
Initial catalogue release with full structural and content-quality validation. All scanner checks pass.
