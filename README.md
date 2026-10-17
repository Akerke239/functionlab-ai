# FunctionLab 3.2 — AI Differentiated Math Learning

Static website with a Vercel serverless Groq AI tutor.

## Deploy
Upload **the files and api folder**, not the ZIP, into the root of your GitHub repository. Import the repository to Vercel with framework **Other**. Configure Vercel Environment Variables:

- `GROQ_API_KEY` — your secret Groq API key (never commit it).
- `GROQ_MODEL` — `openai/gpt-oss-120b` (the model you confirmed works in your Groq account).

Redeploy after environment variable changes. The HTML loads KaTeX, marked and DOMPurify from a CDN; internet is needed for their rich formatting.

## New in 3.2
- Safe Markdown and KaTeX rendering for AI tutor output (sanitized HTML)
- Task-specific instructions, and hiding the formula and family for identify-the-function exercises until submission
- Show correct answer after an incorrect attempt, including a green interval overlay when a single interval is expected
- Zoom in, zoom out and reset graph scale
- Optional recommendation to try the next level after a streak of three correct answers
- Existing EN/RU, progress, function families, custom graphs and Groq backend preserved

## Important limitations
The interval and domain/range checkers approximate answers within the visible x-window [-4,4], not the full real-number domain. Some functions have disconnected or open intervals; endpoints are approximated numerically. The `Show correct answer` overlay highlights one interval when applicable. The app is a learning prototype and should be tested across families before assessment.
