# 🤖 Legal Chatbot — AI Legal Assistant

## Overview
An AI-powered legal chatbot built with n8n and OpenAI, specialized in Jordanian law.
Provides legal guidance and clarification based on the latest Jordanian legislation.

## How it works
1. User sends a message via POST request to the webhook
2. AI Agent processes the message using GPT-4.1-mini
3. Responds with legal guidance based on Jordanian law
4. Simple Memory stores the last 10 messages for context

## Nodes
| Node | Description |
|------|-------------|
| Webhook | Receives POST requests at `/website` |
| AI Agent | Processes messages with legal system prompt |
| OpenAI Chat Model | GPT-4.1-mini for responses |
| Simple Memory | Keeps context of last 10 messages |
| Respond to Webhook | Returns the AI response |

## System Prompt Rules
- Responds **only** under Jordanian law
- Uses formal Modern Standard Arabic
- Provides legal rights and pathways
- Refuses non-legal questions

## Tech Stack
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
