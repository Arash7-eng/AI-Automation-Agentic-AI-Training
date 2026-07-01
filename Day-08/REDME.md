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

# Guess Number Game
# Number Strength Checker

## Overview

The Number Strength Checker is a simple interactive web application developed using HTML, CSS, and JavaScript. Users manually enter a number into the input field, and the application analyzes it based on predefined conditions to classify it as **Easy**, **Medium**, or **Strong**.

This project demonstrates user input handling, conditional statements, JavaScript functions, and DOM manipulation in a simple and interactive way.

---

## Project Objective

To build a browser-based application that accepts a user-entered number and categorizes it into Easy, Medium, or Strong based on predefined rules.

---

## Technologies Used

- HTML5
- CSS3
- JavaScript

---

## Features

- Manual number input
- Instant result display
- Easy, Medium, and Strong classification
- Simple and user-friendly interface
- Input validation
- Responsive design

---

## How the Application Works

### Step 1

The user enters a number into the input field.

---

### Step 2

The user clicks the **Check** button.

---

### Step 3

The JavaScript program evaluates the entered number using predefined conditions.

---

### Step 4

Based on the evaluation, the application displays one of the following results:

- Easy
- Medium
- Strong

---

### Step 5

The user can enter another number and check the result again.

---

## Project Structure

```
Number-Strength-Checker/

│── index.html

│── style.css

│── script.js

│── README.md
```

---

## Sample Usage

### User Input

```
4
```

Output

```
Easy
```

---

### User Input

```
15
```

Output

```
Medium
```

---

### User Input

```
28
```

Output

```
Strong
```

---

## Learning Outcomes

This project helped me understand:

- HTML Forms
- CSS Styling
- JavaScript Variables
- Functions
- DOM Manipulation
- Event Handling
- Conditional Statements
- User Input Validation

---

## Future Improvements

- Dynamic strength meter
- Better UI animations
- Reset button
- Input history
- Dark mode
- Mobile-friendly enhancements

---

## Conclusion

The Number Strength Checker is a beginner-friendly JavaScript project that demonstrates how to accept user input, process it using conditional logic, and display meaningful results. It provides practical experience with DOM manipulation, event handling, and interactive web development.

## Overview
The Guess Number Game is a beginner-friendly JavaScript project that demonstrates how interactive web applications work using HTML, CSS, and JavaScript. It provides hands-on experience with DOM manipulation, user input handling, and game logic while offering an engaging user experience.
