# THE 1,000 HOURS OF WISDOM™

A premium, single-file spiritual growth, prayer-tracking, wisdom-development and personal-transformation platform. The goal: **complete 1,000 hours of prayer before December 31, 2026**, with everything you record kept **locally and privately on your own device**.

The entire application is one self-contained `index.html` — no build step, no server, no external dependencies, no tracking. Open it, or deploy it, and it just works.

---

## Features

- **Executive dashboard** — progress ring, animated counters, live countdown, at-a-glance stats, weekly/monthly reports, personalized insights, activity heatmap and dual timelines.
- **Completion forecast engine** — a recency-weighted, variance-aware statistical model that projects **Best / Expected / Worst** finish dates, each with a confidence percentage, updated live.
- **Immersive prayer session** — precise start/pause/resume/stop timer, manual entry, edit/delete, categories, notes, plus a **Focus Mode** (fullscreen, drifting particles, breathing guide and gently generated ambient sound).
- **Gamification** — XP, levels, an 11-tier rank ladder, four living scores (Wisdom · Consistency · Devotion · Growth), daily/weekly/monthly missions, personal records, 33 achievements including hidden ones, and celebration animations.
- **Wisdom Library** — ~90 curated verses across 21 themes with search, filters, favorites, highlights, personal notes, a Random Wisdom mode and Recently Viewed.
- **Wisdom Journal** — rich-text editor, moods, tags, categories, images, autosaving drafts, and card/timeline views.
- **Analytics** — interactive, animated charts with hover tooltips, selectable ranges, category breakdowns and a 3-scenario projection.
- **Goals, Daily Reflection, Prayer Calendar (click any day to log), and an interactive Vision Board.**
- **Settings** — light/dark themes, six accent palettes, motion controls (full/reduced/off), performance mode, ambient-sound controls, and full data management.

## Data & durability

Your data never leaves your device. It is stored with a layered, resilient persistence system:

1. **IndexedDB** — primary durable store, safe for large data (e.g. journal images).
2. **localStorage** — mirror, with a **synchronous flush on tab close / refresh** so nothing is lost.
3. **In-memory** fallback for restricted preview sandboxes.

It also includes schema **versioning + migrations**, **integrity checks**, automatic **backup snapshots** (with one-click restore), **crash recovery**, and **undo/redo** (⌘/Ctrl-Z / Y). Export a full JSON backup any time, and re-import it on any device.

> Note: in-app previews (inside some chat/embed sandboxes) may block browser storage. Deploy the app or open `index.html` directly and persistence works permanently.

## Keyboard shortcuts

`P` start prayer · `F` focus mode · `Space` start/pause timer · `D` `L` `J` `A` jump to Dashboard/Library/Journal/Analytics · `1–9` jump to sections · `T` theme · `⌘/Ctrl-Z / Y` undo/redo · `Esc` close.

---

## Run locally

Just open `index.html` in any modern browser. That's it.

## Deploy to Vercel

**Option A — GitHub (recommended)**
1. Create a new GitHub repository and add `index.html`, `README.md`, `vercel.json`, `.gitignore`.
2. On [vercel.com](https://vercel.com) → **Add New → Project → Import** your repo.
3. Framework preset: **Other**. No build command, no output directory needed.
4. Click **Deploy**. Your app is live in seconds.

**Option B — drag & drop**
Install the CLI (`npm i -g vercel`), run `vercel` in this folder, and follow the prompts — or drag the folder onto the Vercel dashboard.

Because this is a static site, there is nothing to configure. `vercel.json` only adds sensible security headers and clean URLs.

## Tech

Vanilla HTML + CSS + JavaScript, organized into clear modules (Config · Constants · Utils · Storage · Store · Business Logic · Animation · Charts · UI · Views · Router · Boot). Charts, animations, confetti and ambient audio are all hand-built — zero third-party libraries.

---

*"The fear of the LORD is the beginning of wisdom." — Proverbs 9:10*
