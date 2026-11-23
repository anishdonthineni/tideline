# Tideline – Focus Dashboard

A small focus dashboard: a Pomodoro timer, a task list, and stats that show how much you actually focused. It runs in the browser with no sign-up and no backend.

**Live demo:** https://anishdonthineni.github.io/tideline/
**Source:** https://github.com/anishdonthineni/tideline
Submitted to the Creators AI Winter Challenge (open theme).

## Features

- Pomodoro timer with focus, break and long break modes, and a progress ring that fills as the session runs
- Custom session lengths for each mode, saved between visits
- Sound when a session ends, with an on/off toggle
- Spacebar shortcut to start or pause
- Task list: add, complete and delete tasks, and pick one as your current focus
- Session count shown on each task
- Stats: minutes and sessions today, tasks completed, and a 7-day bar chart
- Daily goal progress bar (100 focus minutes) and a day streak
- Light and dark mode that follow your device setting
- Keyboard-friendly, with labelled controls for screen readers
- Everything saves in your browser (`localStorage`), so nothing leaves your device

## Run it

No install or build step.

1. Download `index.html`.
2. Open it in any modern browser.

Or visit the live demo link above.

## How it works

- **Timer:** when you press Start, the app stores the session's end time and recalculates the time left from the clock on every tick. This keeps it accurate even if the tab is in the background and the browser slows its timers.
- **Progress ring:** an SVG circle whose `stroke-dashoffset` changes as time passes.
- **Sound:** a short tone generated with the Web Audio API, so no audio files are needed.
- **Storage:** tasks, the active task, session lengths and a per-day focus log are saved to `localStorage`. All reads and writes are wrapped in try/catch, so the app still works if storage is blocked.
- **Stats:** the weekly chart, daily goal and streak are all calculated from the daily log, with plain HTML elements and no chart library.

## Tech

HTML, CSS and vanilla JavaScript in a single file. SVG for the ring and the Web Audio API for sound. The Bricolage Grotesque typeface is loaded from Google Fonts.

## AI disclosure

This project was built with Claude (Anthropic) as a coding and design assistant, as the hackathon rules allow. I reviewed and tested the result and can explain how it works.

## Ideas for later

- Time tracking per task
- Optional sync across devices
- Adjustable daily goal and monthly insights
- Offline install as a PWA

## License

MIT. Fonts are served by Google Fonts under their own license.
