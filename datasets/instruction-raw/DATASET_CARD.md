---
artifact_id: instruction-raw
release: 2026-Q4
kind: raw
format: jsonl
record_count: 52002
language: en
---

# Instruction-Raw (2026-Q4)

General instruction-following corpus collected and normalized by the platform team.
Used as the instruction side of the Q4 batch.

## Record Schema

| field | type | description |
| --- | --- | --- |
| sample_uid | string | Stable artifact-scoped identifier |
| task_instruction | string | User instruction text |
| target_response | string | Reference response |
| input_context | string | Optional supporting context |
| origin_dataset | string | Upstream dataset identifier |
| curation_flag | string | Curation state applied by the pipeline |

## Provenance

- upstream_dataset: tatsu-lab/alpaca
- upstream_owner: Stanford NLP
- pipeline: instruction cleaning, blank-response removal, schema normalization
