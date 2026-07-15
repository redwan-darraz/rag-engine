# rag-engine

Building a Retrieval-Augmented Generation pipeline from the ground up — starting with zero abstractions to understand what LangChain actually does under the hood, then rebuilding with LangChain, a reranker, and rigorous RAGAS evaluation, and finally shipping it as a publicly deployed app.

## Labs

### LAB 3.1 — RAG From Scratch, No LangChain

PDF extraction, three chunking strategies compared, local embeddings, ChromaDB vector search, and a full query pipeline with cited sources — no framework, just the raw mechanics. → [`lab01_rag_scratch/`](lab01_rag_scratch/)

### LAB 3.2 — Reranker + RAGAS Evaluation

Rebuilding the same pipeline with LangChain, adding a CrossEncoder reranker, and measuring it rigorously with RAGAS (faithfulness, answer relevancy, context recall/precision) instead of eyeballing it. → [`lab02_rag_advanced/`](lab02_rag_advanced/)

### LAB 3.3 — Deployed Streamlit App 🌟

The full pipeline (with reranker) wrapped in a Streamlit UI, deployed publicly on Streamlit Cloud. Upload a PDF, ask questions, see the sources. → [`lab03_rag_streamlit/`](lab03_rag_streamlit/)

**Live demo: _(URL added once deployed)_**

## Projects

### ask-my-notes — RAG on Your Own Notes

The same pipeline pointed at a personal notes folder instead of a single PDF, with automatic re-indexing on file changes and a CLI for quick questions. → [`projects/ask_my_notes/`](projects/ask_my_notes/)

## Stack

Python 3.11 · PyMuPDF · sentence-transformers · ChromaDB · LangChain · RAGAS · Streamlit · Mistral API

## Resources

- [Mistral API docs](https://docs.mistral.ai/)
- [LangChain documentation](https://python.langchain.com/)
- [RAGAS documentation](https://docs.ragas.io/)
