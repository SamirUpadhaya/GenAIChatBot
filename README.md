# GenAIChatBot 📚

**GenAIChatBot** is an AI-powered PDF-based question-answering application.  
Upload your PDF notes or documents, and ask natural-language questions. The bot returns context-aware answers using semantic search + an LLM backend.

---

## 🚀 What it Does

- Accepts a **PDF file upload** (e.g. lecture notes, book, document).  
- Extracts text from the PDF.  
- Splits text into manageable “chunks” for semantic processing.  
- Converts chunks into vector embeddings (via OpenAI Embeddings).  
- Stores embeddings in a **FAISS** vector database for fast similarity search.  
- On user query: finds relevant chunks, feeds them to an LLM (e.g. GPT-3.5-turbo), and returns the best answer.  
- Provides an interactive, simple UI using **Streamlit**.

---

## 🧰 Tech Stack

- Python  
- Streamlit — Web UI & user interface  
- LangChain (classic + community) — for document management, splitting, vector store & chain orchestration  
- PyPDF2 — PDF text extraction  
- FAISS — Vector store for semantic search  
- OpenAI API — embeddings & LLM backend  

---

## 📥 How to Install & Run

```bash
pip install streamlit PyPDF2 langchain-openai langchain-text-splitters langchain-community langchain-core faiss-cpu
streamlit run notebot_app.py
