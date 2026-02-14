# Level Up to Agentic AI: Hands-On Workshop for Future Builders

> Build your first self-correcting AI agent — from scratch, for free, in 1 hour.

A hands-on workshop where students build a **"Roast My Resume" AI Agent** — an autonomous system that analyzes resume bullet points, roasts the weak ones, rewrites them stronger, and then *critiques its own rewrite* to improve it further. All built from scratch in Python, running on Google Colab with free APIs.

**No installs. No paid tools. No credit cards.**

---

## Open the Workshop Notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/ieee-workshop/blob/main/workshop.ipynb)

> Replace `YOUR_USERNAME` with your GitHub username after pushing this repo.

---

## Pre-Workshop Checklist (Share With Students)

Students need **3 things** before the session starts:

| # | What | How |
|---|------|-----|
| 1 | A **Google account** | Any Gmail works |
| 2 | A **laptop with a browser** | Chrome recommended |
| 3 | A **free Gemini API key** | Go to [aistudio.google.com](https://aistudio.google.com) → "Get API Key" → "Create API key in new project" → Copy it |

That's it. Everything runs in the browser.

---

## What Students Will Learn

| Level | Concept | What They Build |
|-------|---------|-----------------|
| **Level 1** | Structured Output | Prompt that returns JSON (score, roast, rewrite) instead of prose |
| **Level 2** | Tool Use | Python function that gives the agent recruiter context per role |
| **Level 3** | Self-Correction | Reflection loop — agent critiques and rewrites its own output |
| **Bonus** | Deployment | Gradio web app with a shareable public URL |
| **Bonus** | ATS Scoring | Gamified ATS compatibility score (before vs after) |
| **Bonus** | LinkedIn Post | Auto-generated LinkedIn post about what they built |

---

## Tech Stack

| Component | Tool | Cost |
|-----------|------|------|
| IDE | [Google Colab](https://colab.research.google.com) | Free |
| LLM | [Gemini 1.5 Flash](https://aistudio.google.com) (Google AI Studio) | Free tier — no credit card |
| Web App | [Gradio](https://gradio.app) | Free (runs in Colab) |
| Code Distribution | This GitHub repo + "Open in Colab" badge | Free |

---

## Repo Structure

```
ieee-workshop/
├── README.md              ← You are here
├── slides.html            ← Reveal.js slide deck (open in browser)
├── demo.ipynb             ← Live demo notebook (presenter only)
├── workshop.ipynb         ← Student notebook (has TODO cells)
└── solutions.ipynb        ← Completed solutions (all TODOs filled in)
```

---

## Running the Slides

Open `slides.html` in any browser. Arrow keys to navigate. Press `F` for fullscreen. Press `S` for speaker notes.

---

## Workshop Duration

**1 hour** — designed for 1st–3rd year engineering students with basic Python familiarity.

---

## Presenter

**Ishan** — AI Engineer | GDG Cloud New Delhi Speaker | Agentic AI & RAG Specialist

---

## License

MIT — use, remix, and teach freely.
