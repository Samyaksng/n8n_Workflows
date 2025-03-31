# 🚀 Reddit Automation Workflow with n8n

## 📌 Overview
This **n8n workflow** automates the process of fetching Reddit posts, storing them in a database, analyzing comments, generating AI-based responses using OpenAI, and replying to comments automatically.

## 🛠️ Features
- 🔍 **Fetch posts** from Reddit based on a search query.
- 🗄️ **Store posts** in a PostgreSQL database.
- 💬 **Retrieve comments** from Reddit posts.
- 🤖 **Generate AI responses** using OpenAI.
- ✉️ **Auto-reply** to comments on Reddit.

## 🏗️ Workflow Steps
1. **🔔 Trigger:** Initiates on receiving a chat message.
2. **🔎 Search Reddit:** Queries Reddit for posts based on the given input.
3. **📥 Store Data:** Saves retrieved posts into PostgreSQL.
4. **📝 Get Comments:** Fetches comments from a specific post.
5. **💡 Generate AI Response:** Uses OpenAI to create a reply.
6. **📢 Post Reply:** Sends the AI-generated response back to Reddit.

## ⚙️ Setup Instructions
### 🔧 Prerequisites
- n8n installed and configured
- Reddit API credentials (Client ID & Secret)
- PostgreSQL database
- OpenAI API key



## 🔄 Usage
- Send a chat message to trigger the workflow.
- Monitor logs to see real-time interactions.
- Review database entries to track stored posts.

## 🛠 Troubleshooting
- ❌ **API Errors:** Ensure API keys are correct and have the necessary permissions.
- ⚠️ **Rate Limits:** Reddit and OpenAI have rate limits; consider delays between API calls.
- 🗄 **Database Issues:** Check PostgreSQL connection settings.

## 🤝 Contributing
Pull requests are welcome! 🚀 If you find any bugs or want to improve the workflow, feel free to contribute.

## 📜 License
This project is licensed under the **MIT License**.

---

### 🎯 Happy Automating! 🚀


