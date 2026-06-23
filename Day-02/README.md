# Day 2 - Prompt Engineering

## Overview

Today I learned Prompt Engineering, which is the process of designing effective prompts to get accurate and useful responses from AI models.

---

# What is Prompt Engineering?

Prompt Engineering is the practice of writing clear instructions for AI systems to generate desired outputs.

### Example

Prompt:
Explain Python for beginners.

Output:
Python is an easy-to-learn programming language used for web development, AI, data science, and automation.

---

# Components of a Good Prompt

A good prompt contains:

### 1. Role

Defines who AI should act as.

Example:
You are a Python Teacher.

### 2. Task

Defines what AI should do.

Example:
Explain recursion.

### 3. Context

Provides background information.

Example:
Explain recursion to first-year engineering students.

### 4. Constraints

Adds limitations.

Example:
Keep the explanation under 100 words.

### 5. Output Format

Specifies how the answer should be presented.

Example:
Provide the answer in bullet points.

---

# Types of Prompt Engineering

## 1. Zero-Shot Prompting

No examples are provided.

### Example

Prompt:
Translate the following English sentence into Hindi:
"I love coding."

Output:
मुझे कोडिंग पसंद है।

---

## 2. One-Shot Prompting

One example is provided.

### Example

Input: Apple
Output: Fruit

Input: Rose
Output: Flower

---

## 3. Few-Shot Prompting

Multiple examples are provided.

### Example

Input: Dog → Mammal
Input: Eagle → Bird
Input: Snake → Reptile

Input: Frog

Output:
Amphibian

---

## 4. Chain of Thought Prompting

AI solves problems step by step.

### Example

Prompt:
A shopkeeper buys a pen for ₹20 and sells it for ₹25.
Calculate profit percentage.
Think step by step.

---

## 5. Self-Consistency Prompting

AI explores multiple reasoning paths and selects the best answer.

### Example

Question:
There are 3 boxes with 5 apples each.

Path 1:
3 × 5 = 15

Path 2:
5 + 5 + 5 = 15

Final Answer:
15 Apples

---

## 6. Role Prompting

Assign a role to AI.

### Example

Prompt:
You are a Data Scientist.
Explain Machine Learning.

---

## 7. Instruction Prompting

Give direct instructions.

### Example

Prompt:
Summarize the paragraph in 5 bullet points.

---

## 8. Contextual Prompting

Provide background information.

### Example

Prompt:
Rahul is a B.Tech student who knows Python and wants to learn AI.
Suggest a learning roadmap.

---

## 9. ReAct Prompting

Reason + Action.

### Example

Question:
Should I carry an umbrella in Delhi today?

AI:
Reason → Check weather
Action → Search weather
Answer → Carry an umbrella.

---

## 10. Tree of Thoughts Prompting

Explore multiple solutions before selecting the best one.

### Example

Problem:
How can a startup increase sales?

Options:

* Advertising
* Discounts
* Better Product

Best Solution:
Advertising + Better Product

---

## 11. Meta Prompting

AI creates prompts.

### Example

Prompt:
Create a prompt to learn Machine Learning in 30 days.

Output:
AI generates a complete roadmap prompt.

---

# Practice Tasks Completed

## Task 1: Translation

Prompt:
Translate English to Hindi while preserving meaning.

Input:
I love coding.

Output:
मुझे कोडिंग पसंद है।

---

## Task 2: Sentiment Analysis

Review:
The phone is amazing.

Output:
Positive

Review:
The laptop hangs frequently.

Output:
Negative

---

## Task 3: SQL Generation

Question:
Show all students whose marks are greater than 80.

SQL:
SELECT * FROM students
WHERE marks > 80;

---

## Task 4: Information Extraction

Input:

Name: Arash
Age: 19
Course: AI

Output:

{
"name":"Arash",
"age":19,
"course":"AI"
}

---

## Task 5: Animal Classification

Input:
Dog → Mammal
Eagle → Bird
Snake → Reptile

Question:
Frog → ?

Output:
Amphibian

---

## Task 6: Travel Planner Prompt

Role:
Travel Expert

Destination:
Goa

Budget:
₹15,000

Duration:
4 Days

Output:

* Day-wise itinerary
* Hotel suggestions
* Food recommendations
* Estimated cost

---

## Task 7: AI Study Assistant

Features:

* Explain Concepts
* Generate Quizzes
* Summarize Notes
* Create Flashcards
* Evaluate Answers

---

# Learning Outcomes

* Learned Prompt Engineering fundamentals.
* Practiced Zero-Shot, One-Shot, Few-Shot, and Chain of Thought prompting.
* Built prompts for travel planning, coding, study assistance, and sentiment analysis.
* Improved AI interaction and prompt design skills.

# Tools Used

* ChatGPT
* GitHub
* Markdown
* Prompt Engineering Techniques

# Conclusion

Successfully explored Prompt Engineering concepts and applied multiple prompting techniques through practical exercises and real-world examples.
