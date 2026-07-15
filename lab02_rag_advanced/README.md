# RAG advanced — reranker + RAGAS evaluation

Rebuilding the lab01 pipeline with LangChain, adding a reranking step, and replacing "it looks like it works" with actual numbers.

## What it does

- Same pipeline as lab01, rebuilt with LangChain — measuring how much boilerplate it removes
- Adds a CrossEncoder reranker (`ms-marco-MiniLM-L-6-v2`): retrieve 20 candidate chunks, rerank, keep the top 5
- A 20-question evaluation dataset (question, ground truth) built on the same PDF as lab01
- RAGAS metrics: faithfulness, answer relevancy, context recall, context precision
- Before/after comparison table (with vs. without reranker) across all 20 questions
- Written analysis of the 3 worst-performing questions and why they fail

## Why this matters

"It works" isn't a result a recruiter can evaluate. "Faithfulness went from 0.71 to 0.87 after adding a reranker" is.

## Stack

Python 3.11 · LangChain · sentence-transformers (CrossEncoder) · RAGAS · ChromaDB · Mistral API

## Recruiter demo

"My RAG scores faithfulness=X. Here's how I measured it and what I changed to improve it."
