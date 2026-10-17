# FunctionLab 3.3 — AI Tutor feedback update

Updated AI Tutor with four independent modes: **Hint**, **Explain**, **Feedback after Check Answer**, and **Ask AI**.

- Feedback receives the actual selected interval or entered answer and the checked outcome.
- Ask AI only answers the student's typed question.
- Basic explanations avoid calculus; Standard and Advanced scale up appropriately.
- Short responses, Markdown/KaTeX math formatting, scrollable response panel.
- Existing graphs, progress counter, EN/RU and design retained.

## Deploy
Upload the contents (not the ZIP) to your existing GitHub repository, preserving `api/chat.js` in the `api` directory. Vercel redeploys on commit. Keep `GROQ_API_KEY` secret and `GROQ_MODEL=openai/gpt-oss-120b` in Vercel Environment Variables.

## Testing
Test a wrong interval → Check Answer → AI feedback; Hint; Explain; and a separate typed question → Ask AI. Groq requires a live deployment and active credentials.
