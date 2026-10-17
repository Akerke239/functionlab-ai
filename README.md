# FunctionLab — Interactive AI Math Tutor

A bilingual (English/Russian) educational website for differentiated learning of functions. Students can drag to select intervals of increase/decrease, work with domains/ranges, calculate function values, and request Groq AI guidance.

## Deploy using GitHub + Vercel

1. Create a **new public GitHub repository** and upload `index.html`, `api/chat.js`, `package.json` and `README.md` (keep the `api` folder structure).
2. On [Vercel](https://vercel.com/new), import that repository. Choose **Other** as the framework preset, leave build command empty, and use the repository root as the root directory.
3. In Vercel → Project → Settings → Environment Variables add **GROQ_API_KEY** and paste your Groq key as its value. Never paste the key into GitHub or HTML. Optionally add `GROQ_MODEL` (default: `llama-3.3-70b-versatile`).
4. Redeploy after setting the variable. Open your `*.vercel.app` site and test the Hint, Explain and Check buttons.

The graph and local answer checking run without an API key. AI explanations require the deployed `/api/chat` endpoint and a valid Groq key. Opening `index.html` directly from disk will not activate AI.

## Differentiation

- Basic: linear function, foundational questions.
- Standard: quadratic function, turning points.
- Advanced: cubic function, multiple monotonicity intervals.

The AI receives the chosen level, task, current answer and checking outcome. AI output is guidance; deterministic local checking decides correctness.

## Security and limits

`GROQ_API_KEY` is read only on the server. This sample does not implement per-user authentication or rate limiting; for public/high-traffic use add rate limiting and abuse prevention. Never commit `.env` files.
