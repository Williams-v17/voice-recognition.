# Voice Authentication System — GitHub Pages edition

Static version of the project. No Python server needed: the "backend" runs
inside the browser (`js/demo-backend.js`), so it works on GitHub Pages.

## Deploy
1. Create a new GitHub repo and upload everything in this folder (index.html must be at the repo root).
2. Repo → Settings → Pages → Source: "Deploy from a branch" → Branch: `main`, folder `/ (root)` → Save.
3. Wait ~1 minute, open `https://<your-username>.github.io/<repo-name>/`.

## What works
- Sign up / log in (stored in your browser's localStorage)
- Record 5+ voice samples, build a voiceprint, verify a voice against it
- All pages, animations and visualisations

## Limits (demo mode)
- Voice matching uses an in-browser MFCC fingerprint, not the SpeechBrain ECAPA model. Good for demos, not real security.
- Accounts live only in that browser. Clearing site data wipes them.
- The download button gives a voiceprint JSON, not a real `.whl` package.
- For the real thing (ECAPA model + .whl builds) deploy the original Docker project on Render/Railway/Hugging Face Spaces.
- Microphone needs HTTPS, which GitHub Pages provides.
