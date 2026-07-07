# Day 12 – Building the AI WhatsApp Personal Assistant Workflow

## Objective
The objective of this task was to create an automated workflow in n8n that receives WhatsApp messages, processes them using Google Gemini AI, and sends AI-generated replies back to the user through Evolution API.

## Workflow Overview

Webhook → Edit Fields → AI Agent (Google Gemini) → HTTP Request → WhatsApp Reply

## Steps Performed

### 1. Created a Webhook
- Added a **Webhook** node in n8n.
- Configured it to receive incoming WhatsApp messages from Evolution API.
- Tested the webhook using the test URL.

### 2. Extracted Required Data
- Added an **Edit Fields** node.
- Extracted the sender's phone number.
- Extracted the user's WhatsApp message.

Expressions used:

**Phone**
```javascript
{{$json.body.data.key.remoteJid.replace('@s.whatsapp.net','')}}
```

**Message**
```javascript
{{$json.body.data.message.conversation}}
```

### 3. Configured the AI Agent
- Added an **AI Agent** node.
- Connected the **Google Gemini Chat Model**.
- Used the incoming WhatsApp message as the prompt.
- Generated an intelligent response for the user.

Prompt:

```javascript
{{$json.message}}
```

### 4. Configured HTTP Request
- Added an **HTTP Request** node.
- Used the Evolution API **sendText** endpoint.
- Added the required API Key.
- Configured the request body to send the AI-generated response back to WhatsApp.

Request Body

```json
{
  "number": "{{$node['Edit Fields'].json.phone}}",
  "text": "{{$node['AI Agent'].json.output}}"
}
```

### 5. Tested the Workflow
- Sent a message from WhatsApp.
- The webhook received the request.
- Google Gemini generated an AI response.
- Evolution API delivered the response back to WhatsApp successfully.

## Workflow

Webhook → Edit Fields → AI Agent → HTTP Request

## Technologies Used

- n8n
- Google Gemini AI
- Evolution API
- WhatsApp
- HTTP Request
- Webhook

## Outcome

- Successfully received WhatsApp messages.
- Extracted user information automatically.
- Generated AI-powered responses using Google Gemini.
- Sent responses back to WhatsApp automatically through Evolution API.
- Built a complete AI-powered WhatsApp Personal Assistant workflow.
