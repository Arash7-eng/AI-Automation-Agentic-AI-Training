# 🤖 Day 17 – AI Content Repurposer & AI Image Generation using n8n

## 📌 Overview

Day 17 focused on developing two AI-powered automation workflows using **n8n**. The first workflow automates the generation of marketing content for multiple social media platforms from a single topic, while the second workflow generates AI images from text prompts, uploads them to Google Drive, and updates the generated content back into Google Sheets.

These workflows demonstrate how Artificial Intelligence and automation can simplify digital marketing by reducing repetitive tasks and producing high-quality content with minimal human effort.

---

# 🚀 Workflow 1 – AI Content Repurposer

## 📖 Project Description

The **AI Content Repurposer** is an intelligent workflow that transforms a single content idea into multiple platform-specific marketing assets.

A user only needs to provide the topic, target audience, writing tone, language, and preferred platform in Google Sheets. Once a new row is added, the workflow automatically triggers, sends the data to an AI Agent powered by Google Gemini, and generates content for various social media platforms in a structured JSON format.

The generated content is then stored back into the same Google Sheet, making it easy for marketing teams to review and publish.

---

## 🎯 Objectives

- Automate social media content creation
- Generate multiple content formats from one topic
- Produce SEO-friendly marketing content
- Eliminate repetitive manual writing
- Store generated content automatically

---

## 🛠 Technologies Used

- n8n
- Google Sheets
- Google Gemini Chat Model
- AI Agent
- Structured Output Parser
- Google Sheets Trigger
- Google Sheets Update Row
- JSON Schema

---

## ⚙ Workflow Architecture

```text
Google Sheets Trigger
        │
        ▼
Check Status (IF)
        │
        ▼
AI Agent (Google Gemini)
        │
        ▼
Structured Output Parser
        │
        ▼
Update Google Sheet
```

---

## 📥 Input

The workflow accepts the following information from Google Sheets.

- Topic
- Audience
- Tone
- Language
- Platform Focus

---

## 📤 Generated Content

The AI automatically creates:

### Social Media

- Instagram Caption
- Instagram Hashtags
- Instagram CTA
- LinkedIn Post
- LinkedIn CTA
- Twitter/X Thread
- Facebook Post

### Marketing Content

- Short Caption
- Medium Caption
- Long Caption

### SEO Content

- SEO Title
- Meta Description
- Focus Keyword

### Image Prompts

- Realistic Image Prompt
- Cartoon Image Prompt

---

## ⭐ Key Features

- AI-powered content generation
- Multi-platform content repurposing
- Structured JSON output
- Automatic Google Sheets update
- SEO optimization
- No-code automation

---

## 📸 Screenshots to Include

- Google Sheet
- Google Sheets Trigger
- AI Agent
- Structured Output Parser
- Workflow Execution
- Updated Google Sheet

---

# 🖼 Workflow 2 – AI Image Generation & Google Drive Automation

## 📖 Project Description

The second workflow focuses on automatically generating AI images based on the image prompt created in the first workflow.

The workflow retrieves the generated image prompt, sends it to the Pollinations AI Image API using an HTTP Request node, downloads the generated image, uploads it to Google Drive, and finally updates the corresponding Google Sheets row with the generated image link and workflow status.

This workflow completely automates AI-based visual content creation without requiring manual image design.

---

## 🎯 Objectives

- Generate AI images automatically
- Upload generated images to Google Drive
- Save image links back into Google Sheets
- Automate visual content creation

---

## 🛠 Technologies Used

- n8n
- Pollinations AI
- HTTP Request Node
- Google Drive
- Google Sheets Update Row

---

## ⚙ Workflow Architecture

```text
Image Prompt
      │
      ▼
HTTP Request
(Pollinations AI)
      │
      ▼
Upload File
(Google Drive)
      │
      ▼
Update Row in Google Sheets
```

---

## 🌄 Workflow Process

### Step 1

Receive the AI-generated realistic image prompt.

### Step 2

Generate an AI image using the Pollinations AI API.

### Step 3

Download the generated image using the HTTP Request node.

### Step 4

Upload the generated image automatically to Google Drive.

### Step 5

Obtain the Google Drive file link.

### Step 6

Update the corresponding Google Sheets row with:

- Google Drive Image Link
- Generated Status

---

## ⭐ Key Features

- AI image generation
- Automatic image download
- Google Drive integration
- Cloud storage
- Automatic Google Sheets update
- End-to-end automation

---

## 📸 Screenshots to Include

- HTTP Request Node
- Generated AI Image
- Google Drive Upload
- Google Drive Folder
- Updated Google Sheet
- Successful Workflow Execution

---

# 📚 Skills Learned

During Day 17, I gained practical experience in:

- AI Automation using n8n
- Prompt Engineering
- Google Gemini AI
- Structured Output Parsing
- JSON Schema Design
- AI Image Generation
- REST API Integration
- HTTP Request Configuration
- Google Drive Automation
- Google Sheets Automation
- Workflow Orchestration
- Digital Marketing Automation

---

# 🎯 Learning Outcome

This project demonstrated how Artificial Intelligence can automate both written and visual content creation. By integrating Google Gemini, Pollinations AI, Google Sheets, and Google Drive within n8n, I successfully built a complete AI-powered content automation system capable of generating high-quality marketing assets with minimal manual effort.

The workflows highlight the practical application of AI in digital marketing, workflow automation, and cloud integration, providing a scalable solution for content creators and marketing teams.

---

# 📌 Conclusion

Day 17 helped me understand how multiple AI services can work together in a single automation ecosystem. The AI Content Repurposer simplifies content creation for different social media platforms, while the AI Image Generation workflow automatically creates visual assets and stores them in the cloud.

Together, these workflows showcase the power of no-code AI automation using n8n, improving productivity, consistency, and efficiency in modern content marketing.
