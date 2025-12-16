# LexiSemIR: A Two-Stage Retrieval Framework for Code-Mixed IR

This repository implements a **two-stage Information Retrieval pipeline** for **Code-Mixed Information Retrieval (CMIR)**, focusing on **Roman-transliterated Bengali–English queries** commonly found on social media platforms such as Facebook and WhatsApp.

The system combines the **high recall of lexical retrieval (BM25)** with the **semantic understanding of transformer-based embeddings (Sentence-BERT)**.

---

## 🧠 Method Overview

**Stage 1: Lexical Retrieval**

- BM25 implemented using PyTerrier
- Retrieves top 100 candidate documents per query

**Stage 2: Semantic Re-ranking**

- Sentence-BERT (`all-mpnet-base-v2`) bi-encoder
- Encodes queries and documents into dense vectors
- Uses cosine similarity to re-rank candidates
- Final top-10 results returned

---

## 🚫 Dataset Availability

The dataset used in this project is **not included** in this repository due to a **Data Usage Agreement**.

Required data files :

- `Baseline_Corpus.trec`
- `Train_query.trec`
- `Test_query.trec`
- `QRels_Train.txt`

---

## ⚙️ How to run

Install dependencies: pip install -r requirements.txt

Navigate to notebooks/ and run pipeline_main.ipynb.

The index/ folder will be generated automatically.

---

## 📊 Evaluation Metrics

Metrics are computed using training qrels.

Test queries generate ranked outputs without evaluation labels.
