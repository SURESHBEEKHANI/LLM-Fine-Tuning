LLM Fine-Tuning
================

**A hands-on collection of notebooks, notes, and mini-projects for fine-tuning modern Large Language Models (LLMs) across tasks, domains, and frameworks.**

This repository brings together practical workflows for:
- **Encoder models**: BERT and related variants  
- **Decoder/Chat models**: LLaMA, Gemma, GPT-style models, Mistral, etc.  
- **Frameworks & tooling**: Hugging Face, Unsloth, Llama-Factory, Axolotl, and more  
- **Modalities**: text-only LLMs, multimodal LLMs, and **TTS** models  
- **Advanced topics**: preference-based training, knowledge distillation, quantization, PDF/domain-specific fine-tuning

All content is organized as self-contained folders with Jupyter notebooks and slides/notes so you can jump directly into the topic you care about.

---

### Repository structure (high level)

- **`Axolotl/`**: Axolotl-based LLM fine-tuning configurations and example runs.  
- **`Bert/`, `Bert-finetuning/`**: BERT and encoder-style fine-tuning workflows (classification, QA, etc.).  
- **`Embedding-and-Embedding-Finetuning/`**: Embedding models and how to fine-tune them for retrieval / similarity.  
- **`Finetune-Any-SLM/`**: Recipes for fine-tuning smaller language models (SLMs).  
- **`GEMINI-Finetuning/`**: Gemini model fine-tuning examples and notes.  
- **`Gemma/`**: Gemma model fine-tuning / adaptation workflows.  
- **`GPT-Finetuning/`**: GPT-style model fine-tuning using Hugging Face and related tooling.  
- **`huggingface/`**: General Hugging Face utilities, training scripts, and starter examples.  
- **`Instruction Fine-Tuning Explained -Domain-Specific Fine-Tuning with Hugging Face/`**: Instruction fine-tuning walkthrough on domain-specific datasets (notebooks + notes).  
- **`knowledge-distillation/`**: Distillation from larger teacher models into smaller student models.  
- **`Llama/`, `Llama-Factory/`**: LLaMA fine-tuning and Llama-Factory-based training pipelines.  
- **`LLM Fine-Tuning/`, `LLM Fine-Tuning-Huggingface/`, `LLM Fine-Tuning-unsloth-vs-hf/`**: Core LLM fine-tuning workflows, including comparisons between Unsloth and vanilla Hugging Face.  
- **`LLM Finetuning-Crash-Course/`**: “All-in-one” and crash-course style notebooks for quick start.  
- **`LLM-Quantization/`**: Quantization techniques and examples for serving fine-tuned models efficiently.  
- **`Mistral/`**: Mistral model fine-tuning workflows.  
- **`Multimodal-LLM-Finetuning/`**: Finetuning for text+vision (and other) multimodal models.  
- **`Notes/`**: PDFs and slide decks (syllabus, overviews, and topic-specific notes).  
- **`Preference-based-training/`**: Preference optimization / alignment style training (DPO/RLHF-style recipes).  
- **`Train-LLMs-on-Your-PDF-Text-Data-Domain-Specific-Fine-Tuning-with-HuggingFace/`**: End-to-end pipelines to build datasets from your PDFs/text and fine-tune domain models.  
- **`TTS/`**: Text-to-Speech model fine-tuning (e.g., Orpheus 3B LoRA TTS).  
- **`unsloth/`**: Unsloth-based fine-tuning examples and benchmarks.  
- **`Why-Finetuning-Hard-in-LSTM/`**: Historical/educational materials on finetuning in pre-transformer architectures.

> **Tip:** Each folder is mostly self-contained. Open the primary notebook (often named something like `*_all_in_one.ipynb`, `*_finetuning*.ipynb`, or similar) to get a guided, step-by-step workflow.

---

### Prerequisites

- **OS**: Tested primarily on modern Windows (with WSL or native Python), Linux, and macOS.  
- **Python**: 3.10+ recommended.  
- **Hardware**: A GPU with at least 8–16 GB VRAM is strongly recommended for most LLM fine-tuning examples (some smaller/CPU-friendly workflows exist).  
- **Package manager**: `conda` or `mamba` is convenient, but `pip` also works.

Most individual folders will include their own environment or `requirements` information (inside notebooks or `requirements.txt`/`environment.yml` where applicable).

---

### Getting started

1. **Clone the repo**
   ```bash
   https://github.com/SURESHBEEKHANI/LLM-Fine-Tuning.git
   cd LLM-Fine-Tuning
   ```

2. **Create a Python environment (example with conda)**
   ```bash
   conda create -n llm-finetune python=3.10 -y
   conda activate llm-finetune
   ```

3. **Install dependencies for a specific module**
   - Check for a `requirements.txt` or `environment.yml` in the folder you’re interested in, or  
   - Open the main notebook in that folder and follow the first code cells (which often install the required libraries).

4. **Launch Jupyter / VS Code / Cursor**
   ```bash
   jupyter lab
   ```
   or use VS Code / Cursor’s built-in notebook support and open the `.ipynb` files directly.

---

### Suggested learning path

If you’re not sure where to start:

1. **Concepts & overview**
   - Skim the PDFs in `Notes/` (syllabus, introduction, frameworks list) to understand the landscape.  
2. **Core fine-tuning**
   - Start with `LLM Finetuning-Crash-Course/Final_Finetuning_all_in_one.ipynb` (or similar “all-in-one” notebooks) for an end-to-end example.  
3. **Framework-specific practice**
   - Explore `LLM Fine-Tuning-Huggingface/`, `unsloth/`, `Llama-Factory/`, `Axolotl/` to see different tooling around similar tasks.  
4. **Domain & modality**
   - Use `Instruction Fine-Tuning Explained -Domain-Specific Fine-Tuning with Hugging Face/`, `Train-LLMs-on-Your-PDF-Text-Data-.../`, and `Multimodal-LLM-Finetuning/` to adapt models to your own data and modalities.  
5. **Advanced topics**
   - Dive into `Preference-based-training/`, `knowledge-distillation/`, and `LLM-Quantization/` once you’re comfortable with basic supervised finetuning.

---

### Using your own data

Many notebooks show how to:
- Load datasets from CSV/JSON/Parquet or PDFs.  
- Preprocess and tokenize text for different model families.  
- Configure LoRA / QLoRA / full fine-tuning strategies.  
- Evaluate models on held-out validation sets or simple benchmarks.

Look for sections named **“Data Preparation”**, **“Training Configuration”**, or **“Evaluation”** inside the notebooks.

---

### Contributing

Contributions are welcome, especially:
- **New notebooks** demonstrating finetuning for additional model families or tasks.  
- **Bug fixes / improvements** to existing notebooks.  
- **Documentation enhancements** (better explanations, diagrams, or links to external resources).

If you submit a PR, please:
- Keep notebooks relatively lightweight (avoid committing large outputs / checkpoints).  
- Add short comments or markdown cells explaining key design choices.  
- Verify that your notebook runs end-to-end on at least one GPU environment.

---

### License

This project is licensed under the terms of the **LICENSE** file in this repository. Please review model-specific licenses and API terms of service (e.g., for Gemini, proprietary models, or hosted APIs) before running or deploying any fine-tuned models.
