# Chunking Experiments

Notebooks exploring different chunking strategies and their impact on downstream tasks.

## Available Notebooks

### chunking_exercise.ipynb

**Purpose:** Evaluates how different chunking strategies affect contradiction detection using semantic similarity-based chunk comparison.

**Note:** This is an idealized workflow that chunks both the test document and reference documents, then uses cosine similarity to find semantically similar chunk pairs for evaluation. This differs from production RAG which would use vector search over a pre-built knowledge base.

**Components tested:**
- Chunking strategies: Fixed-size, Recursive Text Splitting (LangChain), Semantic
- Embedding models: SentenceTransformers
- Similarity thresholds for candidate pair selection
- LLM judgement via VLLM server

**Workflow:**
```
Contradictory Doc → Chunking → Embeddings ─┐
                                            ├→ Cosine Similarity → Candidate Pairs → LLM Evaluation
Consistent Docs → Chunking → Embeddings ───┘
```

**Datasets:** Follows CuratorApp test dataset structure

**Key findings:** [Add findings after running experiments]

## Running These Notebooks

```bash
# From repository root
jupyter lab notebooks/chunking/
```

## Dependencies

See main `requirements.txt`. Key dependencies:
- `langchain-text-splitters` - Chunking strategies
- `sentence-transformers` - Embeddings
- `vllm` - Local LLM inference

## Future Experiments

Ideas for additional chunking experiments:
- Token-based vs character-based chunking
- Overlap strategies and their impact
- Domain-specific chunking (e.g., scientific papers)
- Chunking for tables and figures
- Performance benchmarks (speed vs quality)