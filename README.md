# Retrieval-Augmented Generation (RAG) with LangChain, ChromaDB & Groq

This repository implements an **end-to-end Retrieval-Augmented Generation (RAG)** pipeline for document-based question answering using **LangChain Community**, **Hugging Face embedding models**, **ChromaDB**, and **Groq-hosted LLMs**.

The system retrieves relevant document chunks using semantic search and generates grounded responses based on the retrieved context, improving accuracy and reducing hallucinations.

---

## 🚀 Project Overview

The RAG pipeline follows these steps:
1. Load and preprocess source documents  
2. Split documents into manageable text chunks  
3. Generate embeddings using Hugging Face models  
4. Store embeddings in a persistent Chroma vector database  
5. Retrieve relevant context using similarity search  
6. Generate answers using a Groq-powered LLM with source references  

---

## 🧠 Architecture

**Documents → Embeddings → Vector Store → Retrieval → LLM → Answer + Sources**

---

## 🛠️ Tech Stack

- **Python**
- **LangChain (Community)**
- **Hugging Face 🤗** – Text embeddings
- **ChromaDB** – Vector database
- **Groq** – Low-latency LLM inference
- **Jupyter Notebook**

---

## 📂 Repository Structure

├── data/ # Sample source documents
├── langchain_rag_document_qa.ipynb # Document ingestion & vector creation
├── langchain_rag_retrieval_qa.ipynb # Retrieval + question answering
├── requirements.txt # Project dependencies
└── README.md

---

## 📘 Notebooks Description

### 1️⃣ `langchain_rag_document_qa.ipynb`
- Installs required dependencies  
- Loads and preprocesses documents  
- Splits text into chunks  
- Generates embeddings using Hugging Face models  
- Stores embeddings in a persistent Chroma vector database  

### 2️⃣ `langchain_rag_retrieval_qa.ipynb`
- Loads the persisted Chroma vector store  
- Retrieves relevant document chunks using a retriever  
- Uses LangChain’s `RetrievalQA` chain  
- Generates grounded answers using a Groq LLM  
- Returns source document metadata for transparency  

---

## ⚙️ Installation

Clone the repository:
```bash
git clone https://github.com/your-username/rag-langchain-groq.git
cd rag-langchain-groq
pip install -r requirements.txt
export GROQ_API_KEY="your_api_key_here"

