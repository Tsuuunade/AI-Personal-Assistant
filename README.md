# AI-Personal-Assistant

# AI Personal Assistant Workflows (n8n Demo Suite)

This repository contains a set of AI-powered agents integrated with the [n8n](https://n8n.io/) automation platform. The agents demonstrate modular task automation for handling emails, calendar events, research queries, and personal assistance via Telegram.

---

## 🧠 Overview

Each agent workflow serves a dedicated function and can be used independently or in combination as part of a larger AI Personal Assistant. These workflows leverage OpenAI's language model integration with Google services, Wikipedia, SerpAPI, and more.

### Included Agents

| Agent              | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Email Agent        | Handles professional Gmail email generation, retrieval, and replies.        |
| Calendar Agent     | Schedules, updates, and queries calendar events via Google Calendar.        |
| Research Agent     | Searches information using Wikipedia, Hacker News, and SerpAPI.             |
| AI Personal Assistant | Combines all above agents with a Telegram interface and contact database. |

---

## 📁 File Descriptions

| File Name                  | Purpose                                 |
|---------------------------|-----------------------------------------|
| `Email_Agent_Demo.json`   | Automates composing, sending, and retrieving emails via Gmail. |
| `Calendar_Agent_Demo.json`| Enables scheduling and retrieving Google Calendar events.         |
| `Research_Agent_Demo.json`| Performs intelligent research using multiple data sources.       |
| `AI_Personal_Assistant.json` | Central AI assistant integrating all tools with contact lookup and Telegram interface. |

---

## 🔧 Setup Instructions

1. **Install n8n**: Follow the [official guide](https://docs.n8n.io/hosting/installation/) to set up n8n on your environment.

2. **Import Workflows**: Upload the provided `.json` files via the n8n UI.

3. **Credentials Configuration**:
   - Gmail and Google Calendar OAuth2 credentials
   - OpenAI API key
   - SerpAPI key
   - Telegram Bot API token
   - Google Sheets link for Contact Database (for the Personal Assistant)

4. **Enable Webhooks**:
   - Ensure all workflows with Telegram triggers have active webhooks.
   - Provide valid contact entries in the Google Sheets document for lookup.

---

## 🧪 Agent Behaviors

### 📧 Email Agent
- Removes placeholders and finalizes email drafts.
- Replies using a consistent professional signature ("Nate").
- Supports sending and retrieving Gmail messages.

### 📅 Calendar Agent
- Automatically determines appropriate actions: create, retrieve, or invite.
- Supports event creation with or without attendees.
- Time parsing includes 1-day buffers for lookups.

### 🔍 Research Agent
- Tool selection hierarchy: Wikipedia → Hacker News → SerpAPI.
- Only one tool is called per query to optimize performance.

### 🤖 AI Personal Assistant
- Handles user queries via Telegram.
- Verifies contact info before proceeding with email or calendar actions.
- Ensures precision by enforcing a tool sequence (Contacts → Email/Calendar).

---

## 📝 Example Use Cases

- “Schedule a call with Alice on Friday at 2 PM.”
- “Send an email to John: 'Let's move the meeting to Monday.'”
- “Get me 3 recent articles about quantum computing.”

---

## 📎 Credits

Built with:
- [n8n](https://n8n.io/)
- [OpenAI](https://openai.com/)
- [SerpAPI](https://serpapi.com/)
- [Google Workspace APIs](https://developers.google.com/)
- [Telegram Bot API](https://core.telegram.org/bots)

---

## 📜 License

MIT License. See `LICENSE` for details.

---

## 🚀 Future Improvements

- Add authentication and session memory persistence
- Expand contact database integrations
- Integrate voice interface for assistant

---

