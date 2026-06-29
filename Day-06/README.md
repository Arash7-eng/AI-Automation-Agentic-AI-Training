# 📚 Day 06 - AI Study Tutor using n8n AI Agent

## 📖 Overview

On Day 06, I built an **AI Study Tutor** using **n8n**, **Google Gemini AI**, and **Google Sheets**. The workflow automates answering students' academic questions by combining workflow automation with artificial intelligence.

The system receives student information through a Webhook, checks existing records in Google Sheets, processes the data using conditional logic, generates an AI-powered response using Google Gemini, stores the interaction, and returns the response instantly.

---

# 🎯 Objective

- Build an AI-powered study assistant.
- Automate question answering using Google Gemini.
- Manage student records using Google Sheets.
- Store every interaction automatically.
- Return AI-generated responses in real time.

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

# 🚀 Workflow Execution

## Step 1: Webhook Trigger

The workflow starts when a student submits the HTML form.

The Webhook receives information such as:

- Student Name
- Subject
- Question

This data becomes the input for the workflow.

---

## Step 2: Read Student Data from Google Sheets

The **Get Rows** node searches the connected Google Sheet using the student's name.

Purpose:

- Check whether the student already exists.
- Retrieve any matching records.
- Pass the result to the next node.

---

## Step 3: IF Node

The IF node checks whether a matching student record was found.

### If the student exists

The workflow follows the **True** path and sends the data to the **Code (JavaScript)** node.

### If the student does not exist

The workflow follows the **False** path and sends the data to the **Edit Fields** node.

---

## Step 4A: Code (JavaScript)

When an existing student is found, the Code node processes the retrieved data.

Tasks performed include:

- Reading student information.
- Formatting the data.
- Preparing the prompt for the AI Agent.
- Passing structured data to the next step.

---

## Step 4B: Edit Fields

If no matching student is found, the Edit Fields node creates a clean JSON object containing:

- Student Name
- Subject
- Question

This ensures that the AI Agent always receives data in the correct format.

---

## Step 5: AI Agent (Google Gemini)

The AI Agent receives the formatted data and sends the student's question to the Google Gemini Chat Model.

The AI analyzes the question and generates a detailed educational response.

Example:

**Question**

```
Explain Newton's First Law.
```

**AI Response**

```
Newton's First Law states that an object remains at rest or continues moving with constant velocity unless acted upon by an external force.
```

---

## Step 6: Append Row in Google Sheets

After generating the response, the workflow stores the interaction in Google Sheets.

The following information is saved:

- Student Name
- Subject
- Question
- AI Response

This creates a history of all interactions for future reference.

---

## Step 7: Respond to Webhook

Finally, the Respond to Webhook node sends the AI-generated answer back to the user.

The student immediately receives the response on the webpage without needing to refresh or manually check the results.

---

# ✨ Features

- AI-powered study assistant
- Automated workflow using n8n
- Google Gemini AI integration
- Google Sheets database
- Student record verification
- Conditional workflow execution
- Automatic response storage
- Real-time AI-generated answers

---

# 📚 Learning Outcomes

Through this project, I learned how to:

- Create AI-powered workflows using n8n.
- Integrate Google Gemini with AI Agent nodes.
- Use Webhooks to receive user requests.
- Read and write data using Google Sheets.
- Implement conditional logic with IF nodes.
- Process data using JavaScript.
- Structure workflow data using Edit Fields.
- Automate complete AI-based processes.
- Return responses using the Respond to Webhook node.

---

# 🚧 Challenges Faced

- Configuring the Webhook correctly.
- Connecting Google Sheets with n8n.
- Mapping fields between nodes.
- Passing data correctly through the workflow.
- Writing expressions in different nodes.
- Handling IF node conditions.
- Formatting prompts for the AI Agent.
- Managing null or missing values during testing.

---

# ✅ Outcome

Successfully built an AI-powered Study Tutor capable of answering students' academic questions automatically. The workflow efficiently receives student queries, checks existing records, processes data, generates intelligent responses using Google Gemini, stores every interaction in Google Sheets, and returns responses instantly through a Webhook.

This project strengthened my understanding of workflow automation, AI integration, conditional logic, data processing, and API communication using n8n.
