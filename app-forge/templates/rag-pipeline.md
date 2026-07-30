# RAG Pipeline Template

## Architecture
Documents > Parser > Chunker > Embedder > Vector DB > Retriever > Generator

## Chunking
- Size: 500-1000 tokens
- Overlap: 10-20 percent
- Split on semantic boundaries
- Preserve metadata (source, date, section)

## Retrieval
1. Semantic search (top 20 results)
2. Metadata filtering (date, source, type)
3. Re-ranking (cross-encoder, top 5)
4. Prompt construction (system + context + query)

## Evaluation
- Recall@k: percent of relevant docs in top k
- MRR: Mean Reciprocal Rank
- Faithfulness: percent of answer supported by context
