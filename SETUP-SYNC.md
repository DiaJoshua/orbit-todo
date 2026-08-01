# ☁ Cloud sync: how it works (no setup needed)

Good news: there is nothing to configure. Sync is built into the app using Puter, a free cloud service that gives each user their own private storage. No API keys, no project setup, no config files.

## Turning it on

1. Open your Orbit site (your Vercel URL)
2. In the sidebar footer, click **☁ Sign in to sync devices**
3. A popup appears. Create a free account the first time (takes seconds) or sign in if you already have one
4. Done. The button turns green: **✓ Sync on**

Do the same on your phone, laptop, or any other browser. Same account = same data everywhere.

## What to expect

- **You sign in once per device.** The login is remembered, so next time you open Orbit it connects automatically
- **Every change saves to the cloud automatically**, about half a second after you make it
- **Other devices update within about 20 seconds**, or instantly the moment you switch to their tab
- **Nothing gets lost when you first sign in.** If a device already has tasks and notes on it, they are merged with what is in the cloud, not overwritten
- If you are offline, Orbit keeps working from the device copy and pushes your changes when you are back online (most recent change wins)

## Sign in on your desktop first

Your desktop browser holds the notes and tasks you have already been adding. Sign in there first so that copy becomes the cloud original, then sign in on your other devices to receive it. (Because of merging, the order is not critical, but this keeps things tidy.)

## Troubleshooting

- **Button says "Sync unavailable":** the sync service could not be reached. Check your internet and reload the page
- **Popup closed by accident:** just click the sync button again
- **Something looks out of date on another device:** switch to that tab or reload, it pulls the latest copy on focus
- **Want off?** Click the green sync button and confirm sign out. Your data stays on the device and in the cloud

## Privacy note

Your data is stored in your own private Puter storage that only your account can access. As always: keep passwords out of notes, use a password manager for those.
