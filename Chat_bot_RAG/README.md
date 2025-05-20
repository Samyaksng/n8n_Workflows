# 🤖 Chatbot with Retrieval-Augmented Generation (RAG)

This project offers a complete solution for developing an automated document ingestion and Retrieval-Augmented Generation (RAG) chatbot. By utilizing a no-code/low-code workflow created in n8n, users can effectively scrape content-rich websites, process the gathered data, and launch a semantic chatbot powered by OpenAI and LangChain.

## 📌 Features

- 🌐 Web Scraping - Extracts data from any site's XML sitemap

- 🧠 AI-Powered Processing - Uses OpenAI embeddings for semantic search.

- 🏪 Supabase Vector Store - Stores processed data for efficient retrieval.

- 🧾 Chat Memory - with PostgreSQL-based persistence

- 🤖 Chatbot Integration - Allows users to query any question related to website.

- 🔄 Automated Workflow - Runs seamlessly in an n8n environment.
---

## 🧩 Workflows Overview

### 🗂 Document Ingestion Flow

| Step                    | Description                                                             |
| ----------------------- | ----------------------------------------------------------------------- |
| **Manual Trigger**      | Manually starts the ingestion pipeline                                  |
| **HTTP Request**        | Fetches the website's sitemap (e.g., `https://example.com/sitemap.xml`) |
| **XML Parser**          | Parses the sitemap and extracts URLs                                    |
| **Split & Loop**        | Iterates over each extracted URL                                        |
| **Wait & Check**        | Ensures pages are scraped without errors                                |
| **Content Loader**      | Extracts textual data (Markdown/HTML) from each page                    |
| **Text Splitter**       | Splits content into 5000-character chunks                               |
| **Embedding Generator** | Uses OpenAI API to create vector embeddings                             |
| **Supabase Upload**     | Uploads content chunks and embeddings into Supabase’s `documents` table |

---

### 💬 Chat Interaction Flow

| Step                       | Description                                                 |
| -------------------------- | ----------------------------------------------------------- |
| **Chat Trigger**           | Receives user queries via webhook/chat UI                   |
| **Chat Memory**            | Stores and retrieves past user interactions (PostgreSQL)    |
| **LangChain Agent**        | Handles context-aware reasoning and tool usage              |
| **Supabase Vector Search** | Retrieves top matching content chunks using semantic search |
| **OpenAI LLM**             | Generates answers based on retrieved context and query      |

---


## 📦 Installation

### Clone the Repository
```bash
git clone https://github.com/Samyaksng/n8n_Workflows.git
cd Chat_bot_RAG
```
Deploy with Docker:
```bash
docker volume create n8n_data
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```
Access the editor at http://localhost:5678

Import the .json file workflow in n8n 

---


## ❤️ Contributing
PRs are welcome! Feel free to **fork** the repo and submit your improvements. 🔥

