# 🪐 Orbit 10 — Canvas

**Every task, note and page is a document now.** Orbit 10 puts a Notion-grade writing surface at the centre of the app and keeps the Liquid Glass skin that makes it feel like it belongs on an iPhone. One HTML file, no build step, no dependencies, no backend.

---

## What's new in 10 · Canvas

### The document surface
Click a task, a note or a page and it opens **full screen** — a soft gradient cover, a big emoji icon you can change, a 40px title you type straight into, a Notion-style property table, and then an enormous canvas to write on. Shift-click instead and the same document slides in as a **resizable side peek** so you never lose your list. On a phone that peek becomes a bottom sheet you can flick away.

- `‹ Back` returns you exactly where you were
- `⋯` holds duplicate, copy, download, cover, icon, full-width and delete
- Properties are one click each: status, space, due, priority, stage, repeat
- Sub-tasks live under the properties with their own checkboxes
- A footer shows word count, reading time and related items

### The block editor
Everything you write is made of blocks, and it behaves the way you expect.

| Type this | Get this |
|---|---|
| `# ` `## ` `### ` | Headings |
| `- ` or `* ` | Bulleted list |
| `1. ` | Numbered list (renumbers itself) |
| `[] ` | A to-do you can tick |
| `> ` | Quote |
| `:: ` | Callout |
| ` ``` ` | Code block |
| `---` | Divider |
| `/` | The block menu — every type plus five templates |

Inline, `**bold**`, `*italic*`, `` `code` ``, `~~strike~~`, `==highlight==` and links render **live as you type**, with the caret pinned to exactly where you left it. Select any text for a floating toolbar — bold, italic, strike, code, highlight, link, and 🎯 which turns the selection into a real Orbit task.

Every block has a hover gutter: `＋` adds one below, `⠿` drags it anywhere or opens a menu (duplicate, move, turn into…, turn into a task, delete). Enter splits at the caret, Enter on an empty list item leaves the list, Backspace un-formats before it deletes, Tab promotes a line to a bullet then a to-do, Shift+Enter makes a soft break, and pasting several lines explodes them into proper blocks — headings, lists and checkboxes included.

It all still saves as **plain markdown-ish text**, so sync, export and backup are unchanged.

### Multi-select and bulk actions
⌘/Ctrl-click tasks to build a selection, Shift-click to extend a range, ⌘/Ctrl+A to take the lot. A floating bar appears with Complete, When (today / tomorrow / weekend / next week / clear), Priority, Move to space and Delete — all undoable from the toast. `⌫` deletes the selection, `Esc` clears it.

### Inline editing
Double-click a task title, a card title, a page name or a space name and rename it right there. Enter saves, Escape cancels. Nothing opens, nothing navigates.



### The bigger picture — All tasks
Press **G** (or ☰ All tasks in the sidebar) for every task you own on one page.

- **Group by** When · Space · Priority · Flat
- **Show** To do · Everything · Done
- **Space chips** filter to one area in a tap, each with a live count
- **▥ Dense** collapses every task to a single line — title, space, due and priority in one row — so you can scan dozens at a glance
- **Width** cycles narrow → wide → full, and it sticks

Multi-select, bulk actions, swipes and drag all work here exactly as they do everywhere else.

### New task is a document
`＋ New task` and **N** no longer open a cramped sheet. You get the full page — big title, properties, and the whole block editor — so you can write as much as you want while creating it. The title still understands plain words: type *"Study CCNA weekdays !med"* and Orbit lifts the repeat and the priority out for you. Walk away without typing anything and the empty draft quietly deletes itself.

Quick-add is still there for speed: the ＋ bar at the top of Today, All tasks and every space adds in one line without leaving the page.

### Done sinks, open floats
One rule everywhere: **anything you finish drops below the things you haven't.**

- Task lists keep open work on top and park completed items in their own group at the bottom
- Board columns push ticked cards under the live ones
- Today grows a quiet **Done today** shelf at the very bottom — crossed out, collapsed, with a one-tap *Clear* (undoable)
- Sub-tasks inside a task slide under a hairline "done" divider, with a progress meter and *Clear done*
- Your writing is never reordered behind your back — inside a page, ticked to-dos stay exactly where you typed them, and `⋯ → Tidy ticked items` moves them down only when you ask

Turn the whole behaviour off in **Settings → Features → Completed sinks to the bottom**.

### A quiet start
Orbit opens straight into your work. No welcome sheet, no daily briefing card, no mascot chatter, no update toast. Orbie only speaks when you tap it, and the briefing is still there if you ever want it — Settings → Features → Daily briefing.

### The new chrome
- **Sidebar** — quick row (search, today, week, habits, new task), collapsible Notes / Spaces / Apps sections with hover `＋` and `⋯` menus, and a drag handle on its right edge to resize it (remembered per device)
- **Breadcrumbs** — the topbar tells you where you are and takes you back up
- **Notes & pages home** — one gallery of everything you've written, filterable by pages or notes, switchable between gallery cards and a dense table
- **Space notes** — the same gallery, scoped to one space

---

## Everything else Orbit does

- **Spaces** — sidebar sections for Job Applications, Work, Reminders, Household, Personal (add your own, with custom emoji, color and pipeline stages)
- **Three views per space** — ☑ Tasks (grouped by Overdue / Today / Upcoming), ▦ Board (drag cards between stages), 🗒 Notes
- **Today dashboard** — a bento grid: stats, a focus ring against a daily goal, a 7-day glance, habit chips and your pinned notes
- **Smart quick-add** — `Call recruiter tomorrow !high` parses the date and priority (`today`, `tomorrow`, `next week`, `!high !med !low`, `daily`, `weekdays`, `weekly`)
- **Focus timer** — a 25-minute session with a floating progress ring that survives reloads and feeds a "Focus today" stat
- **Week planner** — a 7-day board plus a "No date" parking column; drag to schedule, drag back to unschedule
- **Habits with streak freeze** — daily check-in dots, per-habit streaks that survive one missed day
- **Voice capture 🎤** — tap the mic on quick-add and speak; Orbit types it live and parses the date and priority
- **Orbie** — press `O` for a chat panel that creates, completes, reschedules and recommends, in plain words
- **☀️ Daily briefing** — off by default; switch it on for a once-a-day card with your plan and one-tap starts
- **✨ Your Galaxy** — every finished task becomes a star on a golden-angle spiral; click one to remember what it was
- **Work page** — clock in/out, weekly hours, a standup generator built from your real tasks, meeting notes and an end-of-day wrap-up
- **Apps hub** — embed any website as an app in the sidebar, pin one beside Orbit on wide screens
- **Integrations** — Google Calendar, Outlook, Apple `.ics`, email or copy your day as Markdown, paste a list to bulk-add
- **Installable PWA** — offline service worker, home-screen icons, app shortcuts and a share target
- **Deep links** — `?add=Buy milk tomorrow`, `?view=week|habits|pad`, `?quick=1`, `?focus=1`
- **Five interface styles** — 💎 Liquid Glass, 🍃 Zen, 📐 Pro, ⚡ Pop, 📜 Journal — mixed with any accent, theme and glass level
- **A full sound design** — every action has its own synthesized tone, all offline, one switch turns it off
- **Settings hub** — appearance, features, dashboard tiles, behavior, data and privacy, all toggleable

---

## Keyboard

| Key | Does |
|---|---|
| `⌘/Ctrl K` | Command palette and universal search |
| `N` / `E` | New task / new page |
| `T` `G` `W` `H` `P` | Today · All tasks · Week · Habits · Notes |
| `⌘/Ctrl \` | Show or hide the sidebar |
| `⇧ click` | Open a task or note in the side panel |
| `⌘/Ctrl click` | Add a task to the selection |
| `⌫` | Delete the selection |
| Double-click | Rename a title in place |
| `/` | Block menu, inside the editor |
| `⌘/Ctrl B · I · E · U` | Bold · italic · code · highlight |
| `Tab` | Paragraph → bullet → to-do |
| `⇧ ↵` | Soft line break |
| `F` `M` `O` `A` `L` | Focus · mute · Orbie · Launchpad · lock |
| `?` | The full cheat sheet |
| `Esc` | Close the top-most thing |

---

## Files

`index.html` (the whole app) · `manifest.json` + `sw.js` + icons (installable PWA with offline support and share target) · `vercel.json` (clean URLs, no-cache for the service worker).

## Run it

**Just open it:** double-click `index.html`.

**Local server:**
```bash
npm i -g vercel
cd orbit-todo
vercel dev        # http://localhost:3000
```

**Deploy free:**
```bash
vercel --prod
```
Or drag the folder onto https://vercel.com/new.

## Your data

Data lives in the browser, tied to the URL you use. Sign in from the sidebar (free, powered by Puter) and everything — tasks, notes, pages, focus stats, preferences, pane widths — syncs to your own private cloud storage and follows you across devices, merging without duplicates. Export regularly for offline backups.

Orbit ships locked with the default PIN **110523**. Change it in Settings → Privacy.

## Customizing

Start with ⚙ Settings for accent, glass, style and theme — no code needed. Under the hood everything lives in one `index.html`: colors are CSS variables in `:root` at the top, app logic is the single `<script>` at the bottom. The document layer is clearly sectioned — the block editor engine, the document surface, the chrome, and the finishing touches — so it's easy to find what you want to change.
