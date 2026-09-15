# Submission run evidence

This directory contains the selected, immutable run and UI transcript files
used by `artifacts/REPORT.md`. It is intentionally tracked even though local
scratch output under `runs/` and `transcripts/` remains ignored.

## Final v4 evidence

- `v4_B_base_openai_20260915T002658653525.json`
- `v4_B_group_openai_20260915T002731266631.json`
- `v4_B_extension_openai_20260915T002731522569.json`
- `v4_B_adversarial_openai_20260915T002734445196.json`
- `ui-test_openai_20260915T005305358713.transcript.json`

The extension run has two manually reviewed `missing_api_key` tool-result
errors (E09 and E10). Its routing and arguments passed, but it is not evidence
of successful external execution until rerun with `TAVILY_API_KEY` configured.

## Historical base evidence

The version progression uses unedited JSON payloads generated with the exact
artifact hashes recorded in `artifacts/version_log.csv`:

- `v0_B_base_openai_20260915T093439522130.json`
- `v1_B_base_openai_20260915T093703997596.json`
- `v2_B_base_openai_20260915T093540464304.json`
- `v3_B_base_openai_20260914T193341132347.json`

The v0, v1, and v2 files were rerun on 2026-09-15. Each has 30 measured cases
and zero provider errors. Artifact versions remain in `starter_v0/artifacts/`;
this directory intentionally contains evidence outputs only.

## Why this directory exists

`runs/`, `transcripts/`, and `tickets/` are scratch/output directories and stay
ignored so accidental provider output and generated actions are not committed.
Only reviewed evidence selected for submission belongs here. Never copy `.env`,
credentials, real user data, or generated ticket files into this directory.
