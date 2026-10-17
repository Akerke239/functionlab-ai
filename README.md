# FunctionLab 3.0

Interactive EN/RU math practice with random linear, quadratic, absolute value, root, exponential, cubic, rational, logarithmic, trigonometric and piecewise functions (availability depends on difficulty), mixed practice, score tracking, custom graph input, and Groq AI tutoring.

## Deploy
1. Upload **contents** of this folder to the root of your GitHub repository, including `api/chat.js`.
2. Import GitHub repository in Vercel, Framework Preset **Other**, Root Directory `./`.
3. In Vercel Project Settings → Environment Variables add `GROQ_API_KEY` with your private Groq API key. Optional `GROQ_MODEL` (default `llama-3.3-70b-versatile`). Redeploy.
4. Open the Vercel URL and try **Hint** or **Ask AI**.

## Notes
- Scores are saved locally in the current browser, not shared across devices.
- Domain/range tasks refer to the shown x-window `[-4,4]`, not necessarily the function's full natural domain/range. Range practice is disabled for rational and logarithmic generated functions because their asymptotes complicate finite-window numerical checking.
- Increasing/decreasing selections should span nearly an entire monotonic section. When multiple monotonic sections exist, any one complete section is accepted.
- Custom formula input supports arithmetic, `^`, `sin`, `cos`, `tan`, `sqrt`, `abs`, `log`, `ln`, `exp`, `pi`, with explicit `*` multiplication. This is a math expression evaluator, not a full symbolic algebra system.
- The API key is read server-side; never put it in HTML, commit it to GitHub, or send it to chat.
