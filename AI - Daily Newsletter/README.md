# AI Daily Newsletter Pipeline

## 📌 Overview
A modular automation system designed to eliminate manual research and curation. This pipeline aggregates specific RSS feeds across Tech and Finance, filters them by date, and uses AI agents to score their importance before generating a categorized HTML newsletter.


<img width="2286" height="851" alt="Screenshot 2026-04-21 191620" src="https://github.com/user-attachments/assets/4d5ebab5-8270-4282-97c5-182e3890b936" />


## 🏗 Architecture & Logic
Rather than building one massive, unmaintainable workflow, this system is broken down into an **Orchestrator** and reusable **Tools**:

* **Orchestrator:** Triggers daily, sets date variables, and utilizes LangChain AI Agents to execute the downstream tools.
* **Sub-Workflows (Tools):** Independent workflows that handle specific data sources (e.g., `Tool - AI Financial News`, `Tool - AI Research Papers`). They fetch, parse, normalize, and de-duplicate the raw XML/RSS data using custom JavaScript.
* **LLM Integration:** Groq (Llama 3.1) and Gemini handle the heavy lifting of scoring the news on a 1-100 scale and converting raw JSON data into clean HTML list items.

## ⚙️ Status
**Status:** Active / Iterating. Currently refining the importance-scoring prompt to better filter out low-value PR announcements.
