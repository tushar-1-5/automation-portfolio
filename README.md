Workflow Automation Projects
<img width="2286" height="851" alt="image" src="https://github.com/user-attachments/assets/70face4d-3443-4eca-b71e-5d92d26d288d" />
AI - Daily Newsletter


Welcome to my automation portfolio. This repository showcases my hands-on projects using self-hosted infrastructure and AI agents to solve operational bottlenecks.
Instead of relying on simple integrations, my goal is to practice building modular and reliable systems.

## 🛠 Tech Stack & Infrastructure
* **Core Orchestration:** n8n (Self-hosted via Docker)
* **AI & LLMs:** Google Gemini, Groq (Llama/Qwen)
* **Media Processing:** FFmpeg (CLI integration)
* **Integrations:** YouTube API, Google Drive API, Telegram Bots, Webhooks, Pexels API
* **Data Parsing:** Custom JavaScript code nodes, RSS parsing, Regex

---

## 🚀 Featured Projects

### 1. [AI Daily Newsletter Pipeline](./AI-Daily-Newsletter)
An end-to-end data aggregation engine that ingests daily tech and financial RSS feeds. Instead of a messy single-canvas workflow, this system utilizes a master **Orchestrator** that calls independent **Tool Workflows**, passing parameters to LLMs to score, summarize, and categorize high-value news into a clean HTML newsletter.

### 2. [Automated Shorts Generator (Human-in-the-Loop)](./Automated-Shorts-Generator)
A complete video generation pipeline that sources quotes/content, generates relevant audio, and renders final MP4 files using local FFmpeg commands. Crucially, this system integrates a Telegram bot to enforce a **human-in-the-loop approval process**, halting the workflow until a user reviews and approves the AI-generated caption and image.

---
*Note: Sensitive data (emails, API keys, personal Webhook IDs, and Drive folders) have been sanitized from these JSON files for public viewing.*
