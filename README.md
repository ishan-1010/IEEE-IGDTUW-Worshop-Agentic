# Level Up to Agentic AI: Hands-On Workshop

<a href="https://colab.research.google.com/drive/1T4TVh-2A1-i4IBTh0v2B-rLAefw7S52a?usp=sharing" target="_blank" rel="noopener noreferrer">[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1T4TVh-2A1-i4IBTh0v2B-rLAefw7S52a?usp=sharing)</a>
![Python 3](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![Gemini API](https://img.shields.io/badge/Powered%20by-Gemini-4E86F8?logo=google&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

> **Build your first self-correcting AI agent — from scratch, for free, in 1 hour.**

Welcome to the **IEEE IGDTUW Workshop**! Today, you won't just *talk* about AI; you will **build** an autonomous agent that acts as a savage (but helpful) career coach.

Your agent will:
1.  **Analyze** resume bullet points.
2.  **Roast** the weak ones.
3.  **Rewrite** them to be stronger.
4.  **Critique its own work** to make it perfect.

---

## Quick Start (Do This Now)

You need exactly **3 things** to participate. Get them ready before we start!

### 1. Open the Notebook
Click the badge above or <a href="https://colab.research.google.com/drive/1T4TVh-2A1-i4IBTh0v2B-rLAefw7S52a?usp=sharing" target="_blank" rel="noopener noreferrer">**click here**</a> to open the student notebook in Google Colab.

### 2. Get Your Free API Key
1.  Go to <a href="https://aistudio.google.com" target="_blank" rel="noopener noreferrer">**Google AI Studio**</a>.
2.  Click **"Get API Key"**.
3.  Click **"Create API key in new project"**.
4.  Copy the key (it starts with `AIza...`).

### 3. Setup in Colab
1.  Inside Colab, click the **Key Icon** (secrets) in the left sidebar.
2.  Add a new secret:
    *   **Name:** `GEMINI_API_KEY`
    *   **Value:** *(Paste your key)*
3.  Toggle **"Notebook access"** to **ON**.

### Optional: Local `.env` Setup (for VS Code/Jupyter)

If you are running locally instead of Colab Secrets:

1. Copy `.env.example` to `.env`
2. Put your real key in `.env`

Example:

```bash
cp .env.example .env
```

For a fast pre-session checklist, see `WORKSHOP_SETUP.md`.

---

## What You Will Learn

| Level | concept | What You Build |
|---|---|---|
| **Level 1** | **Structured Output** | Stop the LLM from yapping. Make it return JSON. |
| **Level 2** | **Tool Use** | Give the LLM "eyes" to read recruiter guidelines. |
| **Level 3** | **Self-Correction** | The "Reflection Pattern" — forcing the AI to fix its own mistakes. |
| **Bonus** | **Deployment** | Turn your code into a **shareable web app** with Gradio. |

---

## Tech Stack

*   **Google Colab** (Free Python Environment)
*   **Gemini 2.5 Flash** (Default model; most reliable free tier. Use `gemini-2.5-flash` in Setup.)
*   **Gradio** (Instant Web UIs)

---

## Troubleshooting

**"I got an API Key Error!"**
*   Did you add the secret in the left sidebar?
*   Did you name it exactly `GEMINI_API_KEY`?
*   Did you toggle "Notebook access" to ON?

**"roast_my_resume is not defined" (Gradio cell)**
*   Run the **Full Pipeline → Helpers** cell first (the one with `call_llm`, `get_role_requirements`, `roast_my_resume`). It must run before the Gradio "Deploy" cell.

**"Resource Exhausted" / "429" / "limit: 0"**
*   Notebooks use **gemini-2.5-flash** by default (most reliable free tier). If you changed the model, set it back to `genai.GenerativeModel('gemini-2.5-flash')` in the Setup cell.
*   If you see **limit: 0**, your project has no quota — create the key from <a href="https://aistudio.google.com/app/apikey" target="_blank" rel="noopener noreferrer">aistudio.google.com/app/apikey</a>, enable **Generative Language API** in Cloud Console, or try another Google account.
*   Daily limit resets at midnight Pacific.

---

## Connect with the Speaker

**Ishan Katoch**
*   **Role:** AI Engineer & Agentic AI Specialist
*   **LinkedIn:** <a href="https://www.linkedin.com/in/ishan-katoch" target="_blank" rel="noopener noreferrer">Connect with me</a> (Tag me in your post!)

---

> **Note:** This repository includes a completed `solutions.ipynb` in case you get stuck. But try to build it yourself first!

> **Presenters:** See `PRESENTER.md` for a minute-by-minute workshop runbook.
