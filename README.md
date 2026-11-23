# Tab Stacks

A lightweight, local-first Chrome extension used to save tabs in the current window, preserve existing Chrome tab groups, closing ordinary web tabs and restore a saved session later.

It also includes a small detail pad for each saved session that pairs free-form notes with an outline of saved groups, page titles, favicons, and URLs.

## Features

- **Save session:** captures the current window without closing anything, with live tab and group counts updated automatically.
- **Save & close tabs:** uses a two-step inline confirmation, saves first, then closes restorable web tabs while leaving Chrome's protected pages open (or leaving one blank tab if every tab is closable).
- **Restore session, group, or single tab:** reopens saved pages concurrently in the current window and recreates original tab groups (names, colours, collapsed state, and pinned state), or lets you restore a single group or click an individual tab.
- **Memory-safe restore:** optional setting to discard background tabs immediately upon restore so large sessions consume minimal RAM.
- **Update & undo:** overwrite a saved session with the current window's tabs, rename sessions inline, and undo accidental deletions or updates from the notification bar.
- **Detail pad & export:** store notes alongside your tab outline, search across all sessions, copy as plain text or Markdown, insert into a focused webpage field, or back up/restore sessions via local JSON files.
- **Local storage only:** session metadata and notes stay in Chrome's local extension storage (`chrome.storage.local`). The extension makes zero network requests.

## Install in Chrome

1. Download and unzip `tab-stacks-extension.zip`.
2. Open `chrome://extensions` in Chrome.
3. Turn on **Developer mode**.
4. Select **Load unpacked**.
5. Choose the unzipped folder containing `manifest.json`.
6. Pin **Tab Stacks** from the Extensions menu, click its toolbar icon, or press `Alt+Shift+S` (`Option+Shift+S` on macOS) to open the side panel.

Requires Chrome 116 or later for the Side Panel API.

## Project files

- `manifest.json` — extension manifest, permissions, and keyboard shortcut
- `service-worker.js` — configures toolbar-click side-panel behaviour
- `sidepanel.html` — side-panel structure
- `sidepanel.css` — responsive light/dark styling
- `sidepanel.js` — live telemetry, session capture, storage, restore, search, JSON backup, and detail-pad logic
