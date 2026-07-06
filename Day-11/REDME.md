# 🤖 Day 11 – AI WhatsApp Personal Assistant using n8n & Evolution API

An AI-powered WhatsApp chatbot built with **n8n**, **Evolution API**, and **Google Gemini**. This workflow automatically receives WhatsApp messages, processes them with an AI model, and sends intelligent replies back to the user in real time.

---

## 📖 Overview

This project demonstrates how to integrate WhatsApp with n8n using Evolution API and build an intelligent chatbot powered by Google Gemini.

The workflow listens for incoming WhatsApp messages through a webhook, extracts the required data, sends the user's message to Gemini AI, and automatically replies back to the sender using Evolution API.

This project is ideal for learning:

- Webhook Automation
- AI Integration
- REST APIs
- WhatsApp Automation
- n8n Workflow Design

---

# 🚀 Features

- 📱 Receive WhatsApp messages automatically
- 🤖 AI-generated responses using Google Gemini
- ⚡ Real-time webhook automation
- 🔗 Evolution API integration
- 📩 Automatic WhatsApp replies
- ☁️ Cloud deployment
- 🔄 End-to-end workflow automation
- 🧠 Smart conversational assistant

---

# 🛠️ Technologies Used

- n8n
- Evolution API
- Google Gemini API
- Webhooks
- HTTP Request
- JSON
- REST API
- Cloud Station

---

# 📂 Workflow

```
WhatsApp User
      │
      ▼
Evolution API
      │
      ▼
Webhook
      │
      ▼
Edit Fields
      │
      ▼
AI Agent (Google Gemini)
      │
      ▼
HTTP Request
      │
      ▼
Evolution API
      │
      ▼
WhatsApp User
```

---

# ⚙️ Workflow Steps

## Step 1 – Deploy Evolution API

- Deploy Evolution API on Cloud Station.
- Connect your WhatsApp account using the QR Code.
- Wait until the service becomes active.

---

## Step 2 – Configure Webhook

Copy the **Production URL** from the n8n Webhook node and paste it into the Evolution API Webhook settings.

Enable the **Message Upsert** event.

Whenever a new WhatsApp message arrives, Evolution API forwards it to n8n.

---

## Step 3 – Webhook Node

The Webhook node receives incoming WhatsApp messages.

Example Input

```json
{
  "body": {
    "data": {
      "key": {
        "remoteJid": "919876543210@s.whatsapp.net"
      },
      "message": {
        "conversation": "Hello"
      }
    }
  }
}
```

---

## Step 4 – Edit Fields Node

Extract only the required information.

**Phone**

```
={{$json.body.data.key.remoteJid}}
```

**Message**

```
={{$json.body.data.message.conversation}}
```

Output

```json
{
  "phone": "919876543210@s.whatsapp.net",
  "message": "Hello"
}
```

---

## Step 5 – AI Agent

Connect Google Gemini to the AI Agent.

### System Prompt

- Helpful assistant
- Friendly replies
- Short responses
- Safe conversations
- Answer clearly

User Message

```
={{$json.message}}
```

The AI processes the user's message and generates an intelligent response.

---

## Step 6 – HTTP Request

The HTTP Request node sends the AI-generated response back to WhatsApp.

Method

```
POST
```

Example Body

```json
{
  "number": "{{$json.phone}}",
  "text": "{{$json.output}}"
}
```

---

# 🔄 Complete Workflow Execution

1. User sends a WhatsApp message.
2. Evolution API receives the message.
3. Evolution API forwards it to the n8n Webhook.
4. Webhook triggers the workflow.
5. Edit Fields extracts the phone number and message.
6. Google Gemini generates an AI response.
7. HTTP Request sends the response through Evolution API.
8. The user receives the reply on WhatsApp automatically.

---

# 📁 Project Structure

```
---

# 🎯 Learning Outcomes

After completing this project, you will understand:

- Building AI-powered automation workflows
- Webhook configuration
- WhatsApp automation
- REST API integration
- Google Gemini integration
- JSON data processing
- HTTP Request node configuration
- End-to-end workflow automation using n8n

---

# 🔮 Future Improvements

- Conversation memory
- Voice message support
- Image analysis
- PDF question answering
- Google Sheets logging
- CRM integration
- Calendar scheduling
- Multi-language chatbot
- Appointment booking

---

# 💼 Use Cases

- Personal AI Assistant
- Customer Support Bot
- FAQ Automation
- Business Inquiry Assistant
- AI Helpdesk
- WhatsApp Information Bot

---

# 🏷️ Repository Topics

```
n8n
automation
whatsapp
evolution-api
google-gemini
ai-chatbot
webhook
rest-api
workflow
artificial-intelligence
low-code
no-code
```

---
