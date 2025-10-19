# 🤖 RAG Pipeline + Chatbot using n8n

This project demonstrates how to build a **Retrieval-Augmented Generation (RAG) chatbot** powered by **n8n automation** and **LLM integration**.

---

## 🚀 Overview

This automation pipeline:
- Extracts FAQ data from knowledge sources  PDFs, DOCS 
- Embeds text chunks using OpenAI 
- Stores embeddings in a vector database Pinecone Vector Store 
- Answers user  FAQ queries with relevant context

---

## 🧩 Tools Used
- **n8n** — workflow automation
- **OpenAI API** — for embeddings and completions
- **Pinecone** — vector database
---

## ⚙️ Workflow Structure

Below is the flow diagram from n8n:

![n8n Workflow](https://github.com/MubeenaHussain/AUTOMATION-PROJECTS/blob/main/Screenshot%202025-10-19%20210100.png)


---

## 🧠 How It Works

1. User uploads or specifies a FAQ source.  
2. n8n splits the text and sends to embedding node.  
3. Vector DB stores embeddings.  
4. When a question is asked, it retrieves context.  
5. Sends both context + question to LLM → returns the answer.

---

## 🧰 Files

| File | Description |
|------|--------------|
| `workflow_files/rag_chatbot.json` | n8n workflow export |
| `images/rag-pipeline-flow.png` | architecture diagram |
| `README.md` | documentation (this file) |

---

## 📸 Screenshots

Add visuals here 👇

![Chatbot Demo](images/chatbot-demo.png)


---

## 🧕MUBEENA HUSSAIN
mubeenahussain1205@gmail.com  
📧 your.email@example.com

