# n8n AI Study Material Automation 📚

## Project Overview

The **n8n AI Study Material Automation** project automates the process of generating personalized study materials and delivering them to students through email. It uses AI and workflow automation to reduce manual effort and simplify the preparation of educational content.

Students submit their requirements through Google Forms. The responses are stored in Google Sheets and processed by an n8n workflow. Google Gemini generates the study content, which is formatted as HTML, converted into a PDF using PDF.co, and sent to the student's email through Gmail.

## Objectives 🎯

- Automate the generation of study materials.
- Collect student requirements through Google Forms.
- Store and process responses using Google Sheets.
- Generate customized content using Google Gemini AI.
- Convert generated content into PDF format.
- Automatically deliver study materials through email.

## Technologies Used 🛠️

- **n8n** — Workflow automation
- **Google Forms** — Student request collection
- **Google Sheets** — Response storage
- **Google Gemini AI** — AI content generation
- **AI Agent** — Processing student requests
- **HTML** — Document formatting
- **PDF.co API** — PDF conversion
- **HTTP Request** — API communication
- **Gmail** — Automated email delivery

## Workflow Architecture ⚙️

```text
Google Forms
     ↓
Google Sheets
     ↓
Google Sheets Trigger
     ↓
AI Agent + Gemini Chat Model
     ↓
Edit Fields
     ↓
HTML Generation
     ↓
PDF.co API
     ↓
HTTP Request
     ↓
Gmail
     ↓
Student Receives PDF
```

## How It Works 🔄

1. Students submit their study-material requirements using Google Forms.
2. Form responses are saved in Google Sheets.
3. The Google Sheets Trigger starts the n8n workflow when a new response is added.
4. The AI Agent uses Google Gemini to generate content based on the student's requirements.
5. The Edit Fields node organizes the generated data.
6. The HTML node formats the content into a document.
7. PDF.co converts the HTML document into a PDF.
8. The HTTP Request node handles communication with the PDF conversion service.
9. Gmail sends the generated study material PDF to the student's email address.

## Key Features ✨

- Automated study-material generation
- Personalized content based on student requirements
- Support for different material types
- Customizable difficulty levels and word counts
- HTML-based document formatting
- PDF generation
- Automated email delivery
- Integration of AI and multiple cloud services

## Future Enhancements 🚀

- Multilingual study-material generation
- Improved PDF designs and templates
- Content validation and teacher review
- Error handling and workflow status tracking
- Support for additional AI models
- Better reporting and delivery confirmation

## Learning Outcomes 🎓

This project provides practical experience in workflow automation, AI integration, API communication, document generation, Google Workspace integration, and automated email delivery.




