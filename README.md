# Health Tracker (Afrah & Safwan)

A static dashboard for tracking daily **diet** (1 = good, 0 = not) and **exercise** (1 = done, 0 = not) for two people. Data lives as JSON in this repo, so you both share the same numbers. Works offline too (cached in your browser).

## One-time setup

1. **Create a repo** (e.g. `health-tracker`) and put these files in it:
   - `Health Tracker.dc.html`
   - `support.js`
   - `data.json`  (starts as `{ "entries": {} }`)
2. **Turn on GitHub Pages**: repo → Settings → Pages → Deploy from branch → `main` / root.
   Your app will be at `https://<your-username>.github.io/health-tracker/Health%20Tracker.dc.html`
3. **Make an access token** (each of you, or share one):
   - GitHub → Settings → Developer settings → **Fine-grained tokens** → Generate new token
   - Repository access: only this repo
   - Permissions → **Contents: Read and write**
   - Copy the `github_pat_...` string
4. Open the app → **Connect GitHub** → fill in owner, repo, branch (`main`), path (`data.json`), and your token → **Connect & sync**.

That's it. Every toggle saves back to `data.json` in the repo. Hit **Sync** to pull the latest from the other person.

## How it works
- Tap the big **Today** buttons or any cell in the grid to flip between 1 and 0.
- **Healthy %** = share of logged days with diet = 1. **Active %** = same for exercise.
- Streaks count consecutive days (up to today) at 1.
- The token is stored only in your browser (localStorage), never committed.

## Notes
- Last write wins. If you both edit the same second, one Sync fixes it.
- No token = local-only mode (saves in your browser but doesn't share).
- Date range is set in the code (`START` / `END`) — currently Jul 6 – Oct 10, 2026.
