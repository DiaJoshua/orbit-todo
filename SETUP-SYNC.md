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
- **Cloud-only mode.** Orbit does not save notes, tasks, preferences, or other Orbit data in browser storage. You must be signed in and online for changes to save; closing or refreshing before a confirmed cloud save can lose the latest change
- **Other devices update within about 20 seconds**, or instantly the moment you switch to their tab
- **Nothing gets lost when you first sign in.** If a device already has tasks and notes on it, they are merged with what is in the cloud, not overwritten
- Cloud-only mode needs an internet connection. If you are offline, you can view the current page but new changes are not saved

## Sign in on your desktop first

If you are upgrading from an earlier version that kept a local copy, sign in on the device that has the latest data first. Orbit uploads it to Puter and removes the old local Orbit data after confirmation.

## Troubleshooting

- **Button says "Sync unavailable":** the sync service could not be reached. Check your internet and reload the page
- **Popup closed by accident:** just click the sync button again
- **Something looks out of date on another device:** switch to that tab or reload, it pulls the latest copy on focus
- **Want off?** Click the green sync button and confirm sign out. Your cloud data remains in Puter, but new changes will not be saved until you sign in again

## Privacy note

Your data is stored in your own private Puter storage that only your account can access. As always: keep passwords out of notes, use a password manager for those.
