#  NFL RAG + Agent App

![App Preview](images/RAG-Agent-Preview.png)

Built a hybrid AI system that combines a custom NFL statistics RAG database with web search and tool-based reasoning.

---

##  Features
- Custom RAG system using NFL data (ChromaDB + LlamaIndex)
- Persistent vector database for fast querying
- Agent with tool usage:
  - NFL database search (primary)
  - Web search fallback
  - Calculator tools
- Streamlit web app interface

---

##  How it works
1. Queries NFL stats from local ChromaDB
2. Falls back to web search if data not found
3. Uses tools for calculations when needed

---

##  Tech Stack
- Python
- LlamaIndex
- Ollama (qwen2.5)
- ChromaDB
- Streamlit

---

##  Key Insight
- RAG performance depends heavily on data formatting
- Poor structure leads to incorrect retrieval
- Agents may still produce incorrect answers if tools return weak data
- Model choice impacts accuracy (qwen2.5 performed best)

---

##  How to Run (on Mac)
cd ~ NFL-Stats-RAG-System

python3.11 -m venv venv
source venv/bin/activate

pip install -r requirements.txt

python3.11 -m streamlit run PolicyApp.py
