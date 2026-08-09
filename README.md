# 🪐 Orbit: Tasks & Notes

A personal command center for everything: job applications, work, reminders, household chores, notes and more. Single file, no build step, no dependencies.

## Features

- **Light mode by default** plus a soft, easy on the eyes dark mode. Toggle with the 🌙/☀️ button, your choice is remembered
- **Repeating tasks**: set a task to repeat Daily, Weekdays or Weekly (like Clinic every day). Checking it off completes it for today and automatically rolls it to the next day
- **Cloud sync, zero setup**: click Sign in (sidebar), create a free account once, and your data saves automatically and follows you on every device. Login is remembered per device. Details in `SETUP-SYNC.md`
- **Notepad with pages, Notion style**: multiple pages you can create, rename and delete, each a full writing canvas. Type `/` on a new line (or hit ＋ Insert) for headings, checklists, dividers, date stamps and templates (meeting notes, daily plan, job application). Autosaves, syncs, and lists every sticky note below for easy reading
- **Workspace sidebar**: a clean personal header (your name's Orbit) with a gradient app tile, click it to rename. Reorder spaces by dragging them (desktop) or long pressing then sliding (mobile); the order syncs everywhere
- **Dashboard sticky notes**: pin any note and it shows right on the Today dashboard, add new ones straight from the dashboard
- **Spaces**: sidebar sections for Job Applications, Work, Reminders, Household, Personal (add your own with custom emoji, color and pipeline stages)
- **Three views per space**: ☑ Tasks (grouped by Overdue / Today / Upcoming), ▦ Board (drag cards between stages, like Applied → Interview → Offer), 🗒 Notes (sticky notes with colors and pinning)
- **Natural language quick add with live preview**: type `Follow up with recruiter fri !high`, `Pay rent aug 20`, `Standup weekdays`, `Review in 3 days` and watch Orbit show you exactly what it understood before you press Enter
- **Install it like a real app**: on your phone open the site, then Add to Home Screen (iOS Safari: Share button; Android Chrome: Install app). Opens full screen, works offline, and auto updates itself the next time you open it with internet after a new version is pushed
- **Orbie, your assistant 🪐**: a little planet in the corner whose eyes follow your cursor (or your taps on mobile). Click him and talk in plain language: `gym tomorrow !med in Personal` adds a task, `done clinic` checks one off, `note: idea` pins a note, `find resume` searches, `go to work` navigates, `clear overdue` triages, `help` lists everything. He celebrates completions and milestones, sleeps when you are away, and can be hidden from the Ctrl K palette
- **Task menus everywhere**: right click any task (or long press on mobile, or tap ⋯) for instant actions: mark done, edit, duplicate, due today/tomorrow/next week, delete
- **Natural language in every input**: quick add, the New Task form, and Orbie all understand dates, weekdays, priorities and repeats, with a live "understood as" preview. On the Notepad, highlight any line and hit ＋ Task from selection
- **Board quick move**: every card has a › button to hop to the next stage, perfect for phones where drag and drop is fiddly
- **Notepad export**: download your whole notepad as a .txt any time
- **Checklists inside tasks**: break any task into subtasks, progress shows as ☑ 2/5 on the card
- **One tap triage**: a Move all to today button on the Overdue group, and Duplicate on any task
- **Alive dashboard**: greeting with your name, live clock, daily quote, 🔥 streak counter, stats
- **Modern animations**: staggered card entrances, smooth theme crossfade, spring checkboxes, confetti on completing tasks (respects reduced motion settings)
- **Command palette**: press `Ctrl K` (or tap the Ctrl K chip) to jump to any space, open the board, create tasks or notes, switch theme, export, all from the keyboard
- **Quick due dates**: Today / Tomorrow / Next week buttons right inside the task editor
- **Refined minimalist design**: warm off white light theme, neutral charcoal dark theme, muted accents, Inter typeface, calmer animations
- **Collapsible sidebar**: the ☰ button hides or shows the sidebar with a smooth slide (remembered). On phones there is a big floating ☰ button at the bottom right, plus swipe from the left edge to open and swipe left to close
- **Extras**: search (`/`), keyboard `n` for new task, undo for deletes, JSON export and import backups

## Files in this project

Upload all of these to GitHub:

| File | What it is |
|---|---|
| `index.html` | The entire app |
| `vercel.json` | Vercel config |
| `README.md` | This file |
| `SETUP-SYNC.md` | How cloud sync works |
| `manifest.json` | Makes it installable as an app |
| `sw.js` | Offline support |
| `icon.svg` | App icon |

## Apple style integrations

- **Share sheet**: Share on any task menu or notepad page opens your device's native share sheet (AirDrop, Messages, anything)
- **Calendar**: tasks with a due date have Add to Calendar in their menu; it downloads an .ics that opens straight into Apple or Google Calendar
- **Siri and Shortcuts**: the app understands links like `https://YOUR-URL/?add=Buy milk tomorrow`. To add tasks by voice on iPhone: open **Shortcuts** → ＋ → add **Dictate Text** → add **URL** set to `https://YOUR-URL/?add=` followed by the Dictated Text variable → add **Open URLs** → name it "Add to Orbit". Now "Hey Siri, Add to Orbit" captures a task by voice
- **Daily reminders**: enable from the ⌘K / Ctrl K palette; once a day Orbit notifies you what is due
- **Native feel**: SF Pro typography on Apple devices, ⌘K hints on Mac, haptic ticks on Android, and a one time Add to Home Screen tip

## Run it

**Option A, just open it:** double click `index.html`. (Cloud sync sign in needs a real URL, see below.)

**Option B, local server with Vercel CLI:**
```bash
npm i -g vercel
cd orbit-todo
vercel dev
```

**Option C, deploy to Vercel (free):** push this folder to GitHub, import the repo at https://vercel.com/new, deploy. Every future push auto deploys.

## Sharing with friends

Orbit is friend ready: no personal data ships in the code. New visitors get a clean welcome that asks their name, sample content to explore, and their own private cloud account when they sign in. Everyone's data is completely separate.

**How sign in behaves:** on a device where you have not made changes, signing in simply loads your cloud data (no duplicated samples). If you did make changes on that device first, Orbit merges both sides and removes duplicates automatically.

**Everything is moveable:** drag tasks within their group, drag sticky notes, drag spaces in the sidebar. On phones, long press until it lifts, then slide. Your order syncs everywhere. Installed as an app, the icon even shows a badge with how many tasks are due.

## Your data

Without cloud sync, data lives in the browser's localStorage, tied to the URL you use. Use **Export** and **Import** in the sidebar to move or back up data. With cloud sync on (sidebar sign in, see `SETUP-SYNC.md`), data saves to your own private cloud storage automatically and follows your account everywhere. First sign in merges device and cloud data so nothing is lost.

**Never store passwords in notes.** This repo is public. Use a password manager.

## Customizing

Everything lives in one `index.html`. Light theme colors are in `:root`, dark theme colors in `html[data-theme="dark"]`, app logic is the single script at the bottom.
