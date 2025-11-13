# ⚡ FlashMind — AI Flashcard Bot

> Turn any PDF into interactive flashcards and quizzes — directly from Telegram using unlimited free AI prompts via OpenRouter.

---

## 🧠 Overview

**FlashMind** is an AI-powered Telegram bot that converts uploaded PDF files into **multiple-choice flashcards** and interactive quizzes.

It uses **n8n** as the automation brain, **OpenRouter** for free AI inference, and a custom **HTML/JS quiz engine** for delivery — all without any external backend or paid API costs.

---

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
