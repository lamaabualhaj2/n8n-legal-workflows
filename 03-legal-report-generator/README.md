# 📄 Legal Report Generator

## Overview
A workflow that converts a full legal consultation chat into a formal official legal report,
based on Jordanian law and structured for professional use in law firms.

## How it works
1. User sends the full chat conversation via POST request to the Webhook
2. OpenAI GPT-4o analyzes the conversation and extracts all legal facts
3. Generates a complete formal legal report
4. Returns the report as JSON

## Nodes
| Node | Description |
|------|-------------|
| Webhook | Receives POST requests at `/legal-summary` |
| OpenAI - Generate Legal Text | GPT-4o generates the full legal report |
| Respond to Webhook | Returns the report as `legal_text` |

## Input Parameters
| Parameter | Description |
|-----------|-------------|
| `consultation_id` | Unique consultation reference number |
| `user_name` | Client's full name |
| `lawyer_name` | Assigned lawyer's name |
| `lawyer_spec` | Lawyer's specialization |
| `consultation_date` | Date of the consultation |
| `message_count` | Total number of messages in the chat |
| `report_date` | Date the report was generated |
| `chat_text` | Full conversation content |

## Report Structure
1. **Case Type** — Nature of the legal issue
2. **Facts Summary** — Neutral formal summary of all facts
3. **Legal Issues** — Key legal questions raised
4. **Legal Classification** — Preliminary legal analysis
5. **Recommendations** — Available legal actions and next steps
6. **Lawyer Notes** — Additional observations and warnings

## System Prompt Rules
- Strictly based on Jordanian law and constitution
- No invented facts — only what is stated in the conversation
- Preserves all roles correctly (tenant vs landlord, creditor vs debtor)
- Formal Modern Standard Arabic output only
- Temperature set to 0 for maximum accuracy

## Tech Stack
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
