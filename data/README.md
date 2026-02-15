# Experiment Datasets

This directory contains test datasets used across notebooks.

## Structure

```
data/
├── sample_datasets/
│   ├── contradictory_docs/    # Documents with internal contradictions
│   ├── consistent_docs/        # Consistent reference documents
│   └── mixed_scenarios/        # Complex test cases
└── embeddings_cache/           # Cached embeddings (gitignored)
```

## Dataset Guidelines

### Adding Datasets

1. **Small datasets (< 10MB):** Can be committed to the repo
2. **Large datasets (> 10MB):** Should be gitignored and documented here with download instructions
3. **Sensitive data:** Never commit. Use anonymized samples instead.

### Dataset Format

Follow the CuratorApp structure:

- Plain text files (.txt)
- Markdown files (.md)
- JSON structured data (.json)

### Sample Datasets

**contradictory_docs/**
- Purpose: Documents containing self-contradictions
- Use case: Testing contradiction detection workflows
- Source: TBD

**consistent_docs/**
- Purpose: Clean reference documents without contradictions
- Use case: Baseline testing, negative examples
- Source: TBD

## Downloading Large Datasets

If you need access to large datasets:

```bash
# Example: Download from shared storage
# wget https://example.com/datasets/large_dataset.zip
# unzip large_dataset.zip -d data/sample_datasets/
```

## Data Privacy

⚠️ **Important:** Never commit:
- Proprietary Euclid data
- Personal information
- API keys or credentials
- Large model files

Use anonymized, synthetic, or publicly available data for experiments.