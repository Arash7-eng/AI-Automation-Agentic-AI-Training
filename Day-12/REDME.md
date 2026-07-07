# 📅 Day 12 – AI WhatsApp Personal Assistant using n8n, Google Gemini & Evolution API

## 📌 Project Overview

On Day 12, I built an **AI-powered WhatsApp Personal Assistant** using **n8n**, **Google Gemini AI**, and **Evolution API**. The workflow automatically receives WhatsApp messages, processes them using Google Gemini, and sends intelligent responses back to the user through WhatsApp.

---

# 🎯 Objective

The primary objective of this project was to automate WhatsApp conversations by integrating:

- n8n Workflow Automation
- Google Gemini AI
- Evolution API
- WhatsApp

The chatbot can receive messages, generate AI-powered responses, and reply automatically without any manual intervention.

---

# 🛠 Technologies Used

- n8n
- Google Gemini AI
- Evolution API
- WhatsApp
- HTTP Request
- Webhook

---

# 🔄 Workflow Architecture

```
WhatsApp User
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

# 📖 Workflow Explanation

## Step 1 – Webhook

The workflow starts with the **Webhook** node.

### Purpose

- Receives incoming WhatsApp messages.
- Accepts requests from Evolution API.
- Starts the automation whenever a new message arrives.

---

## Step 2 – Edit Fields

The **Edit Fields** node extracts only the required information from the incoming JSON.

### Extracted Fields

| Field | Description |
|--------|-------------|
| phone | Sender's WhatsApp Number |
| message | User's WhatsApp Message |

### Expressions

#### Phone

```javascript
{{$json.body.data.key.remoteJid.replace('@s.whatsapp.net','')}}
```

#### Message

```javascript
{{$json.body.data.message.conversation}}
```

---

## Step 3 – AI Agent (Google Gemini)

The AI Agent processes the user's message using the Google Gemini model.

### Responsibilities

- Understand user queries
- Generate intelligent responses
- Return natural language replies

### User Prompt

```javascript
{{$json.message}}
```

---

## Step 4 – HTTP Request

The HTTP Request node sends the AI-generated response back to WhatsApp using Evolution API.

### Request Method

```
POST
```

### Required Headers

| Header | Value |
|---------|-------|
| apikey | Your Evolution API Key |
| Content-Type | application/json |

### Request Body

```json
{
  "number": "{{ $('Edit Fields').item.json.phone }}",
  "text": "{{ $('AI Agent').item.json.output }}"
}
```

---

# 🚀 Complete Workflow

### 1️⃣ User sends a message on WhatsApp

↓

### 2️⃣ Evolution API receives the message

↓

### 3️⃣ Evolution API forwards the message to n8n Webhook

↓

### 4️⃣ Webhook starts the workflow

↓

### 5️⃣ Edit Fields extracts

- Phone Number
- User Message

↓

### 6️⃣ AI Agent sends the message to Google Gemini

↓

### 7️⃣ Google Gemini generates an intelligent response

↓

### 8️⃣ HTTP Request sends the AI response to Evolution API

↓

### 9️⃣ Evolution API delivers the response to WhatsApp

↓

### 🔟 User receives the AI-generated reply instantly

---

# ✅ Testing

The workflow was tested successfully by sending WhatsApp messages such as:

```
Hello
```

```
How are you?
```

```
Who invented the computer?
```

The chatbot generated intelligent responses and automatically replied through WhatsApp.

---

# 📊 Final Outcome

✔ Successfully integrated WhatsApp with n8n

✔ Connected Google Gemini AI with the workflow

✔ Automated message processing

✔ Generated AI-powered responses

✔ Sent replies back to WhatsApp using Evolution API

✔ Built a fully functional AI WhatsApp Personal Assistant

---

# 📷 Project Screenshots

- Webhook Configuration
- Edit Fields Node
- AI Agent Configuration
- HTTP Request Configuration
- Workflow Execution
- WhatsApp Conversation
- Successful Response Output

---

# 🎉 Conclusion

This project demonstrates how **n8n**, **Google Gemini AI**, and **Evolution API** can be combined to build a fully automated **AI-powered WhatsApp chatbot**. The workflow efficiently receives user messages, generates intelligent responses, and delivers them back to WhatsApp in real time, providing a seamless conversational experience.
