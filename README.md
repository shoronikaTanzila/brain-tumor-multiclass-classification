# 🧠 Multimodal Brain Tumor Classification & Neural Signal Translation

An advanced deep learning framework designed for multi-class brain tumor classification from MRI scans and neural signal decoding into natural language using hybrid vision/sequence encoders and LLM decoders.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset Architecture](#dataset-architecture)
- [Model Architectures](#model-architectures)
- [Project Workflow](#project-workflow)
- [Repository Structure](#repository-structure)
- [Installation & Setup](#installation--setup)
- [Evaluation & Metrics](#evaluation--metrics)
- [License](#license)

---

## 📖 Overview
Early and accurate identification of brain tumors is vital for clinical diagnosis. This project leverages deep convolutional vision backbones, sequence transformers, and large language model (LLM) decoders to classify brain tumors into multiple pathological categories: **Glioma**, **Meningioma**, **Pituitary**, and **No Tumor (Healthy Control)**.

---

## 📊 Dataset Architecture
The project utilizes the **Merged_Brain_Tumor_MultiClass** dataset (harmonized and standardized across multiple archives):
- **No_tumor**: Healthy control MRI scans.
- **Tumor (Sub-classes)**:
  - `Glioma`: Intra-axial glial cell malignancies.
  - `Meningioma`: Extra-axial meningeal brain tumors.
  - `Pituitary`: Sellar region endocrine abnormalities.

---

## 🤖 Models & Architectures Explored

### 1. ResNet-50 + T5 Seq2Seq (Proposed Model 2 - MRI Scan & Text Generation)
- **Vision Backbone**: `ResNet-50` with residual skip connections for hierarchical spatial feature extraction and tumor boundary localization.
- **Decoder**: `T5 Seq2Seq Decoder` conditioned on prefix prompts to produce multi-class diagnostic tokens and automated clinical caption summaries.

### 2. Conformer + BART LLM (Proposed Model 1 - Neural Signal Sequence Decoding)
- **Encoder**: `Conformer Module` (combining depthwise convolutions with Macaron-style multi-head self-attention) for continuous spatial-temporal representations.
- **Decoder**: `BART LLM Decoder` connected via cross-attention projection bridges for open-vocabulary autoregressive text reconstruction and denoising.

### 3. Hybrid NN Baseline (Benchmarking)
- **Architecture**: `CNN + BiLSTM / Vision Transformer` coupled with a linear classification head for multi-class cross-validation and benchmarking.

---

## ⚙️ Project Workflow
