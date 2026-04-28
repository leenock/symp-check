# Symptom Checker AI - Phase Tasks

## Phase 1 - Ingestion + Vector Store (Current MVP)
- [x] Create TXT document parser (`app/data/ingestion/parser.py`)
- [x] Implement document loader for `app/data/raw_docs/`
- [x] Implement text cleaning and normalization
- [x] Implement overlapping chunking strategy
- [x] Implement embedding generation (`sentence-transformers`)
- [x] Implement FAISS vector store save/load/search
- [x] Build ingestion pipeline to index documents end-to-end
- [ ] Add unit tests for loader, cleaner, chunker, and vector store
- [ ] Add structured logging for ingestion runs

## Phase 2 - Retrieval System
- [x] Implement query embedding helper
- [x] Implement top-k retrieval from FAISS
- [ ] Add retrieval service endpoint contract (input query -> chunks)
- [ ] Add retrieval quality checks with sample symptom queries
- [ ] Add configurable score threshold for low-confidence matches

## Phase 3 - Safe Response Generation
- [x] Implement safe prompt builder with constraints (no diagnosis)
- [x] Implement MVP safe response generator
- [ ] Integrate Ollama response generation path
- [ ] Add fallback behavior when no relevant context is found
- [ ] Add output guardrails tests (safety wording, escalation hints)

## Phase 4 - API Layer (FastAPI)
- [ ] Create API schema for symptom query + response payload
- [ ] Implement `/health` and `/check-symptoms` routes
- [ ] Wire retrieval + risk + generator into API service layer
- [ ] Add request validation and error handling
- [ ] Add integration tests for API happy path + edge cases

## Phase 5 - UI (Optional Dev Interface)
- [ ] Build simple Streamlit UI for symptom input and response view
- [ ] Display retrieved context snippets and risk level
- [ ] Add disclaimer and emergency guidance banner

## Data + Operations
- [ ] Add more medical source documents to `app/data/raw_docs/`
- [ ] Add reproducible re-index command in README
- [ ] Track model/data versions used to build each FAISS index
- [ ] Add `.gitignore` rules for cache files (`__pycache__`, `.pyc`)

## Done Definition for MVP
- [ ] Ingestion pipeline runs successfully on local dataset
- [ ] Retrieval returns relevant chunks for common symptom queries
- [ ] Response includes risk level + safe next steps
- [ ] API endpoint returns stable JSON response for UI consumption