# FunctionLab 2.0

Interactive EN/RU math practice with Basic, Standard, Advanced and custom graph exploration.

## Deploy
1. Upload the **contents** of this folder (not the ZIP) to the root of a GitHub repository. Keep `api/chat.js` inside `api`.
2. Import repository into Vercel. Framework preset: Other. Root: `./`.
3. Set environment variable `GROQ_API_KEY` in Vercel. Optional `GROQ_MODEL` defaults to `llama-3.3-70b-versatile`.
4. Deploy or redeploy. Never commit API keys.

## Features
- Pointer-drag interval selection, success/error colors, multiple preset functions per level
- Domain/range on the **displayed window** [-4,4], point evaluation, no-interval option
- Custom formula input supports x, + - * / ^, parentheses, sin, cos, tan, sqrt, abs, log, exp, pi
- AI requests use Vercel `/api/chat` and Groq. Groq model errors show actionable messages.

## Important notes
Graph checks use numerical approximations. Range questions refer to the plotted x-window, not necessarily the natural domain. For custom graph mode, plotting is client-side; Groq is used only for tutoring. Verify the model selected in your Groq account if the API reports 404.
