# RAG from scratch — no LangChain

Building the full retrieval-augmented generation loop by hand: extract text from a PDF, split it into chunks, turn chunks into vectors, search those vectors, and feed the best matches to an LLM alongside the question. The goal is to come out the other side knowing exactly what LangChain abstracts away.

## What it does

- Extracts text from a public PDF with PyMuPDF
- Implements three chunking strategies from scratch: fixed-size, sentence-based, and semantic — compared side by side
- Generates embeddings locally with `all-MiniLM-L6-v2` (sentence-transformers), no API calls needed for this step
- Stores and searches vectors with ChromaDB (cosine similarity)
- Full query pipeline: question → embedding → top-5 chunks → prompt → Mistral → answer with cited sources
- Tested against 10 real questions, including failure cases and why they fail

## Why this matters

Every RAG tutorial reaches straight for LangChain. Building the loop by hand once means every LangChain abstraction later has a name and a mental model behind it, instead of being magic.

## Stack

Python 3.11 · PyMuPDF · sentence-transformers · ChromaDB · Mistral API

## Recruiter demo

Upload a PDF live, ask 3 questions, show that the cited sources are real passages from the document.
