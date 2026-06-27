# HC Quiz Game

Live multiplayer quiz game. Static HTML/JS + Firebase Realtime Database. No build step.

## Pages
- `index.html` — landing page + Hall of Fame
- `editor.html` — build/edit quizzes (saved to this browser's localStorage)
- `host.html` — run the live game 
- `screen.html` — big shared screen (projector/TV)
- `player.html` — phone client for players

## Deploy to GitHub Pages
1. Create a new GitHub repo and push these files to the root.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / root → Save.
3. Wait ~1 min. Site goes live at `https://<your-username>.github.io/<repo-name>/`.
4. Host opens `.../host.html`, players scan the QR (auto-points to the right URL).

## Important
- **Quizzes live in localStorage, which is per-domain.** Quizzes made on the Netlify site will NOT appear here. Move them with **Export JSON** (Netlify editor) → **Import JSON** (this editor).
- Edit and host on the **same device/browser** — the host reads quizzes from that browser's localStorage.
- After editing a quiz, **re-select it** in the host dropdown to load the update.
- Firebase, QR codes, and fast-image delivery work automatically — no config changes needed between Netlify and GitHub Pages.
