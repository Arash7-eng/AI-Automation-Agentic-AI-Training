# Day 04 - n8n Workflow Automation and Google Sheets Integration

## Overview

On Day 04, I learned the fundamentals of workflow automation using n8n. I explored how to automate tasks, connect applications, receive data through webhooks, and store information automatically in Google Sheets.

As a practical implementation, I built a Student Registration Automation System that collects student information through an HTML form and automatically stores the submitted data in a Google Spreadsheet.

---

# What is n8n?

n8n is an open-source workflow automation platform that enables users to connect different applications and automate repetitive tasks through a visual workflow builder.

It allows data to move automatically between applications without requiring extensive coding knowledge.

---

# Why Use n8n?

* Automates repetitive tasks
* Saves time and effort
* Reduces manual work
* Minimizes human errors
* Connects multiple applications
* Supports APIs and Webhooks
* Improves workflow efficiency

---

# Key Features of n8n

* Visual Workflow Builder
* Webhook Integration
* API Connectivity
* Data Transformation
* Google Sheets Integration
* Automation Triggers
* Real-Time Processing
* Open-Source Platform

---

# Applications of n8n

n8n can be used for:

* Form Automation
* Data Collection
* Spreadsheet Automation
* Email Notifications
* API Integrations
* Database Operations
* Task Scheduling
* Workflow Management

---

# Project Title

Student Registration Automation using n8n and Google Sheets

---

# Project Objective

The objective of this project is to automate the process of collecting and storing student registration information.

Instead of manually entering data into a spreadsheet, the workflow automatically receives form submissions and stores them in Google Sheets.

---

# Technologies Used

* n8n
* HTML
* Webhooks
* Google Sheets
* Workflow Automation

---

# Project Workflow

Student Registration Form

↓

Webhook Node

↓

Google Sheets Node

↓

Student Data Stored Automatically

---

# Project Description

A Student Registration Form was created using HTML. The form collects the following information:

* Student Name
* Email Address
* Course Name

When a user submits the form:

1. The form sends data to an n8n Webhook.
2. The Webhook receives the submitted information.
3. The workflow is triggered automatically.
4. The Google Sheets node processes the data.
5. A new row is added to the spreadsheet.

This automation eliminates manual data entry and ensures accurate record management.

---

# Implementation Steps

## Step 1: Created Student Registration Form

Designed an HTML form containing:

* Name Field
* Email Field
* Course Field
* Submit Button

## Step 2: Configured Webhook

Created and configured a Webhook node in n8n to receive form submissions through HTTP POST requests.

## Step 3: Integrated Google Sheets

Connected Google Sheets with n8n and configured the Append Row operation for automatic data storage.

## Step 4: Tested the Workflow

Submitted sample student data and verified successful transfer of information from the form to Google Sheets.

---

# Learning Outcomes

Through this project, I learned:

* Introduction to Workflow Automation
* Understanding n8n Interface
* Creating Automated Workflows
* Working with Webhooks
* Connecting External Services
* Google Sheets Integration
* Data Mapping Techniques
* Real-Time Data Processing

---

# Screenshots

### 1. n8n Dashboard

Overview of the n8n workspace and workflow creation interface.

### 2. Student Registration Form

HTML form used for collecting student information.

### 3. Webhook Configuration

Webhook setup used to receive form submissions.

### 4. Google Sheets Output

Automated storage of student records inside Google Sheets.

---

# Conclusion

This project provided hands-on experience with workflow automation using n8n. By integrating an HTML form, Webhook, and Google Sheets, I successfully built an automated student registration system that collects and stores data efficiently without manual intervention.
