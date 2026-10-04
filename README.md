# RAG

This repository is a hands-on exploration of Retrieval-Augmented Generation (RAG) patterns using Python, LangChain, and modern vector stores. It contains Jupyter notebooks for document ingestion, text and PDF processing, embedding-based retrieval, and agentic workflows with multiple model providers.

## What this project demonstrates

- Building a basic RAG pipeline with LangChain
- Loading text and PDF documents into retrieval systems
- Chunking and embedding content for semantic search
- Using vector databases such as FAISS, Chroma, and Typesense
- Integrating MongoDB-based retrieval and metadata filtering
- Working with agentic workflows using LangGraph
- Connecting to LLM providers such as OpenAI, Gemini, and Groq

## Repository structure

- `notebook/` – Jupyter notebooks covering the main RAG flows
  - `agenticRag.ipynb` – agentic RAG experimentation
  - `agenticRagWithMongodb.ipynb` – MongoDB-backed agentic retrieval
  - `documents.ipynb` – sample document ingestion and data setup
  - `LLM.ipynb` – LLM integration and advanced pipeline patterns
  - `typesense.ipynb` – Typesense vector search example
- `data/` – sample datasets, text files, PDFs, and vector-store outputs
- `src/rag/` – Python package scaffold for the project
- `requirements.txt` and `pyproject.toml` – dependency definitions
- `.env` – local environment variables for model API keys

## Tech stack

- Python 3.14+
- LangChain / LangGraph
- LangChain community integrations
- sentence-transformers
- FAISS / ChromaDB / Typesense
- PyMuPDF / PyPDF
- MongoDB-oriented examples
- OpenAI, Google Gemini, Groq APIs

## Setup

1. Create a virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate   # macOS/Linux
   .venv\Scripts\activate      # Windows
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   or, if you use `uv`:

   ```bash
   uv sync
   ```

3. Add your API keys to a local `.env` file. Example variables include:

   ```env
   OPENAI_API_KEY=your_key_here
   GEMINI_API_KEY=your_key_here
   GROQ_API_KEY=your_key_here
   ```

4. Open the notebooks in `notebook/` and run them in order as needed.

## Typical workflow

1. Add or prepare documents in `data/`
2. Load them in a notebook with LangChain document loaders
3. Split text into chunks and create embeddings
4. Store embeddings in a vector store or retrieval backend
5. Query the retriever with user prompts
6. Send the retrieved context to an LLM for grounded responses

## Notes

This project is primarily notebook-driven and intended for learning and prototyping. It is not a production-ready application framework by itself, but it provides a solid foundation for experimenting with retrieval pipelines, embeddings, and agentic RAG systems.

## License

This project does not currently declare a repository license in the source metadata. If you plan to distribute or reuse it, confirm the intended licensing terms before publishing.
