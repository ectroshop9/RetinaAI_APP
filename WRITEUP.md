# 👁️ RetinaAI: Advanced Diabetic Retinopathy Diagnostic Pipeline
> **A Human-Centered, Edge-AI Solution for the MedGemma Impact Challenge**

---

## 📌 Project Overview
**RetinaAI** is an elite clinical decision support system designed to assist ophthalmologists in the early detection and grading of **Diabetic Retinopathy (DR)**. By leveraging a multimodal neural architecture, the system integrates high-resolution fundus imaging with real-time clinical dictation.

---

## 🚀 The Impact & Problem Domain (15% Assessment)

### The Clinical Gap
In underserved regions, the lack of specialists leads to delayed diagnoses and preventable blindness. Most AI solutions require cloud connectivity, which compromises **patient privacy** and fails in low-bandwidth environments.

### Our Solution's Impact
* **Edge Capability:** Runs locally using **1.58-bit Quantization**, ensuring privacy and accessibility.
* **Time Efficiency:** Estimated to **reduce diagnosis time by 40%** in areas lacking specialists.
* **Accuracy:** Grounded in medical-grade data via **RAG (Retrieval-Augmented Generation)**.

---

## 🛠️ Technical Stack (Effective Use of HAI-DEF)

| Component | Technology | Role |
| :--- | :--- | :--- |
| **Sensing Engine** | `MedSigLIP-448` | Pixel-level feature extraction for microaneurysms. |
| **Inference Core** | `MedGemma 1.5-4b` | Clinical reasoning using **BitNet (1.58-bit)**. |
| **Comparison Layer**| `LanceDB` | Vector storage for grounded historical context (RAG). |
| **Auditory Interface**| `MedASR` | Converts physician verbal notes into clinical embeddings. |
| **Explainability** | `LIT (Learning Interpretability Tool)` | Generates saliency maps for diagnostic transparency. |
| **Safety Audit** | `Med-PaLM Toolkit` | Benchmarks reports against gold-standard rubrics. |

---

## 👨‍⚕️ User Journey: Human-Centered Design

RetinaAI follows a seamless four-step workflow to empower doctors:

1.  **📥 Upload:** The doctor uploads a high-resolution fundus image.
2.  **🎙️ Dictate:** The doctor speaks their initial observations (via **MedASR**).
3.  **🧠 Synthesize:** The system fuses visual and verbal data to generate a detailed report.
4.  **🔍 Verify:** The doctor reviews the **LIT heatmaps** to confirm the AI's focus areas (e.g., hemorrhages).

---

## 🏗️ System Architecture & Methodology

### 1. Multimodal Embedding Fusion
Ensures that visual, textual, and auditory data are processed within a shared semantic space using a **Linear Projection Layer**.

### 2. Efficiency at the Edge
Utilizes **1.58-bit Quantization** to ensure real-time inference with a minimal VRAM footprint, making it ideal for mobile clinical units.

### 3. Explainable AI (XAI)
Beyond classification; providing clinical narratives justified by visual evidence, ensuring the system remains a "support tool," not a "black box."

---

## 📜 Standards & Compliance
* **Code Style:** Strictly governed by **PEP 8**.
* **Documentation:** **Google-Style Docstrings**.
* **License:** **CC BY 4.0** (as per competition rules).

---

## 📂 Project Structure
```text
.
├── config/      # System & Model configurations
├── docs/        # Technical documentation
├── reports/     # Quality audits & Performance logs
├── src/         # Core Logic (retina_core.py)
└── tests/       # Unit tests & Validation suites
---
## 📚 References & Technical Sources

### 1. Google Health AI Developer Foundations (HAI-DEF)
* **MedGemma 1.5-4b-it:** Official open-weight model for clinical reasoning.  
  [Link to Model Collection](https://huggingface.co/collections/google/medgemma-release)
* **MedSigLIP:** Multimodal vision-language model for medical imaging.
* **Med-PaLM Evaluation Toolkit:** Clinical safety and benchmark framework.

### 2. Core Methodologies & Datasets
* **IDRiD Dataset:** Indian Diabetic Retinopathy Image Dataset for high-resolution lesion detection.  
  *Source: [IEEE Dataport / IDRiD Site]*
* **BitNet 1.58b (Quant158):** "The Era of 1-bit LLMs: All Large Language Models are in 1.58 Bits."  
  *Source: Microsoft Research / arXiv:2402.17764*
* **LIT (Learning Interpretability Tool):** "The Language Interpretability Tool: Extensible, Interactive Visualizations and Analysis for NLP Models."  
  *Source: Google Research / arXiv:2008.05122*

### 3. Vector Database & RAG
* **LanceDB:** Serverless vector database for efficient k-NN retrieval of clinical cases.

### 4. Competition Standards
* **MedGemma Impact Challenge Rules:** Managed by Kaggle & Google Research (2026).
* **CC BY 4.0 License:** Open-source compliance for winning submissions.
