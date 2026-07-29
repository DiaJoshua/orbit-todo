# 🪐 Orbit — Tasks & Notes

A personal command center for everything: job applications, work, reminders, household chores, notes and more. Single-file, no build step, no dependencies.

## Features

- **Spaces** — sidebar sections for Job Applications, Work, Reminders, Household, Personal (add/edit/delete your own, with custom emoji, color and pipeline stages)
- **Three views per space** — ☑ Tasks (grouped by Overdue / Today / Upcoming), ▦ Board (drag cards between pipeline stages, e.g. Applied → Interview → Offer), 🗒 Notes (sticky notes with colors + pinning)
- **Today dashboard** — greeting, stats, everything due across all spaces
- **Smart quick-add** — type `Call recruiter tomorrow !high` and Orbit parses the date and priority (`today`, `tomorrow`, `next week`, `!high !med !low`)
- **Extras** — search (`/`), keyboard `n` for new task, confetti on completing tasks, undo for deletes, JSON export/import backups

## Run it

**Option A — just open it:** double-click `index.html`. That's it.

**Option B — local server via Vercel CLI:**
```bash
npm i -g vercel
cd orbit-todo
vercel dev        # serves at http://localhost:3000
```

**Option C — deploy to Vercel (free):**
```bash
cd orbit-todo
vercel            # log in, accept defaults → get a live URL
vercel --prod     # production deploy
```
Or drag the `orbit-todo` folder onto https://vercel.com/new.

## Your data

Data is stored in the browser's `localStorage`, tied to the URL you use. If you switch between `file://`, `localhost` and a deployed URL, each keeps its own copy — use **Export** (sidebar) on one and **Import** on the other to move data. Export regularly to back up.

## Customizing

Everything lives in one `index.html` — colors are CSS variables in `:root` at the top, app logic is the single `<script>` at the bottom.
