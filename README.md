# AI Email Agent with n8n, Gemini, and Gmail API

## 📌 Overview
This project is an **AI-powered email automation agent** built using **n8n**, **Google's Gemini model**, and the **Gmail API**.  
It allows you to **chat with an AI model**, which then generates professional emails and sends them directly to recipients via Gmail.

### Key Highlights
- AI chat interface powered by Google's Gemini model
- Automatic email generation and sending via Gmail API
- Simple memory system for maintaining context (database-backed)
- Designed for organization-level communication such as:
  - Leave requests  
  - Status updates  
  - Meeting follow-ups  
  - Automated daily/weekly reports

---

## ⚙️ Features
- **AI Agent Workflow**: Type a prompt in the chat tool → AI composes a professional email.
- **Secure Gmail API integration** with OAuth2 authentication.
- **Lightweight memory database** to maintain short-term context.
- **No-code/low-code automation** using n8n’s workflow builder.

---

## 🚀 Setup Instructions

1. **Clone this repository**
   ```bash
   git clone https://github.com/shubhamdhopat/ai-email-agent.git
   cd ai-email-agent
   ```

2. **Import Workflow into n8n**
   - Open your **n8n** instance.
   - Click **Import Workflow** and select the provided `.json` file.

3. **Configure Gmail API**
   - Create a Google Cloud Project.
   - Enable the Gmail API.
   - Add your n8n redirect URI under **Authorized Redirect URIs**:
     ```
     https://<your-domain>/rest/oauth2-credential/callback
     ```
   - Obtain your **Client ID** and **Client Secret**, then add them to your n8n credentials.

4. **Set Up Gemini API**
   - Obtain Gemini API credentials from [Google AI Studio](https://ai.google/).
   - Add them as environment variables or directly in **n8n credentials**.

5. **Run the Workflow**
   - Trigger the chat tool in **n8n**.
   - Type a prompt like:  
     *"Request leave from Aug 1–5, ensure tasks are delegated, and make it professional."*
   - The AI agent will generate the email and send it automatically.

---

## 🛠️ Tech Stack
- n8n – Workflow automation  
- Google Gemini API – AI text generation  
- Gmail API – Email sending  
- Simple Memory Database – Context retention

---

## 📄 License
This project is licensed under the **MIT License**.
