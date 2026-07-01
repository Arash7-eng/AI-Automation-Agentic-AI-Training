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

## Screenshots

- Complete Workflow
- AI Agent Configuration
- JavaScript Node
- Switch Node
- Google Sheets Configuration
- HTML Form
- Final Google Sheets Output

---

## Conclusion

This project demonstrates how Artificial Intelligence and workflow automation can simplify expense management by automatically categorizing expenses and storing them efficiently. It is a practical example of integrating AI with n8n to build intelligent automation solutions.
# Guess Number Game

## Overview

The Guess Number Game is a simple interactive web application developed using HTML, CSS, and JavaScript. The objective of the game is to guess a randomly generated number within a limited number of attempts.

The game provides instant feedback after every guess, making it an excellent beginner-friendly JavaScript project for understanding user interaction, conditional statements, loops, and random number generation.

---

## Project Objective

To build an interactive browser-based game where users can guess a randomly generated number and receive hints until they either win or run out of attempts.

---

## Technologies Used

- HTML5
- CSS3
- JavaScript

---

## Features

- Random number generation
- User-friendly interface
- Input validation
- Instant feedback
- Winning and losing messages
- Restart game functionality
- Responsive design

---

## How the Game Works

### Step 1

When the game starts, JavaScript generates a random number.

---

### Step 2

The player enters a number in the input box.

---

### Step 3

The game compares the entered number with the randomly generated number.

Possible responses:

- Too High
- Too Low
- Correct Guess

---

### Step 4

The game continues until:

- The correct number is guessed.
- The maximum number of attempts is reached.

---

### Step 5

After the game ends, the player can restart and play again.

---

## Project Structure

Guess-Number-Game/

│── index.html

│── style.css

│── script.js

│── images/

│── README.md

---

## Sample Gameplay

Random Number:
37

Player Guess:
25

Output:

Too Low! Try Again.

Player Guess:
45

Output:

Too High! Try Again.

Player Guess:
37

Output:

Congratulations! You guessed the correct number.

---

## Learning Outcomes

This project helped me understand:

- JavaScript Variables
- Functions
- DOM Manipulation
- Event Handling
- Random Number Generation
- Conditional Statements
- Loops
- User Input Validation

---

## Future Improvements

- Difficulty Levels
- Score System
- Timer
- Sound Effects
- Dark Mode
- High Score Board
- Multiplayer Mode

---

## Screenshots

- Home Screen
- Gameplay
- Winning Screen
- Losing Screen

---

## Conclusion

The Guess Number Game is a beginner-friendly JavaScript project that demonstrates how interactive web applications work using HTML, CSS, and JavaScript. It provides hands-on experience with DOM manipulation, user input handling, and game logic while offering an engaging user experience.
