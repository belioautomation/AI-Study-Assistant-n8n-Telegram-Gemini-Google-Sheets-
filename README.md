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
* Telegram Bot API
* Google Gemini AI
* Google Sheets API
* JavaScript

---

# 📂 Workflow

```text
Telegram User
      │
      ▼
Telegram Trigger
      │
      ▼
Set (Edit Fields)
      │
      ▼
AI Agent (Google Gemini)
      │
      ▼
Google Sheets (Append Row)
      │
      ▼
Telegram (Send Message)
```

---

# ⚙️ Workflow Explanation

## 1. Telegram Trigger

Monitors incoming Telegram messages.

Extracted data:

* User Message
* Chat ID
* User Name

---

## 2. Set (Edit Fields)

Prepares the incoming data before sending it to the AI.

Mapped fields:

| Field       | Source                  |
| ----------- | ----------------------- |
| userMessage | message.text            |
| chatId      | message.chat.id         |
| userName    | message.from.first_name |

---

## 3. AI Agent (Google Gemini)

Google Gemini analyzes the user's question and generates an educational response.

Prompt responsibilities:

* Explain concepts clearly
* Keep responses concise
* Use examples when appropriate
* Break complex topics into simple steps
* Maintain a friendly educational tone

Example Prompt:

```text
You are an AI Study Assistant.

Explain concepts clearly and simply.
Use examples when appropriate.
Keep answers concise.
Break difficult topics into smaller steps.

User Question:
{{userMessage}}
```

---

## 4. Google Sheets

Automatically stores every conversation for future reference.

Columns:

| Timestamp | User Name | User Message | AI Response |

---

## 5. Telegram

Sends the AI-generated response back to the user.

Example:

```text
🤖 AI Study Assistant

CPU stands for Central Processing Unit.

It is considered the "brain" of the computer because it processes instructions and performs calculations.

Example:
When you open a web browser, the CPU executes the instructions required to launch the application.

Powered by Google Gemini.
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
├── screenshots/
│   ├── workflow.png
│   ├── telegram-trigger.png
│   ├── set-node.png
│   ├── ai-agent.png
│   ├── google-sheets.png
│   ├── telegram-response.png
│   └── workflow-execution.png
│
└── assets/
    └── sample-conversation.txt
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

# 🎯 Skills Demonstrated

* AI Workflow Automation
* AI Chatbot Development
* Telegram Bot Development
* Google Gemini Integration
* Google Sheets Automation
* Prompt Engineering
* Workflow Automation
* Event-Driven Automation
* JavaScript Data Processing
* No-Code / Low-Code Development

---

# 🚀 Future Improvements

* Add conversation memory
* Support voice messages
* Generate quizzes automatically
* Analyze PDF study materials
* Support multiple languages
* Personalized learning recommendations
* Student progress dashboard
* Integration with Notion

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Belio C. Sinangote**

BS Information Technology Student
Cebu Technological University (CTU)

**GitHub:** https://github.com/belioautomation

This project is part of my **30-Day n8n Automation Portfolio**, showcasing practical workflow automation using **n8n**, AI integrations, APIs, and business process automation.
