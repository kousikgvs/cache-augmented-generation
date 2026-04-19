# CAG Approach Notes

## Folder: CAG_1

### VersionV1 Disadvantages

1. In-memory cache is vulnerable because once the Cache size increases it crosses the LLM context Window.
3. Cross-encoder reranking is accurate but slow and expensive for large numbers of chunks.
3. Token chunking is character-based, so it can split facts mid-sentence and reduce answer quality.
4. The pipeline uses one LLM call after reranking; no self-check pass is used to detect hallucinations.
5. VersionV1 does not use vector indexing.
6. Streaming output currently bypasses cache reuse, so repeated streamed requests still invoke the model.

## Folder: CAG_2

No VersionV1 notebook implementation is added in this folder yet.
