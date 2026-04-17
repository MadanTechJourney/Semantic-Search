# 📘 README: Semantic Search & RAG-based Review Analysis

## 🚀 Project Overview

This project builds a **Semantic Search System** and a **Retrieval-Augmented Generation (RAG) pipeline** using customer review data (Flipkart dataset).

It combines:

* Natural Language Processing (NLP)
* Vector Search (FAISS)
* Transformer Models

The system allows you to:

* Search reviews based on **meaning (not just keywords)**
* Generate intelligent answers using retrieved context

---

## 📂 Dataset

The dataset contains product reviews with the following columns:

* Product Name
* Review Text
* Summary
* Rating

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy (data processing)
* Matplotlib, Seaborn (visualization)
* Sentence Transformers (embeddings)
* FAISS (vector similarity search)
* Hugging Face Transformers (RAG model)
* WordCloud (text visualization)

---

## ⚙️ Installation

Install required libraries:

```bash
pip install sentence-transformers
pip install faiss-cpu
pip install transformers
pip install wordcloud
pip install kaggle
```

---

## 🔍 Project Workflow

### 1. Data Loading

* Upload dataset (`Dataset-SA.csv`)
* Load into Pandas DataFrame

### 2. Text Preprocessing

* Convert text to lowercase
* Remove special characters
* Combine **Review + Summary**

### 3. Data Visualization

* Rating distribution (countplot)
* Word cloud for text insights

### 4. Embedding Generation

* Use `SentenceTransformer (all-MiniLM-L6-v2)`
* Convert text into dense vectors

### 5. FAISS Indexing

* Normalize embeddings
* Store vectors using FAISS for fast similarity search

### 6. Semantic Search

Retrieve top-k similar reviews:

```python
semantic_search("battery life is good", k=5)
```

---

## 🤖 RAG Pipeline (Question Answering)

* Uses retrieved documents as **context**
* Generates answers using **FLAN-T5 model**

Example:

```python
rag_answer("Is the battery life good?")
```

---

## 📊 Evaluation Metrics

* **Precision@K**
* Measures relevance of retrieved results

Example:

```python
precision_at_k("battery life", 5)
```

---

## 📈 Visualization

* PCA used to reduce embedding dimensions
* Scatter plot shows semantic clustering

---

## 🎯 Key Features

✅ Semantic understanding (not keyword-based)
✅ Fast similarity search using FAISS
✅ Context-aware answer generation (RAG)
✅ Data visualization for insights
✅ Simple and extensible pipeline

---

## 📌 Future Improvements

* Improve evaluation with labeled data
* Add UI (Streamlit / Web App)
* Use larger LLMs for better answers
* Optimize search ranking

---

## 👨‍💻 Author

Developed as an NLP + AI project to demonstrate:

* Semantic Search
* Vector Databases
* Retrieval-Augmented Generation (RAG)

---

## 📜 License

This project is open-source and free to use for educational purposes.

---

💡 *Tip: This project is a strong addition to your resume if you're targeting AI/ML roles.*
