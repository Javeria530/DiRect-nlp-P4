# DiReCT - Retrieval-Augmented Generation for Clinical Diagnostics

DiReCT is a clinical information retrieval and summarization project built using Retrieval-Augmented Generation (RAG).

The project explores how semantic retrieval and Large Language Models can be combined to retrieve relevant clinical information and generate context-aware responses from medical data.

## Project Overview

Large Language Models can generate fluent responses, but their answers are not always grounded in the required source information.

DiReCT addresses this problem using a Retrieval-Augmented Generation pipeline.

The system retrieves relevant clinical information before generating a response, allowing the generation process to use retrieved evidence as additional context.

The project demonstrates practical applications of:

- Retrieval-Augmented Generation (RAG)
- Natural Language Processing (NLP)
- Semantic Search
- Vector Embeddings
- FAISS
- LangChain
- Large Language Models
- Clinical Data Processing
- Streamlit

## System Architecture

The overall pipeline follows this structure:

```text
Clinical Data
     |
     v
Data Preprocessing
     |
     v
Document Preparation
     |
     v
Embedding Generation
     |
     v
FAISS Vector Index
     |
     v
User Query
     |
     v
Query Embedding
     |
     v
Similarity Search
     |
     v
Top-K Relevant Documents
     |
     v
Context Construction
     |
     v
Language Model
     |
     v
Context-Aware Response
