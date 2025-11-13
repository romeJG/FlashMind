# ⚡ FlashMind AI Flashcard Bot
Turn any PDF into interactive flashcards and quizzes directly from Telegram using unlimited free AI prompts via OpenRouter.

---

## 🧠 Overview

**FlashMind** is an AI-powered Telegram bot that converts uploaded PDF files into **multiple-choice flashcards** and interactive quizzes.

It uses **n8n** as the automation brain, **OpenRouter** for free AI inference, and a custom **HTML/JS quiz engine** for delivery all without any external backend or paid API costs.

---
> ⚠️ **Note:**  
> This project is fully functional but currently **not operational** since it depends on my local **n8n instance** being online.  
> You can still explore the workflow JSON, screenshots, architecture, and code to see how it all works end-to-end.
---

## 📸 Screenshots

![Answered](assets/answered.jpeg)
![Flipped](assets/fliped.jpeg)
![n8n Flow](assets/n8n-flow.jpeg)
![Sample Conversation](assets/sample-convo.jpeg)



## 🏗️ Architecture

```mermaid
flowchart TB
    A[Telegram User Uploads PDF] --> B[n8n Telegram Trigger]
    B --> C[Extract From File Node]
    C --> D[AI Agent using LangChain and OpenRouter]
    D --> E[JSON Validation and Retry Logic]
    E --> F[Code Node - Builds Interactive HTML Flashcards]
    F --> G[Telegram Sends Flashcards Back to User]
```
