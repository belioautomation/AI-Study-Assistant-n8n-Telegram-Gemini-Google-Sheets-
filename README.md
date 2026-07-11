# 📄 AI Study Assistant using n8n

An AI-powered educational chatbot built with **n8n**, **Google Gemini AI**, **Telegram Bot API**, and **Google Sheets**. This workflow automatically receives questions from Telegram users, generates intelligent educational responses using Google Gemini, logs every conversation into Google Sheets, and replies instantly through Telegram.

Designed as part of my **30-Day n8n Automation Portfolio**, this project demonstrates how AI can automate educational assistance using low-code workflow automation.

---

# 📌 Features

* 🤖 AI-powered study assistant using Google Gemini
* 💬 Receives questions through Telegram
* 📚 Generates clear and educational responses
* 📊 Automatically logs conversations to Google Sheets
* ⚡ Fully automated workflow built with n8n
* 📝 Tracks learning history for analytics
* ☁️ Event-driven automation
* 🔄 Scalable and customizable workflow

---

# 🛠 Technologies Used

* n8n
* Telegram Trigger
* Set (Edit Fields)
* Google Gemini AI
* Google Sheets API
* Telegram Bot API

---

# 📂 Workflow

```text
Telegram User
      │
      ▼
Telegram Trigger
      │
      ▼
Set / Edit Fields
      │
      ▼
AI Agent (Google Gemini)
      │
      ▼
Google Sheets
      │
      ▼
Telegram Send Message
```

---

# ⚙️ Workflow Explanation

## 1. Telegram Trigger

Monitors incoming messages from Telegram users.

**Extracted Data**

* User Message
* Chat ID
* User Name

---

## 2. Set / Edit Fields

Prepares and organizes the incoming data before sending it to the AI.

**Mapped Fields**

| Field       | Source                  |
| ----------- | ----------------------- |
| userMessage | message.text            |
| chatId      | message.chat.id         |
| userName    | message.from.first_name |

---

## 3. AI Agent (Google Gemini)

Google Gemini analyzes the user's question and generates an educational response.

### AI Instructions

* Explain concepts clearly.
* Keep answers simple and concise.
* Use examples when appropriate.
* Break complex topics into smaller steps.
* Respond in a friendly educational tone.

### Prompt

```text
You are Elio AI Study Assistant.

Your job:

- Explain concepts clearly and simply.
- Use examples when helpful.
- Keep answers concise but informative.
- Break down difficult topics step-by-step.

User Question:

{{userMessage}}
```

---

## 4. Google Sheets

Automatically stores every conversation for monitoring and future analysis.

### Logged Data

| Column       |
| ------------ |
| Timestamp    |
| User Name    |
| User Message |
| AI Response  |

---

## 5. Telegram

Sends the AI-generated response back to the user.

### Example Response

```text
🤖 AI Tutor

CPU stands for Central Processing Unit.

It is considered the "brain" of the computer because it processes instructions and performs calculations.

Example:
When you open Google Chrome, the CPU executes the instructions needed to launch the application.

—
Powered by AI Study Assistant
```

---

# 📊 Google Sheets Structure

| Timestamp | User Name | User Message | AI Response |
| --------- | --------- | ------------ | ----------- |

---

# 📁 Repository Structure

```text
AI-Study-Assistant/
│
├── README.md
├── workflow.json
│
└── screenshots/
    ├── workflow.png
    ├── telegram-trigger.png
    ├── set-node.png
    ├── ai-agent.png
    ├── google-sheets.png
    ├── telegram-response.png
    └── workflow-execution.png
```

---

# 📷 Screenshots

Include the following screenshots:

* Complete Workflow
* Telegram Trigger
* Set Node
* AI Agent Output
* Google Sheets Results
* Telegram Response
* Workflow Execution

---

# 🎯 Learning Objectives

This project demonstrates:

* Telegram Bot Automation
* AI Chatbot Development
* Google Gemini AI Integration
* Prompt Engineering
* Google Sheets Automation
* Event-Driven Workflows
* Data Transformation using n8n
* AI-Powered Educational Assistance

---

# 🚀 Possible Improvements

* 🧠 Conversation memory
* 📚 Multi-subject tutoring
* 🎯 Quiz generation
* 📈 Student learning analytics
* 🌍 Multi-language support
* 🔊 Voice message support
* 📎 PDF document analysis
* 📝 Assignment and homework assistance
* 🎓 Personalized learning recommendations

---

# 📄 License

This project is licensed under the **MIT License**.

---

# 🙌 Acknowledgements

* n8n
* Google Gemini AI
* Telegram Bot API
* Google Sheets API
