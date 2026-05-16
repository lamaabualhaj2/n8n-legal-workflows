# ✍️ Legal Text Formatter

## Overview
A workflow that converts any informal or colloquial text into formal legal Arabic (Modern Standard Arabic),
while preserving the original meaning and all details without adding or removing anything.

## How it works
1. User sends the text via POST request to the Webhook
2. AI Agent rewrites the text in formal legal Arabic
3. Returns the formatted text as JSON

## Nodes
| Node | Description |
|------|-------------|
| Webhook | Receives POST requests at `/normalize-message-v2` |
| AI Agent | Rewrites the text in formal legal Arabic |
| OpenAI Chat Model | GPT-4.1-mini for text reformulation |
| Respond to Webhook | Returns the formatted text as `final_text` |

## System Prompt Rules
- Does NOT add any information not present in the original text
- Does NOT remove any details
- Preserves all numbers, dates, and names exactly as stated
- If the input is in English, translates it first then rewrites in formal Arabic

## Tech Stack
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
