# RAG_QA_CHATBOT 🤖📚

A Retrieval-Augmented Generation (RAG) based Question Answering Chatbot built using OpenAI's LLMs and Pinecone vector database. This intelligent assistant is designed to retrieve relevant knowledge from custom data sources and provide accurate, context-aware responses in real time.

---

## 🔍 Problem Statement

Traditional AI chatbots struggle with answering questions that require domain-specific knowledge not present in their training data. This project aims to solve that limitation by using **Retrieval-Augmented Generation (RAG)** — a technique that allows the model to pull relevant data from an external knowledge base before generating answers.

---

## 🎯 Project Goals

- Enable accurate, context-specific answers by integrating external document knowledge.
- Develop a scalable and production-ready QA bot for business use-cases.
- Explore the combination of semantic search (via Pinecone) and generative models (via OpenAI).

---

## 🧠 Tech Stack

| Component           | Technology                      |
|---------------------|----------------------------------|
| Language Model       | OpenAI GPT-4/GPT-3.5             |
| Vector Database      | Pinecone                        |
| Embeddings           | OpenAI Embeddings (`text-embedding-ada-002`) |
| Backend Framework    | Python + FastAPI/Flask (as applicable) |
| Frontend (optional)  | Streamlit / React (customizable) |
| Deployment           | Render / Vercel / Localhost     |

---

## ⚙️ Features

- 🔎 **Semantic Search**: Converts user query and documents into embeddings to find top-k relevant chunks.
- 🧾 **Custom Data Ingestion**: Upload your own documents (PDFs, text, or Markdown) to create a personalized knowledge base.
- 🗣️ **Contextual Answer Generation**: Combines retrieved information with prompts to produce accurate answers.
- 💾 **Vector Store Support**: Utilizes Pinecone for high-speed vector storage and retrieval.
- 🔐 **API Key Security**: Secure handling of OpenAI and Pinecone credentials using `.env`.

---

## 🛠️ How It Works

1. **Data Ingestion**  
   - Upload documents (PDF, TXT, MD)
   - Split into chunks
   - Generate embeddings
   - Store in Pinecone index

2. **Query Handling**  
   - User enters a query
   - Query is embedded and compared with stored vectors
   - Top-k similar chunks retrieved

3. **Response Generation**  
   - Retrieved context + user query → passed to OpenAI API
   - Generated answer returned to user

---

## 🚀 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/bhargavi1973/RAG_QA_CHATBOT.git
cd RAG_QA_CHATBOT
