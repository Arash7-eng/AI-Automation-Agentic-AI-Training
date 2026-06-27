# Project Implementation

During Day 05, I successfully developed two AI-powered automation projects using **n8n**, **Google Gemini Chat Model**, **AI Agents**, **Webhooks**, and **HTML Forms**. These projects demonstrate how Artificial Intelligence can automate real-world tasks by processing user input and generating intelligent, personalized responses.

---

# Project 1: AI Travel Planner using n8n AI Agent

## Step 1: Designing the HTML Travel Planner Form

The project began by creating a user-friendly HTML form to collect travel preferences. The form was designed with essential input fields, allowing users to provide:

* Starting City
* Destination
* Number of Travel Days
* Budget
* Travel Style

The form was configured to send user information to the n8n Webhook using the **HTTP POST** method.

---

## Step 2: Configuring the Webhook Node

The Webhook node was created as the starting point of the workflow. It receives the data submitted from the HTML form and triggers the automation process.

**Configuration**

* HTTP Method: POST
* Authentication: None
* Custom Webhook Path

Once the form is submitted, the workflow starts automatically.

---

## Step 3: Processing User Data with Edit Fields

After receiving the data, the **Edit Fields** node organizes and formats the travel details into a structured AI prompt.

The prompt contains:

* Starting City
* Destination
* Number of Days
* Budget
* Travel Style

This ensures that the AI receives well-structured information for generating accurate travel recommendations.

---

## Step 4: Connecting the Google Gemini Chat Model

The Google Gemini Chat Model was integrated into the workflow to provide Artificial Intelligence capabilities.

Gemini analyzes the formatted prompt, understands the user's travel preferences, and prepares intelligent responses.

---

## Step 5: Configuring the AI Agent

The AI Agent acts as the decision-making component of the workflow.

Its responsibilities include:

* Reading the structured prompt.
* Understanding user travel requirements.
* Sending the prompt to Google Gemini.
* Receiving the generated response.
* Returning a personalized travel itinerary.

---

## Step 6: Generating the Final Travel Itinerary

After processing the request, the AI Agent generates a detailed travel plan containing:

* Trip Summary
* Day-wise Itinerary
* Tourist Attractions
* Local Food Recommendations
* Estimated Budget Breakdown
* Transportation Suggestions
* Travel Tips
* Safety Guidelines

The complete response is generated automatically without manual intervention.

---

# Travel Planner Workflow

HTML Travel Form

↓

Webhook

↓

Edit Fields

↓

Google Gemini Chat Model

↓

AI Agent

↓

Personalized Travel Itinerary

---

# Project 2: AI Shopping Assistant using n8n AI Agent

## Step 1: Designing the HTML Shopping Form

The second project involved creating an intelligent shopping assistant.

A dedicated HTML form was developed to collect shopping preferences, including:

* Product Category
* Product Name
* Budget
* Preferred Brand
* Purpose of Purchase

The form submits user information to the n8n Webhook using the **HTTP POST** method.

---

## Step 2: Configuring the Shopping Webhook

A separate Webhook node was configured to receive shopping details from the HTML form.

**Configuration**

* HTTP Method: POST
* Authentication: None
* Custom Webhook Path

This node acts as the entry point for the shopping assistant workflow.

---

## Step 3: Formatting Data using Edit Fields

The **Edit Fields** node converts the user inputs into a structured prompt before sending the request to the AI Agent.

The formatted prompt includes:

* Product Category
* Product Name
* Budget
* Brand Preference
* Purpose of Purchase

This improves the quality and accuracy of AI-generated recommendations.

---

## Step 4: Integrating Google Gemini Chat Model

The Google Gemini Chat Model processes the shopping prompt and analyzes the user's requirements.

It understands:

* Product type
* Budget limitations
* Brand preferences
* Intended purpose

Based on this information, Gemini prepares intelligent shopping recommendations.

---

## Step 5: Configuring the AI Agent

The AI Agent coordinates communication between the workflow and the Gemini model.

Its responsibilities include:

* Understanding shopping requirements.
* Sending prompts to Gemini.
* Receiving AI-generated recommendations.
* Returning the final shopping guide.

---

## Step 6: Generating Shopping Recommendations

The AI Shopping Assistant automatically produces a detailed recommendation containing:

* Product Overview
* Top 5 Recommended Products
* Product Features
* Price Range
* Pros and Cons
* Best Value for Money Recommendation
* Buying Tips
* Final Recommendation

The complete response is generated within seconds based on the user's preferences.

---

# Shopping Assistant Workflow

HTML Shopping Form

↓

Webhook

↓

Edit Fields

↓

Google Gemini Chat Model

↓

AI Agent

↓

Personalized Shopping Recommendations

---

# Skills Gained

Through these two projects, I gained practical experience in:

* Artificial Intelligence Fundamentals
* AI Agent Development
* Workflow Automation using n8n
* Google Gemini Chat Model Integration
* Webhook Configuration
* Prompt Engineering
* HTML Form Development
* Data Processing using Edit Fields
* AI-powered Response Generation
* Intelligent Workflow Design
* Real-world Automation Solutions

---

# Conclusion

By completing both the **AI Travel Planner** and **AI Shopping Assistant**, I gained hands-on experience in designing intelligent automation workflows using **n8n**, **Google Gemini**, and **AI Agents**. These projects demonstrated how AI can automate complex tasks, process user input, generate personalized recommendations, and improve user experience. They strengthened my understanding of workflow automation, prompt engineering, AI integration, and practical application development while showcasing how modern AI tools can solve real-world problems efficiently.
