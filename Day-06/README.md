# 📚 Day 06 - AI Study Tutor using n8n AI Agent

## 📖 Overview

On Day 06, I developed an **AI Study Tutor** using **n8n**, **Google Gemini AI**, and **Google Sheets**. This project automates the process of answering students' academic questions through an AI-powered workflow.

The workflow receives student details through a Webhook, checks whether the student already exists in Google Sheets, processes the data using conditional logic, generates an intelligent response with Google Gemini, stores the interaction, and sends the answer back instantly.

This project demonstrates how workflow automation and AI can be combined to create an efficient educational assistant.

---

# 🎯 Project Objectives

- Build an AI-powered study assistant.
- Accept student questions through a Webhook.
- Retrieve student records from Google Sheets.
- Generate accurate answers using Google Gemini AI.
- Store every interaction automatically.
- Return AI-generated responses instantly.

---

# 🛠️ Technologies Used

- n8n
- Google Gemini Chat Model
- Google Sheets
- Webhook
- AI Agent
- IF Node
- Code (JavaScript)
- Edit Fields
- Respond to Webhook

---

# ⚙️ Workflow

```
Webhook
      │
      ▼
Get Rows in Google Sheets
      │
      ▼
IF Node
 ┌───────────────┐
 │               │
 ▼               ▼
Code Node    Edit Fields
      │         │
      └─────────┘
          │
          ▼
      AI Agent
          │
          ▼
Append Row in Google Sheets
          │
          ▼
Respond to Webhook
```

---

# 📌 Workflow Explanation

### 1. Webhook
The workflow starts with a Webhook that receives the student's name, subject, and question submitted from an HTML form.

### 2. Get Rows in Google Sheets
The workflow reads data from Google Sheets to determine whether the student already exists.

### 3. IF Node
The IF node checks whether a matching student record is found.

- **True:** The workflow continues through the JavaScript Code node.
- **False:** The workflow continues through the Edit Fields node.

### 4. Code (JavaScript)
The Code node formats or processes the existing student data before sending it to the AI Agent.

### 5. Edit Fields
For new students, the Edit Fields node structures the incoming data into the required format for the AI Agent.

### 6. AI Agent (Google Gemini)
The AI Agent receives the student's question and generates a clear, informative, and accurate response using the Google Gemini Chat Model.

### 7. Append Row in Google Sheets
The student's question and the AI-generated response are automatically saved in Google Sheets for future reference.

### 8. Respond to Webhook
Finally, the generated answer is returned to the user through the Webhook response.

---

# ✨ Features

- AI-powered educational assistant
- Google Gemini AI integration
- Google Sheets database
- Student record lookup
- Conditional workflow logic
- Automatic data storage
- Instant AI responses
- Fully automated workflow

---

# 📚 Learning Outcomes

Through this project, I learned how to:

- Build AI-powered workflows using n8n.
- Integrate Google Gemini with AI Agent nodes.
- Use Webhooks to receive user input.
- Read and write data using Google Sheets.
- Apply conditional logic with IF nodes.
- Process data using JavaScript.
- Format data with Edit Fields.
- Automate complete AI workflows.

---

# 🚧 Challenges Faced

- Configuring the Webhook correctly.
- Mapping Google Sheets data.
- Passing data between workflow nodes.
- Writing expressions for different nodes.
- Debugging IF conditions.
- Formatting prompts for AI responses.
- Handling missing or null values.

---

# ✅ Project Outcome

Successfully developed an AI-powered Study Tutor that can automatically answer students' academic questions using Google Gemini. The workflow retrieves student information, processes requests, generates intelligent responses, stores the interactions in Google Sheets, and returns answers instantly through a Webhook.

This project enhanced my understanding of AI automation, workflow design, Google Sheets integration, JavaScript processing, and API-based communication using n8n.

---

# 📂 Project Structure

```
Day-06-AI-Study-Tutor/
│
├── README.md
├── workflow.json
├── ai-study-tutor.html
└── assets/
```

---

# 👩‍💻 Author

**Arashpreet Kaur**

Computer Science & Engineering Student

Currently learning **n8n, AI Automation, Google Gemini, Workflow Automation, and Web Development.**
