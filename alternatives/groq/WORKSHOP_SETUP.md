# Groq Workshop Setup Checklist

## Student Setup (Colab)

1. Open the workshop notebook in Colab.
2. Add `GROQ_API_KEY` in Colab Secrets.
3. Run the Setup cell.
4. Confirm setup success output and selected model.

## Local Setup (Optional)

```bash
cp .env.example .env
```

Then set:

- `GROQ_API_KEY=your_key_here`
- `GROQ_MODEL=llama-3.3-70b-versatile` (or another supported model)

## Quick Troubleshooting

- `429` / quota: switch model in setup from `GROQ_MODELS` and retry.
- Missing key error: confirm `GROQ_API_KEY` exists in Secrets or `.env`.
- `roast_my_resume is not defined`: run Helpers before Gradio.
