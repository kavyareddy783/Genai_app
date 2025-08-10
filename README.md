# GenAI Hands-on Project — LangChain & Ollama Integration

A hands-on Generative AI project integrating **OpenAI API**, **Ollama**, **LangChain**, and **LangGraph** to build agentic AI workflows, experiment with LLMs, and understand the foundations of modern AI application development.

---

## 🚀 Features
- **OpenAI API Integration** — Make API calls to GPT models for text generation.
- **Ollama Integration** — Run local LLMs for offline experimentation.
- **LangChain Workflows** — Build chains, tools, and agents for modular AI systems.
- **LangGraph Basics** — Design stateful, graph-based AI workflows.
- **Modular Codebase** — Extend and modify easily for your own projects.

---

## 📖 Retrieval-Augmented Generation (RAG) Overview

This project includes a **RAG pipeline** that boosts the accuracy and relevance of AI answers by combining **your data** with LLM capabilities.

**How it works:**

1. **Data Sources & Document Loaders**  
   Ingest content from multiple sources:
   - Websites (Web Loader)
   - PDFs (PDF Loader)
   - JSON/Text files, or any structured/unstructured documents  
   These loaders pull the raw text into the pipeline.

2. **Data Ingestion & Chunking**  
   The text is broken down into **smaller chunks** to improve:
   - Embedding quality  
   - Retrieval accuracy

3. **Embedding Creation**  
   Each chunk is transformed into a **vector** using:
   - **OpenAI Embeddings** (cloud)
   - **Ollama Embeddings** (local)

4. **Vector Storage (Vector DB)**  
   Store embeddings in:
   - **ChromaDB** (uses SQLite by default)
   - **FAISS** for optimized similarity search

5. **Retrieval Chain**  
   When you ask a question:
   - The system **searches** the vector database for the most relevant chunks.
   - Injects those chunks into a **prompt template** alongside your query.
   - Passes everything to the LLM for a grounded, context-aware answer.

6. **Final Output**  
   The LLM responds using **both** the retrieved context and its own reasoning, giving you:
   - More accurate responses
   - Data-backed answers
   - Reduced hallucinations

**In short:**  
RAG lets your AI “look up” facts in your own data before answering — like giving it a private, super-fast library to consult.


---

## 📦 Tech Stack
- **Python 3.10+**
- [LangChain](https://www.langchain.com/)
- [LangGraph](https://langchain-ai.github.io/langgraph/)
- [Ollama](https://ollama.ai/)
- [OpenAI API](https://platform.openai.com/)
- Additional dependencies listed in `requirements.txt`

---


---

## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>

2.**Create a virtual environment**

```
   python -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scripts\activate      # Windows
```

3. **Install dependencies**

   ```
    pip install -r requirements.txt
   ```

4. **Set environment variables**

    ```
    Create a .env file in the project root:
    OPENAI_API_KEY=your_openai_api_key

    ```

