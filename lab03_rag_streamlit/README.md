# RAG UI — deployed on Streamlit Cloud 🌟

The lab02 pipeline (LangChain + reranker) wrapped in a web UI and deployed publicly — a link anyone can open and test with their own PDF, no install required.

**Live app: _(URL added once deployed)_**

## What it does

- Sidebar PDF upload, Q&A area, sources shown with similarity scores
- Processing spinner + conversation history (`st.session_state`)
- API keys never touch the code — loaded via `st.secrets` on Streamlit Cloud, `.env` locally
- Deployed on Streamlit Cloud (free tier, GitHub login only)

## Why this matters

A link a recruiter can click and try themselves, live, with their own document, beats any amount of describing what the project does.

## Stack

Python 3.11 · Streamlit · LangChain · ChromaDB · sentence-transformers · Mistral API

## Recruiter demo

"Here's my RAG in production — upload your own PDF and try it right now." Share the link live. Nothing else needed.
