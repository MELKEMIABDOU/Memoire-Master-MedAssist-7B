# Memoire-Master-MedAssist-7B

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Framework: HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97-HuggingFace-orange)](https://huggingface.com/)

An ethically aligned, secure, and locally deployable AI medical assistant system built on open-source infrastructure. This project fine-tunes a **DeepSeek-R1-Distill-Qwen-7B** model using **QLoRA** and integrates a **Retrieval-Augmented Generation (RAG)** pipeline to provide verifiable, privacy-compliant clinical decision support.

---

## 🚀 Key Features

* **Privacy-First & Local Deployment:** Operates entirely on-premise without relying on third-party APIs (like GPT-4 or Gemini), ensuring strict patient data confidentiality.
* **Resource-Efficient Fine-Tuning:** Leverages **QLoRA (4-bit quantization)** to drastically lower hardware barriers, enabling deployment in resource-limited clinical settings.
* **Hallucination Mitigation:** Combines domain-specific instruction fine-tuning with a robust **RAG pipeline** to ground model responses in verified medical documentation.
* **Semantic Vector Search:** Uses advanced vector embeddings to retrieve relevant clinical contexts dynamically before generating answers.

## 🛠️ Tech Stack & Architecture

* **Base Model:** `DeepSeek-R1-Distill-Qwen-7B`
* **Fine-Tuning:** QLoRA, PEFT, BitsAndBytes, Hugging Face Transformers
* **RAG Pipeline:** Vector Databases (e.g., ChromaDB / FAISS), Semantic Search
* **Language:** Python
* **Hardware Target:** Consumer-grade GPUs (optimized for low VRAM usage)

---

## 📊 Methodology Overview

1. **Quantized Low-Rank Adaptation (QLoRA):** Fine-tuned using 4-bit base model quantization alongside adapter modules to minimize computational overhead while retaining linguistic performance.
2. **Domain Specialization:** Trained on curated clinical instruction datasets to adapt the model to specialized medical terminology.
3. **Knowledge Grounding:** Seamlessly intercepts queries to append retrieved context from verified, domain-specific medical documents via semantic vector matching.

---

## ⚙️ Quick Start & Installation

*(Tip for the user: Replace the placeholder commands below with your actual project setup scripts!)*

### Prerequisites
* Python 3.10+
* CUDA-compatible GPU

### Setup
```bash
# Clone the repository
git clone [https://github.com/YOUR_USERNAME/Memoire-Master-MedAssist-7B.git](https://github.com/YOUR_USERNAME/Memoire-Master-MedAssist-7B.git)
cd Memoire-Master-MedAssist-7B

# Install dependencies
pip install -r requirements.txt

# Run the local application
python app.py
