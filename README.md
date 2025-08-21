# AskYourPDF
Streamlit app to upload single or multiple PDFs and chat to get concise, context-grounded answers.  Uses Retrieval-Augmented Generation (RAG) with history awareness to handle follow-up questions accurately.  Suited for research papers, manuals, policies, contracts, reports, and textbooks.
Streamlit app to upload single or multiple PDFs and chat to get concise, context-grounded answers.

Uses Retrieval-Augmented Generation (RAG) with history awareness to handle follow-up questions accurately.

Suited for research papers, manuals, policies, contracts, reports, and textbooks.

Features:

Multi-file PDF upload and processing.

Semantic chunking (5,000 chars, 500 overlap) and embeddings for precise retrieval.

Local vector index for fast, on-device search.

History-aware retriever that reformulates follow-ups into standalone questions.

LLM answers constrained to three sentences for clarity and brevity.

Honest fallback: clearly says “don’t know” when context is insufficient.

Session-based chat: unique session IDs with in-memory history per session.

Architecture:

PDF parsing via PyPDF loader.

RecursiveCharacterTextSplitter for chunking.

HuggingFace embeddings (all-MiniLM-L6-v2).

Chroma for vector storage and retrieval.

RAG “stuff” chain to pass retrieved context into the answer prompt.

API key entered at runtime; optional .env for tokens (e.g., HF).

Getting started:

Clone repo, install dependencies.

Optionally set environment variables (.env).

Run Streamlit app.

Enter model API key, choose or keep default session ID.

Upload PDFs and start asking questions.

UI flow:

Fields for API key and session ID.

Multi-file uploader.

Chat input for questions.

Inline display of responses and chat history.

Benefits:

Rapid, reliable answers sourced directly from user documents.

Reduced time spent scanning long PDFs.

Simple, local indexing ideal for demos, personal workflows, and internal assistants.

Design principles:

Reliability via retrieval grounding.

Brevity via strict answer-length prompt.

Transparency via visible chat history and context-driven responses.
