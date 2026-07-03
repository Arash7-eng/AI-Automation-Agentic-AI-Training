# Day 10 – AI Job Detection System & AI YouTube Video Summarizer

## 📌 Overview

Day 10 consists of two AI-powered automation workflows built using **n8n** and **Google Gemini AI**.

1. **AI Job Detection System** – Automatically searches for the latest job opportunities, analyzes them using AI, and sends a professional email containing the best job listings.

2. **AI YouTube Video Summarizer** – Automatically retrieves a YouTube video's transcript, generates a concise AI summary, and delivers it directly via Gmail.

These workflows demonstrate how AI and automation can save time by processing information and delivering meaningful insights automatically.

---

# 🚀 Project 1: AI Job Detection System

## 📖 Description

The AI Job Detection System automatically searches for new job opportunities based on predefined keywords, processes the results using Google Gemini AI, and sends a professional email containing the top job recommendations.

## 🛠 Workflow

Schedule Trigger
↓
HTTP Request
↓
Edit Fields
↓
Google Gemini AI Agent
↓
Gmail

---

## Step 1 – Schedule Trigger

Automatically starts the workflow every day at the configured time.

**Purpose**
- Runs automatically
- Eliminates manual execution
- Ensures daily job updates

---

## Step 2 – HTTP Request

Retrieves the latest job listings from the Job API.

**Purpose**
- Connects to Job API
- Fetches recent jobs
- Returns JSON data

---

## Step 3 – Edit Fields

Extracts only the required job information before sending it to AI.

**Fields**

- Job Title
- Company
- Location
- Employment Type
- Salary
- Description
- Apply Link
- Date

---

## Step 4 – Google Gemini AI Agent

Analyzes all retrieved jobs and generates a professional report.

**AI Tasks**

- Selects the best jobs
- Removes unnecessary information
- Creates easy-to-read summaries
- Generates professional recommendations

---

## Step 5 – Gmail

Automatically sends the summarized job report.

**Email Includes**

- Job Title
- Company
- Location
- Salary
- Summary
- Apply Link

---

## ✨ Features

- Automated Daily Job Search
- AI Job Analysis
- Professional Email Reports
- Time Saving Automation
- Easy Customization

---

## 🛠 Technologies Used

- n8n
- Google Gemini AI
- HTTP Request
- Gmail
- Job Search API
- JSON

---

# 🎥 Project 2: AI YouTube Video Summarizer

## 📖 Description

The AI YouTube Video Summarizer automatically retrieves a YouTube transcript, analyzes it using Google Gemini AI, creates a professional summary, and emails the final report.

## 🛠 Workflow

Schedule Trigger
↓
HTTP Request
↓
Edit Fields
↓
Google Gemini AI Agent
↓
Gmail

---

## Step 1 – Schedule Trigger

Starts the workflow automatically every day.

**Purpose**

- Fully automated execution
- No manual intervention
- Daily processing

---

## Step 2 – HTTP Request

Fetches the transcript and video information.

**Retrieved Data**

- Video Title
- Channel Name
- Description
- Transcript
- Thumbnail
- Duration
- Views
- Video URL

---

## Step 3 – Edit Fields

Organizes the video data before passing it to AI.

**Fields**

- Video Title
- Channel Name
- Description
- Transcript
- Video URL
- Thumbnail
- Duration
- Views
- Summary Date

---

## Step 4 – Google Gemini AI Agent

Analyzes the transcript and creates a concise summary.

**AI Tasks**

- Understands the video
- Identifies important topics
- Highlights key insights
- Generates a professional summary
- Creates a readable report

---

## Step 5 – Gmail

Sends the final AI-generated summary via email.

**Email Includes**

- Video Title
- Channel Name
- AI Summary
- Key Insights
- Video Link

---

## ✨ Features

- Automatic Transcript Retrieval
- AI Video Summarization
- Professional Email Reports
- Fully Automated Workflow
- Fast Content Understanding

---

## 🛠 Technologies Used

- n8n
- Google Gemini AI
- HTTP Request
- Gmail
- YouTube Transcript API
- JSONvv
│      

---

# 🎯 Learning Outcomes

- Built AI-powered automation workflows using n8n.
- Integrated external APIs using HTTP Request.
- Processed structured data with Edit Fields.
- Used Google Gemini AI for intelligent content generation.
- Automated email notifications with Gmail.
- Designed scalable workflows for job tracking and video summarization.

---

Built with ❤️ using **n8n**, **Google Gemini AI**, and **Automation**.
