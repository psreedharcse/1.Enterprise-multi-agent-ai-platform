# RAG (Retrieval-Augmented Generation) Architecture

## Overview

The system uses a RAG architecture to provide context-aware responses by retrieving relevant information from enterprise data sources.

---

## Key Components

### 1. Document Ingestion

* Data is collected from enterprise sources (files, SAP data, documents)
* Documents are split into smaller chunks

---

### 2. Embedding Generation

* Each document chunk is converted into vector embeddings using an embedding model

---

### 3. Vector Database

* Embeddings are stored in a vector database (PostgreSQL with PGVector or SAP HANA Vector Engine)
* Enables semantic search

---

### 4. Retriever

* User query is converted into embedding
* Similar documents are retrieved using similarity search

---

### 5. LLM Integration

* Retrieved context is passed to LLM
* LLM generates response using both query and retrieved context

---

## Execution Flow

1. User submits query
2. Query is converted into embedding
3. Vector DB retrieves relevant documents
4. Context is injected into LLM prompt
5. LLM generates response
6. Response is returned to user

---

## Benefits

* Reduces hallucination
* Uses enterprise knowledge
* Improves response accuracy
* Enables scalable knowledge systems
