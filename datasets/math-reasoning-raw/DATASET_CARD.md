---
artifact_id: math-reasoning-raw
release: 2026-Q4
kind: raw
format: jsonl
record_count: 8470
language: en
---

# Math-Reasoning-Raw (2026-Q4)

Raw grade-school math word-problem corpus, normalized for downstream curation.

## Record Schema

| field | type | description |
| --- | --- | --- |
| sample_uid | string | Stable artifact-scoped identifier |
| question_text | string | Word-problem statement |
| worked_solution | string | Step-by-step reference solution |
| answer_value | string | Final answer |
| difficulty_band | string | Bucketed difficulty label |
| source_origin | string | Origin tag preserved from collection |

## Provenance

- upstream_dataset: openai/gsm8k
- upstream_owner: OpenAI
- pipeline: question cleaning, de-duplication and schema normalization

## License

License: mit
