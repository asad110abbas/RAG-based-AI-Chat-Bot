# KnowledgeBot AI Chat

![Part of BRIHA](https://img.shields.io/badge/Part_of-BRIHA-8B5CF6?style=for-the-badge&labelColor=0B1024)

> ⚡ **Part of [BRIHA](https://github.com/asad110abbas)**, built by Syed Asad Abbas.

KnowledgeBot is an AI-powered chatbot built using **LangChain**, HuggingFace embeddings, and OpenAI GPT-5-mini. It can answer questions from your own FAQ or document collection using retrieval-augmented generation (RAG) and provides a clean, interactive Gradio interface.

## Features

- Uses **LangChain** for document retrieval and prompt management.
- Supports custom FAQs in `.docx` format.
- Vector search with HuggingFace embeddings and Chroma.
- Generates responses using OpenAI GPT-5-mini.
- Interactive Gradio UI for easy chatting.

## Setup


```bash
git clone <repo-url>
cd <repo-name>

pip install -r requirements.txt
python app.py
export OPENAI_API_KEY="your_api_key_here"
