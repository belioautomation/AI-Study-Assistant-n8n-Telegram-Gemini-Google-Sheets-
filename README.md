# 🤖 AI Study Assistant (n8n + Telegram + Gemini + Google Sheets)

An AI-powered Telegram study assistant built using **n8n automation**, **Google Gemini AI**, and **Google Sheets logging**.

This bot helps students learn faster by answering questions in a clear, simple, and structured way.

---

## 🚀 Features

- 📩 Telegram chatbot interface
- 🧠 AI-powered explanations (Google Gemini)
- 📊 Google Sheets logging system (chat history)
- ⚙️ Fully automated n8n workflow
- 🧩 Easy to extend (quiz mode, memory system, subjects, etc.)
- 🔁 Scalable automation architecture

---

## 🏗️ System Architecture
Telegram User
↓
Telegram Trigger (n8n)
↓
Set / Edit Fields (Data Cleaning)
↓
AI Agent (Google Gemini)
↓
Google Sheets (Logging)
↓
Telegram Send Message (Response)

---

## 📁 Project Structure
ai-study-assistant-n8n/
ai-study-assistant-n8n/
│
├── workflows/
│ └── telegram-ai-study-bot.json
│
├── docs/
│ ├── setup-guide.md
│ ├── architecture.png
│ └── node-details.md
│
├── README.md
└── .gitignore

---

## ⚙️ Requirements

Before starting, make sure you have:

- n8n installed (cloud or self-hosted)
- Telegram Bot Token (from BotFather)
- Google Gemini API Key
- Google Sheets account (for logging)
- Google Cloud credentials (for Sheets integration)

---

## 🔧 Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ai-study-assistant-n8n.git
cd ai-study-assistant-n8n

🧠 Skills Used in This Project
⚙️ n8n Automation
Workflow design and orchestration
Multi-step automation pipelines (Trigger → AI → Storage → Response)
🤖 AI Integration
Google Gemini API integration
Prompt engineering for educational responses
Structuring AI outputs for chatbot use
💬 Telegram Bot Development
Telegram Bot API setup and configuration
Real-time message handling
Chat-based interaction flow
📊 Data Logging & Storage
Google Sheets API integration
Structured logging (Timestamp, User, Message, AI Response)
Basic dataset creation for analytics
🧩 Backend Logic & Data Handling
JSON transformation and mapping
Data normalization using Set/Edit Fields nodes
Workflow-based backend logic design
☁️ APIs & Cloud Services
REST API usage (Google Gemini endpoint)
OAuth authentication (Google Sheets)
Third-party service integration
🔍 System Design & Problem Solving
Designing scalable AI chatbot architecture
Debugging and optimizing n8n workflows
Connecting multiple services into one automated system

---

If you want next level upgrade, I can also create:

- 🔥 a **professional GitHub repo with badges + UI screenshots**
- 🧠 a **production-ready n8n JSON workflow (fixed + optimized)**
- 📊 a **Google Sheets analytics dashboard**
- 🤖 or a **multi-agent AI tutor system (advanced)**
