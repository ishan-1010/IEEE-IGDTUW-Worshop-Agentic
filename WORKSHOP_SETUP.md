# Workshop Setup Checklist

Use this quick checklist before the session starts.

## Student Setup (Colab)

1. Open the workshop notebook in Colab.
2. Add API key in Colab Secrets:
   - Gemini track: `GEMINI_API_KEY`
   - Groq track: `GROQ_API_KEY`
3. Run the Setup cell.
4. Confirm the output shows setup success.

## Local Setup (Optional)

### Gemini track

```bash
cp .env.example .env
```

Then set `GEMINI_API_KEY` in `.env`.

### Groq track

```bash
cp alternatives/groq/.env.example alternatives/groq/.env
```

Then set `GROQ_API_KEY` in `alternatives/groq/.env`.

## Quick Troubleshooting

- `429` / quota: wait and retry, or verify you are using the default model in setup.
- `roast_my_resume is not defined`: run Helpers before Gradio.
- Missing key error: confirm secret/env var name matches exactly.
