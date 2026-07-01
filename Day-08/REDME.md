# Day 08 - AI Expense Tracker using n8n AI Agent

## Overview

On Day 08, I built an AI-powered Expense Tracker using the n8n automation platform and Google Gemini AI. The workflow automatically classifies expenses based on their descriptions and stores them in categorized Google Sheets.

Instead of manually selecting an expense category, users simply provide the expense description, amount, and date. The AI analyzes the description, determines the appropriate category, and the workflow automatically saves the data into the corresponding Google Sheet.

This project demonstrates how AI can simplify personal finance management through intelligent automation.

---

## Project Objective

The objective of this project is to automate expense tracking by using Artificial Intelligence to categorize expenses accurately and store them in Google Sheets without manual effort.

---

## Technologies Used

- n8n
- Google Gemini AI
- Google Sheets
- Webhook
- JavaScript
- Switch Node
- HTML Form

---

## Workflow

Webhook
↓
AI Agent (Google Gemini)
↓
JavaScript Code
↓
Switch Node
↓
Google Sheets

Food
Travel
Shopping
Bills
Entertainment
Other

---

## Workflow Explanation

### Step 1 – Webhook

A webhook receives expense details submitted from an HTML form.

Input fields include:

- Date
- Expense Description
- Amount

---

### Step 2 – AI Agent

The AI Agent analyzes the expense description and classifies it into one of the following categories:

- Food
- Travel
- Shopping
- Bills
- Entertainment
- Other

The AI returns structured JSON data.

Example:

{
"date":"2026-07-01",
"description":"Lunch at Domino's",
"amount":"450",
"category":"Food"
}

---

### Step 3 – JavaScript Code

The Code node parses the JSON response received from the AI Agent and prepares the data for further processing.

---

### Step 4 – Switch Node

The Switch node checks the category returned by the AI and routes the expense to the correct Google Sheets node.

Possible outputs:

- Food
- Travel
- Shopping
- Bills
- Entertainment
- Other

---

### Step 5 – Google Sheets

Each category has its own Google Sheet where expenses are automatically appended.

Columns:

- Date
- Description
- Amount
- Category

---

### Step 6 – Respond to Webhook

After successfully saving the expense, the workflow returns a confirmation response to the user.

---

## Features

- AI-powered expense classification
- Automatic expense categorization
- Google Sheets integration
- Webhook-based data collection
- Intelligent routing using Switch Node
- Real-time automation
- No manual categorization required

---

## Sample Input

Date:
2026-07-01

Description:
Bought Pizza and Cold Drink

Amount:
450

---

## AI Output

Category:
Food

---

## Google Sheets Output

| Date | Description | Amount | Category |
|------|-------------|--------|----------|
|2026-07-01|Bought Pizza and Cold Drink|450|Food|

---

## Learning Outcomes

Through this project, I learned:

- AI Agent implementation
- Prompt Engineering
- JSON Parsing
- Workflow Automation
- Google Sheets Integration
- Conditional Routing
- Webhook Integration
- JavaScript in n8n

---

## Future Improvements

- Monthly Expense Dashboard
- Email Notifications
- Telegram Notifications
- OCR Receipt Scanner
- Budget Tracking
- Expense Analytics
- Category Charts

---


## Conclusion

This project demonstrates how Artificial Intelligence and workflow automation can simplify expense management by automatically categorizing expenses and storing them efficiently. It is a practical example of integrating AI with n8n to build intelligent automation solutions.

# Guess Number 
# Guess Number

## Overview

Guess Number is a simple and interactive web application developed using HTML, CSS, and JavaScript. In this project, users manually enter a number, and the application analyzes the input based on predefined conditions to classify it as **Easy**, **Medium**, or **Strong**.

The project demonstrates fundamental JavaScript concepts such as user input handling, conditional statements, event handling, and DOM manipulation while providing a clean and responsive user interface.

---

## Project Objective

The objective of this project is to create an interactive web application that evaluates user-entered numbers and provides instant feedback by categorizing them into Easy, Medium, or Strong levels.

---

## Technologies Used

- HTML5
- CSS3
- JavaScript

---

## Features

- Manual number input
- Instant result generation
- Easy, Medium, and Strong classification
- Responsive and user-friendly interface
- Input validation
- Dynamic result display

---

## How the Application Works

### Step 1

The user enters a number in the input field.

### Step 2

The user clicks the **Check** button.

### Step 3

JavaScript processes the entered number according to predefined conditions.

### Step 4

The application displays one of the following results:

- Easy
- Medium
- Strong

### Step 5

The user can enter another number and repeat the process.

---

## Example Output

| User Input | Result |
|------------|--------|
| 5 | Easy |
| 15 | Medium |
| 30 | Strong |
| 42 | Strong |
| 8 | Easy |

---

## Learning Outcomes

Through this project, I learned:

- HTML Form Design
- CSS Styling
- JavaScript Variables
- Functions
- DOM Manipulation
- Event Handling
- Conditional Statements
- User Input Validation
- Interactive Web Development

---

## Future Improvements

- Custom classification rules
- Progress indicator
- Animated result display
- Dark mode
- Reset button
- Mobile-friendly enhancements
---

## Conclusion

Guess Number is a beginner-friendly JavaScript project that demonstrates how to accept user input, process data using conditional logic, and display dynamic results. The project helped strengthen my understanding of JavaScript fundamentals and interactive web application development while focusing on creating a simple and intuitive user experience.
