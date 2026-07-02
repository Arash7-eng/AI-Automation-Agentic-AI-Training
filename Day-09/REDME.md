# 🌤️ AI Weather Detection & Email Notification using n8n

## 📌 Overview

This project is an automated weather notification system built with n8n.

The workflow runs automatically every day using the Schedule Trigger, fetches real-time weather data from the OpenWeatherMap API, checks the weather condition, and sends an email notification through Gmail.

---

## 🚀 Features

- Automatic daily weather check
- Real-time weather data using OpenWeatherMap API
- Scheduled execution
- Weather condition detection
- Rain alert notifications
- Daily weather reports
- Gmail integration
- No manual intervention required

---

## 🛠 Technologies Used

- n8n
- OpenWeatherMap API
- Gmail
- HTTP Request
- Schedule Trigger
- IF Node
- Edit Fields Node

---

## 📊 Workflow

Schedule Trigger
⬇
HTTP Request (Weather API)
⬇
Edit Fields
⬇
IF (Rain?)
├── Yes → Gmail (Rain Alert)
└── No → Gmail (Daily Weather Report)

---

## ⚙️ Workflow Steps

### 1. Schedule Trigger
Runs automatically every day at the configured time.

### 2. HTTP Request
Fetches live weather information from OpenWeatherMap.

### 3. Edit Fields
Extracts:
- City
- Weather
- Temperature
- Humidity
- Wind Speed
- Description

### 4. IF Node
Checks whether the weather condition is Rain.

### 5. Gmail
Sends either:
- Rain Alert
- Daily Weather Report

---

## 📧 Example Email

Subject:
🌤️ Daily Weather Report

Body:
- City
- Weather
- Temperature
- Humidity
- Wind Speed
- Description

---

## 🎯 Learning Outcomes

- API Integration
- HTTP Request Node
- Schedule Automation
- Conditional Logic
- Gmail Automation
- JSON Data Handling
- Workflow Design
- No-Code Automation

---

## 👨‍💻 Author

Arashpreet Kaur
Computer Science Engineering Student
Guru Nanak Dev Engineering College, Ludhiana
