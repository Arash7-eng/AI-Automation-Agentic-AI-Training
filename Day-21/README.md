# 🤖 Day 21 – AutoGen AI Projects with Google Gemini 3.5 Flash

![Python](https://img.shields.io/badge/Python-3.12-blue)
![AutoGen](https://img.shields.io/badge/AutoGen-0.7.5-green)
![Gemini](https://img.shields.io/badge/Google-Gemini%203.5%20Flash-orange)
![License](https://img.shields.io/badge/License-Educational-red)

---

# 📌 Overview

This repository contains two AI-powered applications built using **Microsoft AutoGen**, **Google Gemini 3.5 Flash**, and **Python**.

These projects demonstrate how multiple AI agents can collaborate to solve programming tasks and automate customer support using intelligent ticket classification.

---

# 🚀 Project 1 – Multi-Agent AI System

## 📖 Description

This project demonstrates a collaborative AI workflow using AutoGen.

Three AI agents work together to complete a programming task.

### 👥 Agents

### 📝 Planner

- Understands the task
- Breaks it into logical steps
- Creates an execution plan

### 💻 Developer

- Reads the Planner's instructions
- Generates clean Python code
- Implements the complete solution

### ✅ Reviewer

- Reviews the generated code
- Suggests improvements
- Verifies correctness
- Ends the conversation with **TERMINATE**

---

## Workflow

```
User Task
     │
     ▼
 Planner Agent
     │
     ▼
 Developer Agent
     │
     ▼
 Reviewer Agent
     │
     ▼
 Final Solution
```

---

## Features

- Multi-Agent Collaboration
- Task Planning
- Python Code Generation
- Code Review
- AutoGen RoundRobinGroupChat
- Gemini 3.5 Flash Integration

---

## Sample Task

```
Create a Python program to check whether a number is prime.
```

---

# 🚀 Project 2 – AI Customer Support Ticket System

## 📖 Description

This project simulates an intelligent customer support system using two AutoGen AI agents.

The system automatically:

- Classifies customer support tickets
- Determines priority level
- Generates professional customer responses

---

## 👥 Agents

### 🏷 Ticket Classifier

Responsible for:

- Reading customer issues
- Identifying ticket category
- Assigning priority

Categories:

- Billing
- Technical
- Account
- General
- Feedback

Priority Levels:

- High
- Medium
- Low

---

### 💬 Customer Support Agent

Responsible for:

- Reading classified tickets
- Understanding customer problems
- Providing professional responses
- Suggesting troubleshooting steps
- Requesting additional information when necessary

---

## Workflow

```
Customer Issue
        │
        ▼
 Ticket Classifier
        │
        ▼
 Category + Priority
        │
        ▼
 Customer Support Agent
        │
        ▼
 Professional Response
```

---

## Example

### Customer Issue

```
I was charged twice for my subscription.
```

### Ticket Classification

```
Category: Billing

Priority: High

Reason:
Duplicate payment detected.
```

### AI Response

```
Dear Customer,

Thank you for contacting us.

I'm sorry for the inconvenience.

Please share your payment receipt or transaction ID so our billing team can investigate the duplicate charge.

Once verified, we'll process your refund immediately.

Thank you for contacting Customer Support.
```

---

# 🛠 Technologies Used

- Python 3.12
- Microsoft AutoGen 0.7.5
- Google Gemini 3.5 Flash
- Google AI Studio
- asyncio
- python-dotenv
---

# ⚙ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/Day21-AutoGen.git
```

---

## Create Virtual Environment

```bash
python -m venv autogen-env
```

---

## Activate Environment

Windows

```bash
autogen-env\Scripts\activate
```

---

## Install Dependencies

```bash
pip install autogen-agentchat
pip install autogen-ext[openai]
pip install python-dotenv
```

---

## Create .env File

```
GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
```

---

## Run Multi-Agent Project

```bash
python MultiAgent/main.py
```

---

## Run Customer Support Project

```bash
python CustomerSupport/main.py
```

---

# 📚 Learning Outcomes

Through these projects, I learned:

- AutoGen Framework
- AI Agent Collaboration
- Multi-Agent Systems
- Prompt Engineering
- Google Gemini API Integration
- Customer Support Automation
- Ticket Classification
- Async Programming in Python

---

# 🚀 Future Improvements

- Streamlit Web Application
- Database Integration
- Order Tracking System
- Email Automation
- Voice Assistant
- FAQ Knowledge Base
- Live Chat Support
- CRM Integration
- Dashboard Analytics

Guru Nanak Dev Engineering College, Ludhiana

---

# ⭐ If you found this project useful, consider giving it a star.
