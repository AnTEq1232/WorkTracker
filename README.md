# WorkTracker

A Windows desktop app that automatically tracks your working time, so you can bill hourly work with confidence.

## Why I built it
Freelancers who bill by the hour need to know exactly how long they worked. Manual timers are easy to forget, so WorkTracker runs in the background and counts time only in the programs and websites you choose.

## Features
- Starts with Windows and runs quietly in the system tray.
- Tracks time only in the programs and websites on your own list.
- Ignores idle time (after 5 minutes by default, configurable).
- Shows hours for today and for the last 7 days.
- Breaks statistics down by program.
- All data stays on your computer.

## Tech stack
Electron, React, Vite, SQLite, Vitest.

## Getting started
```
git clone <repository-url>
cd worktracker
npm install
npm run dev
```

## How it works
1. Every few seconds the app checks the active window and the system idle time.
2. The `classify` function decides whether that moment counts as work and which item from your list it belongs to.
3. If it counts, the time is added to today's total in a local database.
4. The interface reads from the database and displays the statistics.

## Roadmap
Hourly rates and amounts, monthly and yearly views, login and multi-device sync, team and office dashboards.

## Limitations
Windows only, one computer. Website detection in browsers is based on [page URL / window title — fill in after the technical spike].
