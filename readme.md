# CAG Approach Notes

## Folder: CAG_1

### VersionV1 Disadvantages

1. In-memory cache is fragile and process-local; cache is lost unless saved and reloaded explicitly.
2. Cache key uses exact question plus selected context, so semantically same questions can miss cache.
3. Cross-encoder reranking is accurate but slow and expensive for large numbers of chunks.
4. Dummy chunking is character-based, so it can split facts mid-sentence and reduce answer quality.
5. Guardrails are rule-based (regex), so they are easy to bypass and can block valid edge cases.
6. No source citation mapping per chunk in the final answer, which reduces traceability.
7. The pipeline uses one LLM call after reranking; no self-check pass is used to detect hallucinations.
8. VersionV1 does not use vector indexing, so scaling to very large corpora is limited.
9. Streaming output currently bypasses cache reuse, so repeated streamed requests still invoke the model.
10. The approach depends heavily on external model and network availability, which affects reliability.

## Folder: CAG_2

No VersionV1 notebook implementation is added in this folder yet. The same disadvantages are expected if the same baseline pattern is reused.
