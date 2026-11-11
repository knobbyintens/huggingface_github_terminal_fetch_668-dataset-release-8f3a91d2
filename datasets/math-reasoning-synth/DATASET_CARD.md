---
artifact_id: math-reasoning-synth
release: 2026-Q4
kind: derived
format: jsonl
record_count: 13200
language: en
derived_from: math-reasoning-raw
---

# Math-Reasoning-Synth (2026-Q4)

Reasoning-augmented corpus derived from Math-Reasoning-Raw. Each record pairs a
question with a synthesized reasoning trace and a normalized final answer.

## Record Schema

| field | type | description |
| --- | --- | --- |
| sample_uid | string | Stable artifact-scoped identifier |
| prompt_instruction | string | Task instruction shown to the model |
| reasoning_trace | string | Synthesized step-by-step reasoning |
| final_answer | string | Normalized final answer |
| origin_dataset | string | Upstream dataset identifier |
| reasoning_style | string | Style bucket assigned during synthesis |
| quality_tag | string | Curation quality label |
| annotations | object | Extra curation metadata |

## Provenance

- upstream_dataset: openai/gsm8k
- upstream_owner: OpenAI
- synthesis_model: deepseek-ai/DeepSeek-V2.5
- synthesis_method: reasoning traces generated with the synthesis model, then filtered
- pipeline: schema remapping, answer normalization and quality filtering
