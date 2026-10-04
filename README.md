# Project 1 — RAG Q&A Chatbot

Build a production-quality question-answering chatbot that retrieves from a document corpus and generates grounded answers with citations. This is the foundational LLM project — every technique you learn here transfers to more complex systems.

## What you'll build

A FastAPI service that:
- Ingests PDF and markdown documents into a persistent ChromaDB vector store
- Retrieves the top-5 most relevant chunks for each user question
- Generates a cited answer using gpt-4o-mini
- Streams the response token-by-token via SSE
- Caches deterministic answers to reduce cost
- Exposes a `/health` and `/stats` endpoint for monitoring




## Tech stack

```
openai==1.51.0
chromadb==0.5.15
fastapi==0.115.0
uvicorn==0.30.6
pydantic==2.9.0
pymupdf==1.24.11
sentence-transformers==3.1.1  # for cross-encoder reranking
httpx==0.27.2
ragas==0.2.3
```

## Result

By the end of this project you will have a working, evaluated, deployable RAG service  with measurable accuracy and latency numbers.
