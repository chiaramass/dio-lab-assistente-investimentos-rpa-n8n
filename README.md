# AI-Driven Investment Recommendation Workflow (n8n)

## Overview
A hands-on automation project built with **n8n**, **Python**, and **Google Gemini**. This workflow demonstrates how financial services can automate data collection, match investor profiles with suitable investment options, and deliver personalized recommendations via email and API responses.

## Workflow Architecture
<img width="860" height="268" alt="image" src="https://github.com/user-attachments/assets/493aa651-2bdd-42a6-9f77-7c7434267bcb" />


## How It Works
1. **Trigger & Data Fetching:** Starts via a **Webhook** and uses an **HTTP Request** node to retrieve external investment and client data.
2. **Data Processing & Merging:** Uses custom logic (`Gerar Recomendacao`), a **Merge** node, and a **Code in Python** step to combine and structure the client profile with available investment options.
3. **AI Agent (Google Gemini):** An **AI Agent** powered by the **Gemini Chat Model** analyzes the merged data and generates a tailored investment recommendation message.
4. **Output & Delivery:** Formats the final response (`Montar Resposta`), returns the payload via **Respond to Webhook**, and sends the personalized message automatically through **Gmail**.

## Tech Stack & Tools
* **n8n** (Workflow Orchestration & AI Agent Node)
* **Google Gemini** (LLM Chat Model)
* **Python** (Data Processing within n8n)
* **Webhooks & REST APIs** (HTTP Request / Response)
* **Gmail Integration** (Automated Email Delivery)
