# 🪐 Orbit — Tasks & Notes

A personal command center for everything: job applications, work, reminders, household chores, notes and more. Single-file, no build step, no dependencies.

## Features

- **Spaces** — sidebar sections for Job Applications, Work, Reminders, Household, Personal (add/edit/delete your own, with custom emoji, color and pipeline stages)
- **Three views per space** — ☑ Tasks (grouped by Overdue / Today / Upcoming), ▦ Board (drag cards between pipeline stages, e.g. Applied → Interview → Offer), 🗒 Notes (sticky notes with colors + pinning)
- **Today dashboard** — greeting, stats, everything due across all spaces
- **Smart quick-add** — type `Call recruiter tomorrow !high` and Orbit parses the date and priority (`today`, `tomorrow`, `next week`, `!high !med !low`)
- **Focus timer** — 🎯 in a task's right-click menu (or ⌘K → "Focus for 25 minutes") starts a 25-minute session. A floating pill shows a live progress ring, survives reloads, and finished minutes land in a "Focus today" dashboard stat that syncs to all your devices.
- **Synced preferences** — your theme and mascot choice are part of your cloud data, so they follow you to every signed-in device.
- **Redesigned editors** — task and space sheets use iOS-style grouped sections on frosted glass: tap chips to pick space, stage and repeat; quick dates include Weekend and Clear; checklists count themselves and Enter adds the next item; ⌘/Ctrl+Enter saves
- **Space customization** — live sidebar preview while you edit, emoji picker grid, 12 color presets plus a full color wheel, per-stage colors that show on Board columns, drag ≡ to reorder stages, and one-tap templates (Job hunt, Project, Fitness, Study, Travel)
- **Appearance panel** — 🎨 Style in the sidebar (or ⌘K): app-wide accent color (presets + custom wheel), frosted glass on/off, theme and mascot — all synced to your devices
- **Extras** — search (`/`), keyboard `n` for new task, confetti on completing tasks, undo for deletes, JSON export/import backups

## Design: how the dark/light switch animates

1. You tap the 🌙/☀️ toggle. The current screen is snapshotted with the **View Transitions API** and held perfectly still.
2. Underneath, the theme flips in a single frame — every color lives in CSS variables, so there are no per-element transitions to compute.
3. The new theme is revealed through a **circle that grows out of the toggle button**: a `clip-path: circle()` animation on `::view-transition-new(root)`, 550 ms, `cubic-bezier(.25,.75,.2,1)` — fast start, gentle landing.
4. Fallbacks: browsers without view transitions get a soft 450 ms crossfade; `prefers-reduced-motion` users get an instant switch, no animation.
5. The choice is saved to your synced preferences, so your other devices adopt it (via a gentle crossfade) on their next sync.

## Why it feels instant

- Renders coalesce into one animation frame; entrance animations play only when the view actually changes, never on re-renders — nothing flickers or replays.
- Scroll position is preserved across re-renders, and group collapse/expand animates in place without touching the rest of the page.
- Modals, popovers and the toast all have matched enter/exit animations; new tasks pop in, checked tasks pop their checkmark, moved cards settle.
- Cloud pushes debounce at 300 ms and flush instantly when the tab hides or closes, pulls happen on focus and every 20 s — your last keystroke is never lost.

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

Data is stored in the browser's `localStorage`, tied to the URL you use. Sign in from the sidebar (free, powered by Puter) and everything — tasks, notes, pages, focus stats, preferences — syncs to your own private cloud storage and follows you across devices, merging without duplicates. Export regularly for offline backups.

## Customizing

Start with the 🎨 Style panel for accent, glass and theme — no code needed. Under the hood everything lives in one `index.html`: colors are CSS variables in `:root` at the top, app logic is the single `<script>` at the bottom. Glass surfaces use `backdrop-filter` behind an `@supports` guard, so older browsers simply get solid panels.
