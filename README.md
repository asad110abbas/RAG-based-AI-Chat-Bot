# 🧠 BRIHA · KnowledgeBot (RAG AI Chatbot)

![Part of BRIHA](https://img.shields.io/badge/Part_of-BRIHA-8B5CF6?style=for-the-badge&labelColor=0B1024)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=white) ![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6F00?style=flat-square) ![Gradio](https://img.shields.io/badge/Gradio-F97316?style=flat-square)

> ⚡ **Part of [BRIHA](https://github.com/asad110abbas)** · Briha Research, built by Syed Asad Abbas.

A **retrieval-augmented generation (RAG)** chatbot that answers questions from your own documents.
Drop in a `.docx` FAQ and chat with it through a Gradio web UI.

## Architecture
```mermaid
flowchart LR
    D[FAQ .docx] --> S[Split into chunks]
    S --> E[Hugging Face embeddings]
    E --> V[(Chroma vector store)]
    Q[User question] --> R[Retriever: top-k chunks]
    V --> R
    R --> P[LangChain prompt]
    P --> L[OpenAI GPT-5-mini]
    L --> A[Grounded answer in Gradio UI]
```

## Highlights
- **LangChain** pipeline for loading, chunking, retrieval and prompting
- **Local embeddings** (Hugging Face) + **Chroma** vector search
- **Grounded answers** from OpenAI GPT-5-mini, using retrieved context only
- **Gradio** chat interface, running in one command

## Run
```bash
pip install langchain langchain-community langchain-openai langchain-huggingface chromadb python-docx gradio
export OPENAI_API_KEY="your-key"
python "RAG BASED AI CHATBOT.py"
```
