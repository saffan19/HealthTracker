# Wedding Glow-Up Tracker (Afrah & Safwan)

A cute, baby-pink dashboard for staying consistent with **diet** and **exercise** on the way to the wedding on **October 22, 2026**. Data lives in a small free cloud database (JSONBin.io) you both share, so your numbers stay in sync. It also caches locally, so it works offline.

## Using it
- **No setup needed.** Already connected to a shared database — open it on any device and you both see and edit the same data.
- A live **countdown** shows how many days until "I do", with rotating pep-talks from a little cast of characters.
- In **Today's glow-up**, tap **Diet** if you ate well and **Move** if you exercised — it turns to **+**. Tap again for **–** if you didn't. **·** means not logged yet.
- Every **+** throws a happy floating-hearts party; every **–** gets a gentle, kind pep-talk.
- Missed a day? Scroll to it in **Our daily log** and tap it in later — any date is editable.
- **Healthy %** / **Active %** and 🔥 streaks track your consistency. Edits save automatically and refresh every 20 seconds; **Sync** pulls the latest now.
- **Export** downloads the raw JSON anytime.

## Hosting
It's a static site — put `Health Tracker.dc.html` and `support.js` in any static host (GitHub Pages, Netlify, Vercel) and open the URL. No server required.

## Changing the shared database
Click **Connect** to:
- **Create new shared database** — makes a fresh one and gives you a **Database ID** to send to the other person.
- **Join an existing one** — paste a Database ID someone shared with you.

## Notes
- Date range is set in code (`START` / `END`) — currently Jul 6 – Oct 22, 2026 (the wedding day).
- Last write wins; the 20-second refresh keeps both of you current.
- This is intentionally low-security (a shared key is embedded). Fine for a private two-person tracker — don't store anything sensitive.
