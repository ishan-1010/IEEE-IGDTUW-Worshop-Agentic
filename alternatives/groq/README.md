# Level Up to Agentic AI: Hands-On Workshop

<a href="https://colab.research.google.com/drive/1PnV2Hao7X7gq1ek8UnK6jn2qUwb-xQGa?usp=sharing" target="_blank" rel="noopener noreferrer">[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1PnV2Hao7X7gq1ek8UnK6jn2qUwb-xQGa?usp=sharing)</a>
![Python 3](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![Groq API](https://img.shields.io/badge/Powered%20by-Groq-F55036?logo=groq&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

> **Build your first self-correcting AI agent — from scratch, for free, in 1 hour.**

Welcome to the **IEEE IGDTUW Workshop**! Today, you won't just *talk* about AI; you will **build** an autonomous agent that acts as a savage (but helpful) career coach.

Your agent will:

1. **Analyze** resume bullet points.
2. **Roast** the weak ones.
3. **Rewrite** them to be stronger.
4. **Critique its own work** to make it perfect.

---

## Quick Start (Do This Now)

You need exactly **3 things** to participate. Get them ready before we start!

### 1. Open the Notebook

Click the badge above or <a href="https://colab.research.google.com/drive/1PnV2Hao7X7gq1ek8UnK6jn2qUwb-xQGa?usp=sharing" target="_blank" rel="noopener noreferrer">**click here**</a> to open the student notebook in Google Colab.

### 2. Get Your Free API Key

1. Go to <a href="https://console.groq.com/keys" target="_blank" rel="noopener noreferrer">**Groq Console**</a>.
2. Click **"Create API key"**.
3. Click **"Create key"**.
4. Copy the key (it starts with `gsk_...`).

### 3. Setup in Colab

1. Inside Colab, click the **Key Icon** (secrets) in the left sidebar.
2. Add a new secret:
   * **Name:** `GROQ_API_KEY`
   * **Value:** *(Paste your key)*
3. Toggle **"Notebook access"** to **ON**.

### Optional: Local `.env` Setup (for VS Code/Jupyter)

If you are running locally instead of Colab Secrets:

1. Copy `.env.example` to `.env`
2. Put your real key in `.env`
3. Keep or change `GROQ_MODEL` as needed

Example:

```bash
cp .env.example .env
```

For a fast pre-session checklist, see `WORKSHOP_SETUP.md`.

---

## What You Will Learn

| Level             | concept                     | What You Build                                                      |
| ----------------- | --------------------------- | ------------------------------------------------------------------- |
| **Level 1** | **Structured Output** | Stop the LLM from yapping. Make it return JSON.                     |
| **Level 2** | **Tool Use**          | Give the LLM "eyes" to read recruiter guidelines.                   |
| **Level 3** | **Self-Correction**   | The "Reflection Pattern" — forcing the AI to fix its own mistakes. |
| **Bonus**   | **Deployment**        | Turn your code into a **shareable web app** with Gradio.     |

---

## Tech Stack

* **Google Colab** (Free Python Environment)
* **Groq** (Default: `llama-3.3-70b-versatile` — 70B, best for JSON. Change in Setup cell to try `qwen-3-32b`, `openai/gpt-oss-20b`, `openai/gpt-oss-120b`, or `meta-llama/llama-4-scout-17b-16e-instruct`.)
* **Gradio** (Instant Web UIs)

---

## Troubleshooting

**"I got an API Key Error!"**

* Did you add the secret in the left sidebar?
* Did you name it exactly `GROQ_API_KEY`?
* Did you toggle "Notebook access" to ON?

**"roast_my_resume is not defined" (Gradio cell)**

* Run the **Full Pipeline → Helpers** cell first (the one with `call_llm`, `get_role_requirements`, `roast_my_resume`). It must run before the Gradio "Deploy" cell.

**"Rate limit" / "429" / quota errors**

* Notebooks use **Groq with `llama-3.3-70b-versatile`** by default. If you changed the model, set it back to `llama-3.3-70b-versatile` in the Setup cell.
* Check usage and limits in <a href="https://console.groq.com" target="_blank" rel="noopener noreferrer">console.groq.com</a>. Verify `GROQ_API_KEY` in Colab Secrets/.env, and try a different model from the `GROQ_MODELS` list in the Setup cell.
* If you hit rate limits, wait and retry; the notebook already uses exponential backoff.

---

## Connect with the Speaker

**Ishan Katoch**

* **Role:** AI Engineer & Agentic AI Specialist
* **LinkedIn:** <a href="https://www.linkedin.com/in/ishan-katoch" target="_blank" rel="noopener noreferrer">Connect with me</a> (Tag me in your post!)

---

> **Note:** This repository includes a completed `solutions.ipynb` in case you get stuck. But try to build it yourself first!
