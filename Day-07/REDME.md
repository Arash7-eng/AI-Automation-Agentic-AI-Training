# Day 07 – AI Fitness Coach & AI Customer Support Assistant using n8n

## Overview

On Day 07, I built two AI-powered automation workflows using the n8n platform: **AI Fitness Coach** and **AI Customer Support Assistant**. These projects demonstrate how AI Agents can automate personalized responses by combining HTML forms, Webhooks, Google Sheets, JavaScript, conditional logic, and Google Gemini AI. I also learned how to check existing records in Google Sheets before processing new requests, making the workflows more efficient and organized.

---

# Project 1 – AI Fitness Coach

## Objective

The goal of this project was to create an AI-powered Fitness Coach that generates personalized workout and diet recommendations based on the user's fitness information. The workflow stores user details in Google Sheets and uses AI to generate customized fitness guidance.

---

## Technologies Used

- n8n
- Google Gemini Chat Model
- AI Agent
- HTML Form
- Webhook
- Google Sheets
- JavaScript
- IF Node
- Edit Fields Node

---

## Workflow

```
HTML Form
      │
      ▼
Webhook
      │
      ▼
Get Row(s) in Google Sheets
      │
      ▼
IF Node
├──────── Existing User ───────► Code (JavaScript)
│                                 │
│                                 ▼
└──────── New User ───────────► Edit Fields
                                   │
                                   ▼
                              AI Agent
                                   │
                                   ▼
                         Append Row in Google Sheets
```

---

## Step 1 – HTML Form

Created an HTML form to collect user information.

The form collects:

- Name
- Email
- Age
- Gender
- Height
- Weight
- Fitness Goal
- Activity Level
- Workout Days
- Diet Preference
- Health Issues

The form sends data to the n8n Webhook using the POST method.

---

## Step 2 – Webhook

Configured the Webhook node to receive form submissions.

- HTTP Method: POST
- Path: `ai-fitness-coach`

The Webhook acts as the starting point of the workflow.

---

## Step 3 – Get Row(s) in Google Sheets

Connected Google Sheets to search for an existing user using the Email or Name column.

This step helps determine whether the user already exists before generating a new fitness plan.

---

## Step 4 – IF Node

Configured the IF node to check whether Google Sheets returned any matching records.

- **True:** Existing user → Code (JavaScript)
- **False:** New user → Edit Fields

This allows different processing for existing and new users.

---

## Step 5 – Code (JavaScript)

The JavaScript node processes and formats data for existing users before sending it to the AI Agent.

This step demonstrates how JavaScript can be used to manipulate workflow data inside n8n.

---

## Step 6 – Edit Fields

The Edit Fields node organizes the incoming data for new users.

Mapped fields include:

- Name
- Email
- Age
- Gender
- Height
- Weight
- Fitness Goal
- Activity Level
- Workout Days
- Diet Preference
- Health Issues

---

## Step 7 – AI Agent

Connected the Google Gemini Chat Model to the AI Agent.

The AI analyzes the user's information and generates:

- Personalized workout plan
- Diet recommendations
- Fitness analysis
- Hydration suggestions
- Sleep recommendations
- Motivation tips

---

## Step 8 – Append Row in Google Sheets

Saved the following information:

- Name
- Email
- Age
- Gender
- Height
- Weight
- Fitness Goal
- Activity Level
- Workout Days
- Diet Preference
- Health Issues
- AI Response
- Date

---

# Project 2 – AI Customer Support Assistant

## Objective

Build an AI-powered Customer Support Assistant that automatically responds to customer queries and stores customer requests in Google Sheets.

---

## Technologies Used

- n8n
- Google Gemini Chat Model
- AI Agent
- HTML Form
- Webhook
- Google Sheets
- JavaScript
- IF Node
- Edit Fields Node

---

## Workflow

```
HTML Form
      │
      ▼
Webhook
      │
      ▼
Get Row(s) in Google Sheets
      │
      ▼
IF Node
├──────── Existing Customer ─────► Code (JavaScript)
│                                   │
│                                   ▼
└──────── New Customer ─────────► Edit Fields
                                     │
                                     ▼
                                AI Agent
                                     │
                                     ▼
                           Append Row in Google Sheets
```

---

## Step 1 – HTML Form

Created a support request form to collect:

- Customer Name
- Email
- Phone Number
- Order ID
- Issue Category
- Priority
- Message

The form submits data using the POST method.

---

## Step 2 – Webhook

Configured the Webhook node to receive customer requests from the HTML form.

---

## Step 3 – Get Row(s) in Google Sheets

Configured Google Sheets to search for an existing customer using the Order ID or Email.

This prevents duplicate customer records.

---

## Step 4 – IF Node

The IF node checks whether the customer already exists.

- **True:** Existing customer → Code (JavaScript)
- **False:** New customer → Edit Fields

---

## Step 5 – Code (JavaScript)

Formats and prepares existing customer information before passing it to the AI Agent.

---

## Step 6 – Edit Fields

Maps incoming customer information into a structured format.

Fields include:

- Customer Name
- Email
- Phone Number
- Order ID
- Issue Category
- Priority
- Message

---

## Step 7 – AI Agent

The AI Agent analyzes the customer's issue and generates a professional response.

The response includes:

- Greeting
- Issue summary
- Suggested solution
- Estimated resolution time
- Escalation guidance when necessary

---

## Step 8 – Append Row in Google Sheets

Stores customer information together with the AI-generated response.

Saved data includes:

- Customer Name
- Email
- Phone Number
- Order ID
- Issue Category
- Priority
- Message
- AI Response
- Date

---

# What I Learned

During Day 07, I gained practical experience with:

- Creating AI-powered workflows using n8n.
- Building HTML forms for user input.
- Configuring Webhook nodes.
- Reading existing records using **Get Row(s)**.
- Applying conditional workflow logic using the **IF** node.
- Processing data with the **Code (JavaScript)** node.
- Organizing data using the **Edit Fields** node.
- Integrating the **Google Gemini Chat Model** with an AI Agent.
- Saving workflow data to Google Sheets.
- Building intelligent automation workflows for real-world applications.

---

# Conclusion

Day 07 focused on developing intelligent AI automation workflows that combine user input, conditional logic, AI processing, and cloud-based data storage. The AI Fitness Coach generates personalized fitness recommendations, while the AI Customer Support Assistant provides automated responses to customer queries. These projects strengthened my understanding of workflow automation, AI integration, Google Sheets connectivity, and real-world problem solving using n8n.
