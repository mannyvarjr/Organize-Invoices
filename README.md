# 📄 AI-Powered Invoice Parser & Data Pipeline

###  Project Overview
This project automates the extraction and organization of data from PDF invoices. By combining the orchestration power of **n8n** with the reasoning capabilities of **Large Language Models (LLMs)**, this workflow transforms unstructured document data into clean, actionable records without manual data entry.

###  How It Works
* **Input**: User submits a name and a PDF invoice via an integrated **n8n Form Trigger**.
* **Extraction**: The system uses the **Extract from File** node to pull raw text data from the uploaded PDF.
* **Intelligence**: A **LangChain Basic LLM Chain** (GPT-4o-mini) processes the text to identify the invoice date, product descriptions, unit prices, and quantities.
* **Formatting**: A **Structured Output Parser** enforces a consistent JSON schema to ensure data integrity.
* **Distribution**: A **Split Out** node handles multiple line items, appending each as a unique row in **Google Sheets**.

###  Key Technical Features
* **LLM Orchestration**: Implements LangChain within n8n to handle complex data extraction that traditional OCR often misses.
* **Data Integrity**: Utilizes JSON schemas for structured output, ensuring a standardized database.
* **Scalability**: Built to handle complex invoices with multiple line items through automated data splitting and looping.

###  Tech Stack
* **Automation Platform**: n8n
* **AI Framework**: LangChain + OpenAI (GPT-4o-mini)
* **Data Storage**: Google Sheets (with optional Airtable integration)
* **Core Skills**: API Integration, Prompt Engineering, Data Mapping, and Workflow Optimization.
