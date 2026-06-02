# 🚀 AI Study Assistant (n8n + Telegram + Gemini + Google Sheets)

## 📌 Implementation Plan

This project is an AI-powered Telegram Study Assistant built using **n8n automation**, **Google Gemini AI**, and **Google Sheets logging**.

It follows an event-driven workflow where user messages are processed, analyzed by AI, stored for logging, and returned as Telegram replies.

---

## 🏗️ System Architecture

```

Telegram User
↓
Telegram Trigger (n8n)
↓
Set / Edit Fields (Data Cleaning)
↓
AI Agent (Google Gemini)
↓
Google Sheets (Logging System)
↓
Telegram Send Message (Response)

```id="arch2"

---

## ⚙️ Implementation Steps

### 1. 📩 Telegram Trigger (Input Layer)
- Captures incoming messages from Telegram users  
- Requires BotFather token  
- Extracted data:
  - message.text → user question  
  - message.chat.id → chat ID  
  - message.from.first_name → username  

---

### 2. ✏️ Data Cleaning (Set / Edit Fields Node)

Purpose: Normalize incoming data for processing.

Mapped fields:
- userMessage → message.text  
- chatId → message.chat.id  
- userName → message.from.first_name  

---

### 3. 🧠 AI Processing (Google Gemini AI)

Purpose: Generate intelligent educational responses.

Rules:
- Explain clearly and simply  
- Use examples when needed  
- Break down complex topics step-by-step  
- Keep responses structured and easy to understand  

---

### 4. 📊 Google Sheets Logging System

Purpose: Store all conversations for tracking and analytics.

Sheet Columns:
- Timestamp  
- UserName  
- Message  
- AI Response  

---

### 5. 📤 Telegram Send Message (Output Layer)

Purpose: Send AI response back to user.

Format:
```

🤖 AI Tutor:

{{AI Response}}

—
Powered by AI Study Assistant

```id="msg3"

---

## 🔄 Full Workflow Summary

```

Telegram Trigger
↓
Set Fields
↓
AI Agent (Gemini)
↓
Google Sheets Log
↓
Telegram Send Message (Reply)

```id="flow3"

---

## 🧠 AI Prompt (Core Logic)

```

You are Elio AI Study Assistant.

Your job:

* Explain concepts clearly and simply
* Use examples when helpful
* Keep answers short but informative
* Break down complex topics step-by-step

User question:
{{userMessage}}

```id="prompt4"

---

## ⚙️ Optional Enhancements

### 🧠 Memory System
- Store previous chats per user  
- Enable contextual learning  

### 🎯 Quiz Mode
- Generate practice questions  
- Provide instant feedback  

### 📚 Multi-Subject Expansion
- Math  
- Science  
- Coding  
- English  

### ⚠️ Error Handling
Fallback message:
```

Sorry, I couldn’t process your request. Please try again.

```id="err4"

### 📈 Analytics Upgrade
Use Google Sheets data for:
- Most asked questions  
- User activity tracking  
- Learning insights  

---

## 🧠 Skills Used in This Project

- ⚙️ n8n workflow automation  
- 🤖 AI integration using Google Gemini API  
- 💬 Telegram Bot API development  
- 📊 Google Sheets data logging  
- 🧩 JSON data handling and transformation  
- ☁️ REST API integration  
- 🔍 System design and debugging automation workflows  

---

## 📁 Project Structure

```

ai-study-assistant-n8n/
│
├── workflows/
│   └── telegram-ai-study-bot.json
│
├── docs/
│   ├── setup-guide.md
│   ├── architecture.png
│   └── node-details.md
│
├── README.md
└── .gitignore

```id="struct5"

---

## 🚀 Project Goal

To build a scalable AI-powered learning assistant that helps students understand topics quickly through Telegram while maintaining structured logs for analytics and improvement.

---

## 📜 License

MIT License — free to use and modify.
```

---
