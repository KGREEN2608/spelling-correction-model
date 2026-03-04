# 🧠 Vietnamese Administrative Text Spell Correction using Transformer

## 📌 Introduction

This project explores the application of Transformer-based Sequence-to-Sequence models for Vietnamese administrative text spell correction.

The study focuses on fine-tuning the ViT5 model combined with a custom-built SmartErrorGenerator to simulate realistic spelling errors in administrative documents.

This is an academic research project conducted as part of an undergraduate thesis in Computer Science.

---

## 🎯 Objectives

- Study the Vietnamese spell correction problem in administrative documents
- Apply Transformer-based Seq2Seq architecture for error correction
- Build a controlled error generation system (SmartErrorGenerator)
- Evaluate model performance on both error detection and error correction tasks
- Deploy an interactive demo for experimentation

---

## 🏗 Methodology

The project follows a structured NLP pipeline:

### 1. Data Collection & Preparation
- Vietnamese administrative-style texts
- Data cleaning and normalization

### 2. Error Simulation
- Custom SmartErrorGenerator
- Controlled injection of realistic spelling mistakes
- Multiple error types (character-level, tone-level, word-level)

### 3. Model Fine-tuning
- Pretrained ViT5-base
- Seq2Seq training using Hugging Face Transformers
- Tokenization & batch processing

### 4. Evaluation
- Detection Metrics
- Correction Metrics
- Loss monitoring
- Experimental analysis

### 5. Deployment
- Google Colab demo
- Model published on Hugging Face Hub

---

## 🤖 Model Architecture

- Transformer-based Encoder–Decoder architecture
- Pretrained ViT5 fine-tuned for Vietnamese spell correction
- Supervised learning with paired (noisy → corrected) sentences

---

## 📊 Evaluation Metrics

### Detection Metrics
- Precision
- Recall
- F1-score

### Correction Metrics
- Exact Match Accuracy
- Token-level Accuracy
- Training & Validation Loss

---

## 📈 Experimental Results

### Model Evaluation Metrics
![Model Evaluation Metrics](https://drive.google.com/uc?export=view&id=128Mxj5nAdtW-R52zXZWcNafOdlJFNxKh)

### Training Results
![Training Results](https://drive.google.com/uc?export=view&id=1_fgw12dZyzX_Ub1_eg9iQT2NOFF8TBHJ)

The experimental results show that the fine-tuned model effectively corrects synthetic administrative spelling errors under controlled conditions.

---

## 🚀 Demo

Google Colab notebook (may require compatible library versions):

👉 [Open Demo on Google Colab](http://colab.research.google.com/drive/1LiYXhIHGiHaM4QaDcUK4Zu9nF0avw93B)

> ⚠️ Note: This notebook was built in 2025 and may need specific dependency versions to execute successfully.

---

## 🔬 Contributions

- Designed a structured pipeline for Vietnamese administrative text correction
- Developed SmartErrorGenerator for controlled error simulation
- Implemented dual-level evaluation (detection + correction)
- Deployed public demo for reproducibility

---

## ⚠ Limitations

- Errors are synthetically generated, not fully real-world data
- Model may over-correct in certain contexts
- Not evaluated on long document-level inputs
- Performance depends on quality of generated training data

---

## 🔮 Future Work

- Fine-tuning larger models (e.g., ViT5-large)
- Integrating semantic consistency checking
- Testing on real-world noisy administrative documents
- Applying reinforcement learning with human feedback

---

## 🛠 Technologies Used

- Python
- Hugging Face Transformers
- PyTorch
- Google Colab
- Weights & Biases
- Hugging Face Hub

---

## 👨‍💻 Authors

Nguyễn Minh Khang  
Manual Tester 

Trần Vĩ Khang  
Developer
