# 🧠 Symptom Checker AI — Project Guide

## 🎯 Project Goal

We are building an AI-powered **Symptom Checker System** that helps users (e.g., parents like Grace) understand possible health conditions based on symptoms and receive safe, non-diagnostic guidance.

The system uses **Retrieval-Augmented Generation (RAG)**:
- It retrieves relevant medical knowledge from a dataset
- Then generates a response using an AI model

This ensures:
- Accuracy (grounded in real data)
- Safety (no hallucinated medical advice)
- Explainability

---

## 🏗️ System Architecture Overview

The system follows this pipeline:


## 🔄 Core Pipeline (VERY IMPORTANT)

### 1. Ingestion Pipeline
- Load documents (TXT, PDF later)
- Clean text
- Split into chunks
- Convert chunks into embeddings
- Store in FAISS vector database

---

### 2. Retrieval System
- Convert user query into embedding
- Search FAISS index
- Return top relevant chunks

---

### 3. Response Generation
- Combine retrieved chunks into context
- Send to LLM (Ollama or OpenAI)
- Generate safe medical response


## ⚙️ Technical Requirements

### Models
- Embeddings: sentence-transformers (offline)
- LLM:
  - Default: Ollama (offline)
  - Optional: OpenAI (future)

---

### Vector Database
- FAISS (primary)
- Future: ChromaDB or PostgreSQL (pgvector)

---

### Backend
- FastAPI (API layer)
- Optional UI: Streamlit (dev only)

---

## 🧪 MVP Scope (IMPORTANT)

We are NOT building everything at once.

### Phase 1 (Current)
- Document ingestion
- Chunking
- Embeddings
- FAISS storage

### Phase 2
- Retrieval system
- Query search

### Phase 3
- AI response generation

### Phase 4
- API + UI

---

## 🚫 Constraints

- The system must NOT provide medical diagnosis
- Responses must be informational only
- Must include safety recommendations
- Must handle uncertainty safely

---

## 🧠 Coding Guidelines for AI Assistant

When generating code:

1. Follow the folder structure strictly
2. Keep modules small and focused
3. Avoid hardcoding paths
4. Write reusable functions
5. Add comments explaining logic
6. Prefer simple implementations first (MVP)

---

## 📌 Key Features to Implement

- Document loader (TXT first)
- Text cleaner
- Chunking system
- Embedding generator
- FAISS vector store
- Retrieval (cosine similarity)
---

## 🚀 Future Enhancements

- Multi-query retrieval
- Hybrid search (keyword + vector)
- Reranking
- Chat memory
- Multilingual support
- Doctor-reviewed datasets

---

## 👩‍👧 User Story (Grace)

Grace is a busy mother who:
- Inputs symptoms (e.g., "child has fever and cough")
- Gets possible explanations
- Gets safe next steps

---

## ✅ Success Criteria

The system should:
- Return relevant medical context
- Generate safe responses
- Be modular and scalable

---

## 🔥 Instruction to AI (Cursor)

You are assisting in building a modular AI system.

Always:
- Respect architecture
- Do not mix layers (data, core, api)
- Keep code production-ready
- Ask for clarification if unclear
