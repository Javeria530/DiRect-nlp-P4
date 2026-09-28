#  DiReCT — Retrieval-Augmented Generation for Clinical Diagnostics

DiReCT is an AI-powered clinical information retrieval and summarization system built using **Retrieval-Augmented Generation (RAG)**.

The project explores how semantic retrieval and Large Language Models can be combined to retrieve relevant clinical information and generate context-aware responses from medical data.

##  Project Objective

Large Language Models can generate fluent responses, but their answers are not always grounded in the required source data.

DiReCT addresses this problem using a RAG pipeline:

1. Clinical information is processed and indexed.
2. Text is converted into vector representations.
3. A user submits a clinical query.
4. Relevant information is retrieved using vector similarity search.
5. Retrieved evidence is supplied as context for response generation.

This architecture helps ground generated responses in retrieved clinical information.

## 🧠 System Architecture

Clinical Dataset
        ↓
Data Preprocessing
        ↓
Text / Document Preparation
        ↓
Embedding Generation
        ↓
FAISS Vector Index
        ↓
User Clinical Query
        ↓
Query Embedding
        ↓
Similarity Search
        ↓
Top-K Relevant Documents
        ↓
Context Construction
        ↓
LLM / Generation Pipeline
        ↓
Evidence-Grounded Response

## Technology Stack

- Python
- PyTorch
- LangChain
- FAISS
- Natural Language Processing
- Retrieval-Augmented Generation (RAG)
- Large Language Models
- Streamlit
- Jupyter Notebook
- Kaggle
- NVIDIA Tesla T4 GPU

## Dataset

The project experiments with clinical information derived from the **MIMIC-IV-Ext** ecosystem.

The data is processed before being passed into the retrieval pipeline so that relevant clinical information can be efficiently searched.

> Important: MIMIC datasets contain sensitive clinical information and must be used according to their applicable access and data-use requirements.

##  Semantic Retrieval

Traditional keyword search depends heavily on exact words appearing in a document.

DiReCT instead explores **semantic retrieval**.

Documents and queries are represented as dense numerical vectors called embeddings.

Conceptually:

```text
Clinical Document
      ↓
Embedding Model
      ↓
Vector Representation
