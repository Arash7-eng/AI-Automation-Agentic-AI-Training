Day 07 – AI Fitness Coach & AI Customer Support Assistant using n8n
Overview

On Day 07, I developed two AI-powered workflow automation projects using the n8n platform: AI Fitness Coach and AI Customer Support Assistant. These projects demonstrate how AI Agents can automate personalized responses by processing user input received through HTML forms. The workflows integrate Webhooks, Google Sheets, JavaScript, IF conditions, AI Agents, and Google Gemini Chat Model to provide intelligent, automated solutions.

Both workflows were designed to check whether a user or customer already exists in Google Sheets before generating a response. Depending on the result, the workflow either processes existing data or creates a new record.

Project 1 – AI Fitness Coach
Objective

Build an AI-powered Fitness Coach that generates personalized fitness recommendations based on user information and stores the results automatically in Google Sheets.

Technologies Used
n8n
Google Gemini Chat Model
AI Agent
Google Sheets
Webhook
JavaScript
IF Node
HTML Form
Workflow Architecture
HTML Form
      │
      ▼
Webhook
      │
      ▼
Get Row(s) in Google Sheet
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
                          Append Row in Google Sheet
Step 1 – HTML Form

Created an HTML form to collect fitness information from users.

Collected information:

Name
Age
Gender
Height
Weight
Fitness Goal
Activity Level
Workout Days
Diet Preference
Health Issues
Email

The form submits data using the POST method to the n8n Webhook.

Step 2 – Webhook

Configured the Webhook node to receive data submitted from the HTML form.

Configuration
HTTP Method: POST
Path: ai-fitness-coach

The Webhook acts as the entry point of the workflow.

Step 3 – Google Sheets (Get Row(s))

Connected Google Sheets to search for an existing user before generating a new fitness plan.

The node searches the sheet using the user's email or name to determine whether the user already exists.

This helps avoid duplicate records and supports returning users.

Step 4 – IF Node

Added an IF node after Google Sheets.

The IF node checks whether the Get Row(s) node returned any matching records.

Existing User

The workflow moves to the JavaScript node.

New User

The workflow moves to the Edit Fields node.

Step 5 – Code (JavaScript)

For existing users, the JavaScript node prepares and formats the retrieved data before sending it to the AI Agent.

The Code node allows custom processing and data transformation within the workflow.

Step 6 – Edit Fields

For new users, the Edit Fields node organizes and maps all incoming form fields into a clean structure.

Mapped fields include:

Name
Email
Age
Gender
Height
Weight
Fitness Goal
Activity Level
Workout Days
Diet Preference
Health Issues

This makes the data easier to use in the AI Agent and Google Sheets.

Step 7 – AI Agent

Connected the Google Gemini Chat Model to the AI Agent.

The AI Agent analyzes the user's information and generates a personalized response that includes:

Fitness analysis
Workout recommendations
Diet suggestions
Hydration advice
Sleep recommendations
Motivation tips

The AI response is generated automatically based on the user's fitness goals and health information.

Step 8 – Append Row in Google Sheets

Stored both the user's information and the AI-generated fitness plan in Google Sheets.

Saved data includes:

Name
Email
Age
Gender
Height
Weight
Goal
Activity Level
Workout Days
Diet Preference
Health Issues
AI Response
Date
Project 2 – AI Customer Support Assistant
Objective

Develop an AI-powered customer support system capable of understanding customer issues and generating professional responses automatically.

Technologies Used
n8n
Google Gemini Chat Model
AI Agent
Google Sheets
HTML Form
Webhook
JavaScript
IF Node
Workflow Architecture
HTML Form
      │
      ▼
Webhook
      │
      ▼
Get Row(s) in Google Sheet
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
                           Append Row in Google Sheet
Step 1 – HTML Form

Created a support request form to collect customer details.

Collected information:

Customer Name
Email
Phone Number
Order ID
Issue Category
Priority
Message
Step 2 – Webhook

Configured the Webhook node to receive support requests submitted from the HTML form.

Step 3 – Google Sheets (Get Row(s))

Used Google Sheets to search for an existing customer or order based on the Order ID or Email.

Step 4 – IF Node

The IF node checks whether a matching customer record exists.

Existing customer → JavaScript
New customer → Edit Fields
Step 5 – Code (JavaScript)

Formats and prepares customer data retrieved from Google Sheets before sending it to the AI Agent.

Step 6 – Edit Fields

Maps incoming customer information into a clean structure for AI processing.

Fields include:

Customer Name
Email
Phone Number
Order ID
Issue Category
Priority
Message
Step 7 – AI Agent

The AI Agent analyzes the customer's issue and generates a professional support response.

The response typically includes:

Greeting
Issue summary
Suggested solution
Estimated resolution time
Escalation guidance if required
Step 8 – Append Row in Google Sheets

Stored customer information together with the AI-generated response in Google Sheets for future reference.

Key Learning Outcomes

During Day 07, I learned how to:

Build complete AI-powered automation workflows in n8n.
Create HTML forms that communicate with Webhook nodes.
Connect Google Sheets for reading and writing data.
Use Get Row(s) to check whether a record already exists.
Apply IF conditions to create different workflow paths.
Process data using the Code (JavaScript) node.
Organize incoming data with the Edit Fields node.
Integrate the Google Gemini Chat Model with an AI Agent.
Store AI-generated responses in Google Sheets.
Design reusable workflows for different real-world use cases.
Conclusion

Day 07 focused on creating intelligent automation workflows that combine AI with data management. The AI Fitness Coach delivers personalized health and fitness guidance, while the AI Customer Support Assistant automates customer query handling with professional responses. These projects strengthened my understanding of workflow logic, conditional processing, AI integration, JavaScript data handling, and Google Sheets automation using n8n.
