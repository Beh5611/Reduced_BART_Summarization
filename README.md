# 🧠 Lightweight BART for Conversational Summarization

This project implements a scaled-down version of the BART (Bidirectional and Auto-Regressive Transformers) model for **abstractive summarization** of conversational data. The goal is to create a summarization model that can be trained and deployed in resource-constrained environments while maintaining reasonable performance.

## 🔍 Motivation

With the increasing use of digital communication platforms like Zoom, Microsoft Teams, and Discord, the ability to summarize large volumes of conversational text is more important than ever. However, full-sized transformer models like BART-base are often computationally intensive. This project explores the performance tradeoffs of a reduced BART model trained on smaller hardware and datasets.

---

## 🧱 Model Architecture

- Based on the original [BART model](https://arxiv.org/abs/1910.13461)
- Reduced to:
  - **4 encoder layers**
  - **4 decoder layers**
  - Smaller hidden sizes and fewer attention heads
- Trained using the Hugging Face `transformers` library

---

## 📊 Datasets

### 📚 Pretraining
- **Gigaword Corpus** (~700k samples)  
  Used for learning general summarization patterns and building foundational knowledge.

### 🗣️ Fine-Tuning
- **SAMsum Dataset**  
  Dialogue-based summarization dataset with informal, multi-speaker conversational text.
