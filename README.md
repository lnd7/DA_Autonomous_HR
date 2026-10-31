# DYNAMIC ACQUISITION (DA) AUTONOMOUS HR
Dynamic Acquisition (DA) is an AI-driven HR agent powered by n8n and Gemini. It autonomously ingests resumes, evaluates candidates against job criteria, and executes a 3-tier routing matrix: instantly sending tailored rejections, distributing assessments, or booking Google Meet interviews on HR calendars.

### Live Production 
Interact with the live agent here: **https://lnd7.app.n8n.cloud/form/91c35cf6-1e30-480c-87c7-ddfaccc2c537**

## How It Works?
* **1. Ingestion:** Extracts text from PDF resumes and fetches exact job requirements from Google Sheets.
* **2. AI Evaluation:** Gemini evaluates the candidate's skills and assigns a tier (High, Medium, or Low).
* **3. Autonomous Actions:** 
  * **High-Tier:** Automatically calculates working hours and books a Google Meet interview on the HR calendar.
  * **Medium-Tier:** Emails technical assessment links to the candidate.
  * **Low-Tier:** Sends a polite, AI-reasoned rejection email.

## Tech Stack
* **Orchestration:** n8n
* **AI Engine:** Google Gemini
* **Integrations:** Google Workspace (Sheets, Gmail, Calendar, Meet)

## Repository Contents
This repository contains the `DA-Autonomous-HR-Screening.json` architecture file. The active engine runs on a dedicated production server. And a folder contains some sample resumes used for evaluating the project.

**To run locally:**
1. Clone this repository.
2. In your n8n instance, go to **Workflows** > **Import from File** and select the JSON file.
3. Re-authenticate your Google and Gemini credentials.
