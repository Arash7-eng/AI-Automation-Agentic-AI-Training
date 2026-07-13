# 🤖 Day 16 - AI Content Generator & Company Blog Generator using n8n

## 📌 Project Overview

On **Day 16** of my **AI Automation & Agentic AI Training**, I built two AI-powered workflows using **n8n** and the **Google Gemini Chat Model**.

The first workflow is an **AI Content Generator**, which automatically generates high-quality content from a user-provided topic.

The second workflow is an **AI Company Blog Generator**, which creates professional and SEO-friendly blog posts based on company information stored in Google Sheets.

These workflows demonstrate how AI and workflow automation can simplify content creation, reduce manual effort, and improve productivity.

---

# 🚀 Projects Included

## 1️⃣ AI Content Generator

### Description

The AI Content Generator automates content creation by generating well-structured content using Google Gemini AI. Whenever a new topic is added to Google Sheets, the workflow automatically generates content and updates the sheet with the AI-generated response.

### Features

- Automatic workflow execution
- AI-generated content
- Google Sheets integration
- Google Gemini AI
- Structured AI responses
- No manual writing required

---

## Workflow

```
Google Sheets Trigger
        │
        ▼
     AI Agent
        │
Google Gemini Chat Model
        │
Structured Output Parser
        │
Update Google Sheet
```

### Workflow Explanation

### Step 1 – Google Sheets Trigger

The workflow starts automatically whenever a new row is added to Google Sheets.

It reads the input information such as:

- Topic
- Content Type
- Target Audience

---

### Step 2 – AI Agent

The AI Agent receives the input data from Google Sheets and prepares a prompt for Google Gemini AI.

---

### Step 3 – Google Gemini Chat Model

Google Gemini generates high-quality content based on the provided topic.

---

### Step 4 – Structured Output Parser

The Structured Output Parser formats the AI response into a clean and structured format.

---

### Step 5 – Update Google Sheet

The generated content is automatically written back to the corresponding row in Google Sheets.

---

## Example Input

| Topic | Content Type | Audience |
|--------|--------------|----------|
| Artificial Intelligence | Blog | Students |

---

## Example Output

- Title
- Introduction
- Main Content
- Conclusion

---

# 2️⃣ AI Company Blog Generator

## Description

The AI Company Blog Generator automatically creates complete company blogs using AI.

The workflow reads company details from Google Sheets and generates an SEO-friendly blog including a title, introduction, headings, detailed content, and conclusion.

---

## Workflow

```
Google Sheets Trigger
        │
        ▼
     AI Agent
        │
Google Gemini Chat Model
        │
Structured Output Parser
        │
Update Google Sheet
```

---

## Workflow Explanation

### Step 1 – Google Sheets Trigger

The workflow begins when a new row is added to Google Sheets.

The workflow reads:

- Company Name
- Industry
- Blog Topic

---

### Step 2 – AI Agent

The AI Agent processes the company details and creates a prompt for Google Gemini AI.

---

### Step 3 – Google Gemini Chat Model

Google Gemini generates a professional company blog containing:

- Blog Title
- Introduction
- Main Content
- Headings
- Conclusion

---

### Step 4 – Structured Output Parser

The Structured Output Parser formats the generated blog into an organized structure.

---

### Step 5 – Update Google Sheet

The generated blog is automatically saved back into the Google Sheet.

---

## Example Input

| Company Name | Industry | Blog Topic |
|--------------|----------|------------|
| ABC Technologies | Information Technology | Benefits of Artificial Intelligence |

---

## Example Output

- Blog Title
- Introduction
- SEO-friendly Headings
- Detailed Blog Content
- Conclusion

---

# 🛠 Technologies Used

- n8n
- Google Sheets
- Google Gemini Chat Model
- AI Agent
- Structured Output Parser
- Prompt Engineering
- Workflow Automation

---

# 🎯 Learning Outcomes

During Day 16, I learned how to:

- Build AI-powered workflows using n8n.
- Integrate Google Gemini Chat Model with AI Agent.
- Connect Google Sheets with AI workflows.
- Generate high-quality AI content automatically.
- Create professional company blogs using AI.
- Format AI responses using Structured Output Parser.
- Automate repetitive content generation tasks.
- Improve prompt engineering for better AI-generated results.
- Design reusable workflow automation solutions.

---

# 💡 Applications

These workflows can be used for:

- Content Writing
- Blog Generation
- SEO Content Creation
- Company Websites
- Digital Marketing
- Business Automation
- AI Content Management
- Marketing Agencies
- Educational Content
- Startup Blogs

---

# ✅ Conclusion

On **Day 16**, I successfully developed two AI-powered automation workflows using **n8n**.

The **AI Content Generator** streamlines the process of creating structured written content from simple user inputs, while the **AI Company Blog Generator** automates the creation of professional, SEO-friendly blog posts for businesses.

These projects enhanced my understanding of workflow automation, AI integration, Google Sheets automation, and prompt engineering. They also demonstrated how AI can significantly improve productivity by automating content creation for real-world business applications.

---
