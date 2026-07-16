# 🤖 Telegram AI Chatbot Automation (n8n)

An automated AI-powered Telegram chatbot built with **n8n**, integrating **OpenAI** for natural language responses. This project demonstrates a no-code/low-code approach to building conversational AI bots using workflow automation.

🔗 **Live Bot:** [@SmartAI_Automation_bot](https://t.me/SmartAI_Automation_bot)

---

## 📋 Overview

This n8n workflow listens for incoming Telegram messages, sends them to an AI model (OpenAI) for processing, and replies to the user automatically — enabling a fully automated conversational assistant without a traditional backend server.

## ⚙️ How It Works

1. **Telegram Trigger** — listens for new messages sent to the bot
2. **Message Processing** — extracts and formats the user's input
3. **AI Node (OpenAI)** — sends the message to an LLM and receives a response
4. **Telegram Send Message** — replies to the user with the AI-generated answer
5. **Error Handling** — if the AI node fails, a fallback message is automatically sent to the user instead of leaving them without a reply

## ✨ Features

- Real-time Telegram message handling
- AI-powered natural language responses (OpenAI)
- Fully visual, no-code workflow (built in n8n)
- Easily customizable and extendable (add memory, commands, media handling, etc.)
- Built-in error handling — sends a graceful fallback message if the AI request fails
- Credential-safe design — no secrets stored in the workflow file

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Automation Platform | [n8n](https://n8n.io) |
| Messaging Platform | Telegram Bot API |
| AI Model | OpenAI GPT |
| Hosting (optional) | n8n Cloud / Self-hosted (Docker, VPS) |

## 📦 Repository Structure

```
telegram-ai-chatbot-n8n/
│
├── workflow.json          # Exported n8n workflow (import-ready)
├── README.md               # Project documentation
├── .gitignore               # Files/folders excluded from Git
├── LICENSE                  # MIT License
├── screenshots/
│   ├── workflow.png         # Screenshot of the n8n canvas
│   └── demo.png              # Screenshot of a live chat demo
└── docs/
    └── setup-guide.md        # Step-by-step setup instructions
```

## 🚀 Getting Started

### Prerequisites

- An [n8n](https://n8n.io) instance (Cloud or self-hosted)
- A Telegram Bot Token (from [@BotFather](https://t.me/BotFather))
- An OpenAI API key

## 🔐 Security Note

This repository does **not** contain any API keys, tokens, or credentials. All sensitive values are managed through n8n's built-in **Credentials** system and must be configured locally after import. See the setup guide for details.

## 🗺️ Roadmap / Ideas

- [ ] Add conversation memory (context retention)
- [ ] Add support for image/voice message inputs
- [ ] Add custom bot commands (`/start`, `/help`, etc.)
- [ ] Deploy on a persistent server with webhook mode

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 🙋 Author

Built by Pari Agrawal. Feel free to connect or reach out with questions!
