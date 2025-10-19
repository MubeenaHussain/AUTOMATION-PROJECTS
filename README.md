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
| ![WORKFLOW JSON FORMAT](https://github.com/MubeenaHussain/AUTOMATION-PROJECTS/blob/main/RAG%20PIPELINE%20%20AND%20CHATBOT.json) | n8n workflow export |
| ![README.md](https://github.com/MubeenaHussain/AUTOMATION-PROJECTS/blob/main/README.md)                                         | documentation (this file) |

---
---


# 2. 🤖 Automated Customer Support Workflow

This project showcases an ** Customer Support Automation Workflow** built using **n8n**, integrating **Gmail**, **OpenRouter LLMs**, **Pinecone**, and **OpenAI embeddings** to deliver intelligent and context-aware replies to customer queries.

---

## 🧩 Workflow Overview

The automation listens to **incoming Gmail messages**, classifies the type of query, routes it through the appropriate **AI model**, and automatically generates a **personalized reply** using contextual memory and vector search.

### 🔧 Workflow Components

| Node | Description |
|------|--------------|
| **Gmail Trigger** | Detects incoming customer emails in real time. |
| **Text Classifier** | Classifies messages as “Customer Support” or “Other”. |
| **OpenRouter Chat Model 1** | First-level LLM used for text classification. |
| **AI Agent 1** | Main chatbot that crafts context-aware responses. |
| **Pinecone Vector Store** | Stores embeddings for semantic search and contextual memory. |
| **OpenAI Embeddings** | Generates embeddings for Pinecone database. |
| **OpenRouter Chat Model 2** | Secondary LLM for refined contextual reasoning. |
| **Reply to Message** | Sends AI-generated responses back to the customer via Gmail. |

---

## 🧠 Workflow Logic

1. **Trigger:** Gmail node activates on new email.  
2. **Classification:** Message text is classified as “Support” or “Other.”  
3. **Routing:**
   - If *Support*: AI Agent processes with contextual search.  
   - If *Other*: The flow stops (“No Operation” node).  
4. **Context Retrieval:**  
   - Embeddings from OpenAI → stored in Pinecone Vector DB.  
   - Relevant context retrieved for response generation.  
5. **Response Generation:**  
   - OpenRouter Model creates human-like replies using context.  
   - Reply node sends message via Gmail API.

---

## 🧭 Workflow Diagram

![Customer Support Workflow](images/customer-support-workflow.png)


---

## 🧰 Tech Stack

| Tool | Purpose |
|------|----------|
| **n8n** | Workflow automation engine |
| **Gmail API** | Email trigger and response |
| **OpenRouter LLMs** | Language model for classification and replies |
| **Pinecone** | Vector database for storing embeddings |
| **OpenAI API** | Text embedding generation |
| **AI Agent (n8n)** | Main reasoning agent |

---

## ⚙️ Setup Instructions

1. Import the `.json` workflow into your **n8n** instance.
2. Configure the following credentials:
   - Gmail API connection
   - OpenRouter API Key
   - OpenAI API Key
   - Pinecone API Key
3. Adjust model parameters or memory settings as needed.
4. Activate the workflow — incoming support emails will now get **automatic intelligent responses**.

---

## 🚀 Use Cases

- AI-powered **Customer Support Automation**
- **Contextual email reply generation**
- Integration with CRM or support ticket systems
- Scalable multi-model AI response handling

---

## 📸 Example Output

> Incoming: “Hi, my order hasn’t arrived yet.”  
>  
> AI Reply: “Hello! I’m sorry to hear about your delay. Could you please share your order ID? I’ll check the status immediately.”

---




## 🧕MUBEENA HUSSAIN
 

