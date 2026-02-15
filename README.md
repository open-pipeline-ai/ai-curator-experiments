# SGS Curator App - Experiments

Experimental notebooks and prototypes for the SGS Curator App project, exploring chunking strategies, retrieval methods, and contradiction detection workflows.

## 🎯 Purpose

This repository contains Jupyter notebooks used to:
- Evaluate different chunking strategies
- Test embedding models and retrieval approaches
- Prototype contradiction detection workflows
- Benchmark components before productionization
- Share experimental findings with the team

## 📁 Repository Structure

```
sgs-curator-experiments/
├── notebooks/
│   ├── chunking/              # Chunking strategy experiments
│   ├── retrieval/             # Retrieval and embedding experiments
│   ├── contradiction_detection/  # Contradiction detection workflows
│   └── end_to_end/            # Full pipeline experiments
├── data/
│   └── sample_datasets/       # Test datasets (following Redmine structure)
├── shared/                    # Shared utility code
└── requirements.txt           # Common dependencies
```

## 📓 Available Notebooks

### Chunking
- **chunking_exercise.ipynb** - Evaluates how different chunking strategies (fixed-size, recursive, semantic) affect the ability to detect contradictions using semantic similarity between chunks

### Retrieval
- Coming soon...

### Contradiction Detection
- Coming soon...

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Jupyter Lab or Jupyter Notebook

### Installation

```bash
# Clone the repository
git clone https://github.com/open-pipeline-ai/sgs-curator-experiments.git
cd sgs-curator-experiments

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter lab
```

### Running Notebooks

Navigate to the `notebooks/` directory and open any `.ipynb` file.

Each notebook includes:
- Purpose and scope
- Workflow overview
- Step-by-step implementation
- Results and analysis

## 📊 Datasets

Test datasets follow the CuratorApp structure for evaluating chunking and contradiction detection.

Place datasets in `data/sample_datasets/` following the structure:
```
data/
└── sample_datasets/
    ├── contradictory_docs/
    ├── consistent_docs/
    └── mixed_scenarios/
```

**Note:** Large datasets should not be committed. Use `.gitignore` to exclude them.

## 🤝 Contributing Experiments

We welcome experimental contributions! To add a new notebook:

1. **Choose the right category:**
   - `notebooks/chunking/` - Chunking strategies
   - `notebooks/retrieval/` - Retrieval and embeddings
   - `notebooks/contradiction_detection/` - Contradiction workflows
   - `notebooks/end_to_end/` - Full pipelines

2. **Follow the notebook template:**
   - Add a title and purpose section
   - Include workflow overview
   - Document parameters and configurations
   - Add results/findings section
   - Include references to related work

3. **Update requirements.txt** if you add new dependencies

4. **Create a PR** with your notebook and a brief description

## 🔗 Related Projects

- [chunking-toolkit](https://github.com/open-pipeline-ai/chunking-toolkit) - Production chunking library
- [retrieval-toolkit](https://github.com/open-pipeline-ai/retrieval-toolkit) - Production retrieval library
- SGS Curator App - Main application (link TBD)

## 📝 Notebook Guidelines

When creating notebooks:

- ✅ Include clear purpose and scope at the top
- ✅ Document all dependencies and versions
- ✅ Use markdown cells to explain methodology
- ✅ Include results and analysis sections
- ✅ Reference datasets and external resources
- ✅ Keep notebooks focused on one experiment
- ✅ Add visualizations where helpful
- ❌ Don't commit large datasets or model files
- ❌ Don't include sensitive API keys (use environment variables)

## 🛠️ Common Dependencies

Key libraries used across notebooks:

- **LangChain** - Text splitting and chunking
- **Sentence Transformers** - Embedding models
- **VLLM** - Local LLM inference
- **NumPy/Pandas** - Data manipulation
- **Matplotlib/Seaborn** - Visualization
- **scikit-learn** - Similarity metrics

See `requirements.txt` for complete list.

## 📄 License

This project is licensed under the GNU Lesser General Public License v3.0 or later (LGPLv3+) - see the [LICENSE](LICENSE) file for details.

## 🤔 Questions?

- Open an issue in this repository
- Refer to the main [Curator App documentation](TBD)
- Contact the project maintainers

---

**Note:** This is an experimental repository. Production-ready code should be contributed to the respective toolkit repositories (chunking-toolkit, retrieval-toolkit).