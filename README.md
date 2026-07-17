# Cashflow

A personal cash flow planner. Know your balance before it happens: projected cash after every paycheck and payment, credit cards, subscriptions, and CSV statement import with automatic recurring-charge detection.

Private by design: no accounts, no server, no sync. All data is stored on the device the app runs on. Every person who opens their own copy gets their own private data.

## What's in this folder

| File | Purpose |
|---|---|
| `index.html` | The entire app. Works on its own. |
| `manifest.webmanifest`, `sw.js`, `icon-*.png` | Only used when the app is hosted at a web address. They make it installable (home-screen / dock icon) and let it work offline. |

All files live at the top level on purpose — upload everything in one drag and it just works.

## Use it on your Mac (no hosting needed)

1. Keep this folder somewhere permanent (e.g. `Documents/Cashflow`).
2. Double-click `index.html`. It opens in your browser and autosaves to that browser on that Mac.
3. Optional, for an app-like feel: in Chrome, use the three-dot menu → Cast, Save and Share → Create Shortcut and check "Open as window". You get a dock icon that opens Cashflow in its own window.

Notes:
- Your data is tied to the browser you use. Stick with one browser (e.g. always Safari, or always Chrome).
- If you move or rename the folder, Safari may treat it as a new site and start blank — use Export data before moving, then Load data after.
- Export a backup file once in a while. It's your insurance and your way to move data between devices.

## Use it on your iPhone (requires hosting — one-time, ~5 minutes)

Apple only allows home-screen web apps that live at an `https://` address. Any static host works. GitHub Pages is free and permanent:

1. Create a free account at github.com (if you don't have one).
2. Click "+" → New repository. Name it `cashflow`, set it to Public, click Create. (Public means the app's code is visible — never your data. Data only ever lives on your devices.)
3. On the repository page: "uploading an existing file" → drag in every file in this folder → Commit changes.
4. Settings → Pages → under "Branch" choose `main` and Save.
5. After a minute your app is live at `https://YOURUSERNAME.github.io/cashflow/`.
6. On your iPhone: open that link in Safari → Share button → Add to Home Screen. It now opens full-screen like a native app, works offline, and saves data on the phone.

The same hosted link also works on your Mac: open it in Safari → File → Add to Dock.

## Moving data between devices

There is deliberately no cloud sync. To move your numbers: Export data on device A (produces a small `.json` file), get the file to device B (AirDrop works well), then Load data on device B. Treat exported files like bank statements — they contain your numbers.

## Updating the app

If you get a new version of `index.html`, just replace the old file (or re-upload it to GitHub). Your data is stored separately in the browser, so replacing app files never touches your numbers. On iPhone, after a re-upload, open the app, pull to refresh or close and reopen it twice — the offline cache updates in the background.
