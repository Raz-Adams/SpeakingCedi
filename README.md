# 🇬🇭 Speaking Cedi: AI Financial Assistant

**Speaking Cedi** is a Telegram-based bot designed to make financial tracking as easy as sending a text. It uses AI to parse natural language, provides instant budgeting advice, and logs every transaction to a Google Sheet for long-term tracking.

---

## 🚀 Project Overview
The goal of this project is to eliminate the "friction" of manual expense tracking. Instead of opening a complex app, I simply text my bot.

### The Stack
* **The "Face":** [Telegram](https://telegram.org) (via BotFather)
* **The "Brain":** [OpenAI API](https://openai.com) (GPT-4o-mini)
* **The "Home":** [PythonAnywhere](https://www.pythonanywhere.com) (hosting for 24/7 uptime)
* **The "Memory":** [Google Sheets API](https://developers.google.com/sheets/api) (as a lightweight database)

---

## 🛠️ Implementation Journey

### Phase 1: Infrastructure
- Created the bot identity via **BotFather** on Telegram (`@SpeakingCediBot`).
- Set up a **PythonAnywhere** environment using a Bash console to install necessary libraries for Telegram and OpenAI communication.
- Initialized the bot to respond to basic commands like "Who are you?".

### Phase 2: Data Pipeline (Google Sheets)
- Created a Google Cloud project (`financebot`) and enabled the **Google Drive** and **Sheets APIs**.
- Generated a **Service Account** and JSON key to allow the Python script to write data securely.
- Formatted a Google Sheet with specific column headers for automated logging.

---

## 🔍 Troubleshooting & Lessons Learned

### 1. Bash vs. Python Consoles
I learned the distinction between a **Bash console** (used for system-level tasks and installing libraries) and a **Python console** (used for running code snippets).

### 2. The "Chatty AI" JSON Error
During development, I hit a `Expecting value: line 1 column 1 (char 0)` error.
* **The Issue:** The AI was being too conversational. It would reply with "Sure! {amount: 40}", but the Python code only wanted the data in the curly brackets `{}`.
* **The Fix:** I refined the AI's instructions to be less conversational and focus purely on returning structured data. This "thinned out" the response so the code could read it perfectly.

---

## ✅ Current Status
- [x] Telegram-to-AI communication established.
- [x] 24/7 hosting on PythonAnywhere.
- [x] Natural language parsing of expenses.
- [x] Successful data logging to Google Sheets.

## 🔜 Next Steps
- [ ] Implement a `.env` file and `.gitignore` for API key security.
- [ ] Add categorization logic (e.g., Food, Transport, Rent).
- [ ] Build a simple dashboard in Google Sheets to visualize spending.

---
*Created by [Abdul-Razaak B. Adams]*
