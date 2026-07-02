# 🌤️ AI Weather Detection & Email Notification using n8n

An intelligent workflow automation project built with **n8n** that automatically monitors real-time weather conditions using the **OpenWeatherMap API** and sends personalized email notifications through **Gmail**. The workflow runs on a predefined schedule, analyzes weather conditions, and delivers either a weather alert or a daily weather report without requiring any manual intervention.

---

# 📖 Project Overview

The **AI Weather Detection & Email Notification** system is designed to automate weather monitoring and email communication.

Every day at a scheduled time, the workflow retrieves live weather information for a specified location using the OpenWeatherMap API. It processes the received weather data, evaluates the current weather condition, and automatically sends an email notification based on the result.

If rain is detected, the workflow sends a **Rain Alert** email. Otherwise, it sends a **Daily Weather Report** containing detailed weather information including temperature, humidity, wind speed, and weather description.

This project demonstrates how API integration, workflow automation, conditional logic, and email services can be combined to build practical real-world automation solutions using n8n.

---

# 🚀 Key Features

- 🌦 Automatic daily weather monitoring
- ⏰ Scheduled workflow execution
- 🌍 Real-time weather data retrieval
- 🔗 OpenWeatherMap API integration
- 📧 Automated Gmail notifications
- ☔ Rain alert detection
- 🌤 Daily weather reporting
- 🌡 Temperature monitoring
- 💧 Humidity tracking
- 🌬 Wind speed reporting
- 🔀 Conditional workflow using IF Node
- ⚡ Fully automated with no manual intervention

---

# 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation Platform |
| OpenWeatherMap API | Live Weather Data |
| Gmail | Email Notifications |
| HTTP Request Node | API Communication |
| Schedule Trigger | Automatic Execution |
| Edit Fields (Set) Node | Data Extraction |
| IF Node | Weather Condition Check |
| Gmail Node | Sending Automated Emails |

---

# 📂 Workflow Architecture

```text
                 Schedule Trigger
                        │
                        ▼
        HTTP Request (OpenWeatherMap API)
                        │
                        ▼
            Edit Fields (Extract Data)
                        │
                        ▼
          IF (Weather == "Rain"?)
                │               │
          Yes   ▼               ▼ No
      Gmail (Rain Alert)   Gmail (Daily Report)
```

---

# ⚙️ Workflow Explanation

## 1️⃣ Schedule Trigger

The workflow starts automatically every day at the configured time.

**Purpose**

- Eliminates manual execution
- Runs automatically every day
- Supports scheduled monitoring

---

## 2️⃣ HTTP Request

The HTTP Request node fetches live weather information from the OpenWeatherMap API.

The request retrieves:

- City Name
- Temperature
- Humidity
- Wind Speed
- Weather Condition
- Weather Description

Example API:

```
GET https://api.openweathermap.org/data/2.5/weather
```

---

## 3️⃣ Edit Fields (Set Node)

This node extracts only the required information from the API response.

Mapped fields:

- City
- Weather
- Description
- Temperature
- Humidity
- Wind Speed

This makes the data easier to use in later workflow steps.

---

## 4️⃣ IF Node

The IF node evaluates the weather condition.

Condition:

```
Weather == Rain
```

### True

Send Rain Alert Email

### False

Send Daily Weather Report

---

## 5️⃣ Gmail Node

Automatically sends a customized email to the recipient.

### Rain Alert

Subject

```
🌧️ Weather Alert: Rain Expected Today
```

The email advises users to carry an umbrella and provides current weather details.

---

### Daily Weather Report

Subject

```
🌤️ Today's Weather Report
```

The email contains:

- City
- Temperature
- Humidity
- Weather
- Description
- Wind Speed

---

# 📧 Sample Email

## Subject

```
🌤️ Today's Weather Report
```

## Email Content

```
City: Ludhiana

Weather: Clouds

Temperature: 31°C

Humidity: 68%

Wind Speed: 4.2 m/s

Description:
Broken Clouds

Have a wonderful day!

AI Weather Detection System
```

---

# 🎯 Learning Outcomes

Through this project, I learned:

- Workflow Automation with n8n
- REST API Integration
- HTTP Request Configuration
- JSON Data Processing
- Conditional Logic using IF Nodes
- Scheduled Workflow Execution
- Gmail Automation
- Dynamic Data Mapping
- Real-Time API Communication
- Automation Best Practices

---

# 💡 Project Highlights

✅ Fully Automated Workflow

✅ Real-Time Weather Monitoring

✅ API-Based Automation

✅ Conditional Decision Making

✅ Email Notification System

✅ Beginner-Friendly n8n Project

✅ Real-World Automation Use Case


---

# 🔮 Future Improvements

- Support multiple cities
- Weather forecast for upcoming days
- Severe weather alerts
- SMS notifications
- Telegram integration
- Slack notifications
- Microsoft Teams integration
- Weather dashboard
- AI-generated weather recommendations
- Multi-language email support

---


