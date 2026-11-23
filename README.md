# Future Tense Quest — ESL Grammar Game

A lightweight, responsive browser game for Grade 7 / A2 learners practising **will** vs **be going to**.

## Files
- `index.html` — the game application (HTML, CSS and JavaScript)
- `lessons.json` — master lesson list (add future units here)
- `will-going-to.json` — all content for this lesson: cheat-sheet, warm-up and main questions

## Run locally
The app loads JSON using `fetch()`, so it must be served over HTTP rather than opened by double-clicking `index.html`.

If Python 3 is installed, open a terminal in this folder and run:

    python -m http.server 8000

Then open:

    http://localhost:8000

## Publish as one URL (no student login)
Upload the **contents** of this folder to any static hosting service, such as GitHub Pages, Netlify or Cloudflare Pages. The host will provide one URL. Students open that URL in Chrome, Safari or Edge; no account, installation or student data collection is required.

Keep `index.html`, `lessons.json`, and `will-going-to.json` together in the same published folder.

## Add another grammar unit
1. Create another JSON file using the same structure as `will-going-to.json` (`id`, `title`, `cheatsheet`, `warmup`, `questions`).
2. Add a lesson entry to `lessons.json` with a unique `id`, display `title`, `subtitle`, `level`, `grade`, and the JSON filename in `file`.
3. Set `available` to `true`.

The main game currently takes 15 randomized questions from the selected lesson's `questions` array. The warm-up is untimed. The main challenge has a 15-second per-question timer and an untimed-practice checkbox.

## Classroom/privacy notes
- No student accounts, emails, analytics, database, or network calls beyond loading the two lesson JSON files.
- Scores and answers are held in memory only and are not uploaded or saved.
- Sound can be muted using the top-right toggle. Audio is generated locally by the browser.
- A student can screenshot the end screen to share results.
