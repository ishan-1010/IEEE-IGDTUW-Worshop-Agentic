# Post-Workshop Challenges

Use these challenges to level up after the workshop. They build on **structured output**, **tool use**, and **self-correction**. Work in your copy of `workshop.ipynb` or `solutions.ipynb` (Colab or local).

---

## How to use

- Pick one challenge and implement it in your notebook.
- Run the relevant cells (Setup, Helpers, then your new code).
- Check `solutions.ipynb` for reference patterns (e.g. `get_role_requirements`, `roast_my_resume`, ATS section).

---

## Challenge 1: Add ATS score to the pipeline (Easy)

**Goal:** After Level 3, call the LLM once more to get an **ATS compatibility score** (1–10) and 2–3 tips for the final bullet.

**What you’ll practice:** Structured output, chaining steps.

**Steps:**

1. Reuse the ATS prompt pattern from the **Bonus: ATS Score** section in `solutions.ipynb`.
2. Pass your Level 3 `final_version` and the target role into the ATS prompt.
3. Ask for JSON: `score`, `verdict` (one sentence), `tips` (list of 2–3 strings).
4. Print the score and tips after the pipeline (or return them from a `roast_my_resume_plus_ats()` function).

**Stretch:** Add the ATS score and tips to the Gradio app output.

---

## Challenge 2: Add a new tool (Medium)

**Goal:** Create a second tool, e.g. `get_industry_keywords(industry)`, that returns a short list of buzzwords for that industry. Use it in your Level 2 prompt so the rewrite uses both **role** and **industry** context.

**What you’ll practice:** Tool use, prompt design.

**Steps:**

1. Define `get_industry_keywords(industry: str) -> str` that returns a string of 5–8 keywords (you can hardcode a small dict for "Tech", "Finance", "Healthcare", "Marketing" or call the LLM once to generate them).
2. In Level 2, call both `get_role_requirements(role)` and `get_industry_keywords(industry)`.
3. Put both contexts into the prompt so the rewrite is tailored to role + industry.
4. Update Gradio to accept an "Industry" dropdown and pass it through.

**Stretch:** Let the LLM decide when to call the industry tool (e.g. only when industry is not "General").

---

## Challenge 3: Batch mode — three bullets at once (Medium)

**Goal:** Run the full pipeline (Level 1 → 2 → 3) on **three** resume bullets and output a short summary: which bullet improved the most, and the three final versions.

**What you’ll practice:** Loops, structured output, aggregating results.

**Steps:**

1. Write a function `roast_batch(bullets: list[str], role: str) -> dict` that loops over each bullet, runs the same pipeline as `roast_my_resume`, and collects results.
2. After all three are done, call the LLM once with the three before/after pairs and ask: "Which bullet improved the most and why? Return JSON: `best_index` (0/1/2), `reason` (one sentence), `summary` (one sentence for each bullet)."
3. Print the summary and the three final versions.

**Stretch:** Add a "Batch" tab in Gradio: text area with one bullet per line, run batch, show summary + table of results.

---

## Challenge 4: Two reflection rounds (Medium)

**Goal:** Run the Level 3 self-critique **twice**: first pass produces a rewrite, second pass critiques that rewrite and produces a final version. Compare confidence scores from both passes.

**What you’ll practice:** Self-correction, multi-step reasoning.

**Steps:**

1. After Level 2, run Level 3 as usual → get `version_1` and `confidence_1`.
2. Run Level 3 again on `version_1` with the same prompt (find 3 problems, fix, output `final_version` and `confidence_score`) → get `version_2` and `confidence_2`.
3. Print both versions and both confidence scores. Optionally ask the LLM: "Which version is stronger and why?" (one sentence).

**Stretch:** Stop after one round if `confidence_score` is already ≥ 8 to save API calls.

---

## Challenge 5: LinkedIn one-liner (Easy)

**Goal:** From the final bullet, generate a **LinkedIn post one-liner** (e.g. a humble brag or a tip that uses the same achievement). Add it to your pipeline or Gradio.

**What you’ll practice:** Structured output, prompt design.

**Steps:**

1. After Level 3 (or after ATS), call the LLM with the final bullet and ask for JSON: `linkedin_one_liner` (one sentence, first person, suitable for a LinkedIn post).
2. Print it or show it in the Gradio UI.
3. Reuse the style from the **Bonus: LinkedIn** section in `solutions.ipynb` if you like.

**Stretch:** Add a "Tone" option (Professional / Casual / Humorous) and pass it into the prompt.

---

## Challenge 6: Gradio upgrade (Easy–Medium)

**Goal:** Improve the Gradio app: add a **role dropdown** (prefill 4–5 roles), show **before vs after** side by side, and add a **"Copy final bullet"** button.

**What you’ll practice:** Gradio components, layout, UX.

**Steps:**

1. Use `gr.Dropdown(choices=["Software Engineer", "Data Scientist", "Product Manager", "ML Engineer", "Other"])` for role.
2. Use two `gr.Textbox` components (read-only) for original and final bullet so they appear side by side.
3. Add a "Copy to clipboard" button that copies the final bullet (you can use `gr.Button` plus a small JS or `gr.Textbox(interactive=False)` and tell the user to select and copy; or search for Gradio copy-button patterns).

**Stretch:** Add a "Download report" button that generates a short markdown or text summary and triggers a file download.

---

## Need help?

- **Reference:** Open `solutions.ipynb` for full implementations of the pipeline, tools, ATS, and Gradio.
- **Stuck?** Re-run the Setup and Helpers cells; ensure `call_llm`, `get_role_requirements`, and `roast_my_resume` are defined before your new code.
- **Share:** Tag [Ishan Katoch](https://www.linkedin.com/in/ishan-katoch/) on LinkedIn when you ship one of these.

Good luck — and keep building.
