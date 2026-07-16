# 🛠️ Setup Guide

This guide explains how to import and run this n8n workflow on your own instance.

## 1. Prerequisites

- An n8n instance — [n8n Cloud](https://n8n.io) or self-hosted (Docker/npm)
- A Telegram bot token from [@BotFather](https://t.me/BotFather)
- An OpenAI API key ([platform.openai.com](https://platform.openai.com)) or Google Gemini API key ([ai.google.dev](https://ai.google.dev))

## 2. Create Your Telegram Bot

1. Open Telegram and message [@BotFather](https://t.me/BotFather)
2. Run `/newbot` and follow the prompts
3. Copy the **Bot Token** you receive — you'll need it in Step 4

## 3. Import the Workflow

1. Open your n8n instance
2. Go to **Workflows** → click **Import from File**
3. Select `workflow.json` from this repository
4. The workflow will appear on the canvas with all nodes and connections, but **without any credentials attached**

## 4. Add Your Credentials

You'll need to create two credentials inside n8n (these are stored securely by n8n, not in this repo):

### Telegram credential
1. Click the **Telegram Trigger** or **Telegram** node
2. Under **Credential**, click **Create New**
3. Paste your Bot Token from Step 2
4. Save

### OpenAI / Gemini credential
1. Click the **AI node** (OpenAI or Gemini)
2. Under **Credential**, click **Create New**
3. Paste your API key
4. Save

## 5. Set the Telegram Webhook (if self-hosting)

If you're self-hosting n8n, make sure your instance is reachable via a public HTTPS URL (or use n8n's tunnel feature for testing). n8n handles Telegram webhook registration automatically once the Telegram Trigger node is activated.

## 6. Activate the Workflow

Toggle the workflow to **Active** in the top-right corner of the canvas. Your bot is now live — message it on Telegram to test.

## 7. Troubleshooting

| Issue | Likely Cause |
|---|---|
| Bot doesn't respond | Workflow not activated, or webhook not registered |
| "Unauthorized" error | Invalid or expired bot token |
| AI node fails | Invalid API key, or usage limits reached |
| Import fails | Make sure you're using a compatible n8n version |

## 8. Customization Ideas

- Add a **Switch** node to handle bot commands like `/start` or `/help`
- Add a **Memory/Database node** (e.g., Postgres, Redis) to retain conversation context
- Add error-handling nodes to send a fallback message if the AI call fails
