# ATLAS

A premium, minimal fitness OS for tracking workouts, stretches, mobility work, and body measurements — built as a single self-contained web app with no backend and no build step.

![ATLAS](atlas-logo.png)

## Overview

ATLAS replaces a notebook or spreadsheet with a fast, dark, athletic-styled tracker that lives entirely in your browser. Everything is editable — there's no fixed exercise database to fight against, just a clean structure you fill in yourself and check off day to day.

## Features

- **Daily progress ring** — a homepage ring that fills based on how many sets you've completed today, computed live from your workout plan
- **7-day workout planner** — editable exercise lists (name, sets, reps) for every day of the week
- **Today view** — tap-to-complete set tracking that drives the progress ring
- **Stretch library** — separate lists for Monday–Sunday plus a "Daily" category
- **Warm-up, posture, and jaw exercise lists** — simple editable lists for non-tracked routines
- **Measurements** — quick-set height and weight, plus a body-part-by-body-part measurement log (cm)
- **Lift log** — record each exercise's max as either a weight (kg) or a sets × reps target
- **Monthly calendar** — days are filled when you hit 100% of that day's plan, outlined at 50%+, and plain otherwise
- **Local persistence** — all data saves to `localStorage`, so it survives refreshes and browser restarts on the same device

## Tech Stack

- Plain HTML, CSS, and JavaScript — no frameworks, no bundler, no dependencies
- `localStorage` for data persistence
- Google Fonts (Space Grotesk + Inter) loaded via CDN
- Single file: everything (markup, styles, logic) lives in `atlas.html`

## Getting Started

No installation required.

1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/atlas.git
   cd atlas
   ```
2. Open `atlas.html` directly in a browser, or serve it locally:
   ```bash
   python3 -m http.server 8000
   ```
   then visit `http://localhost:8000/atlas.html`

## Usage

- Set up your week from **Workouts** — add exercises with sets and reps for each day
- Open **Today's workout** from the home screen to check off sets as you train; the progress ring and calendar update automatically
- Use **Stretches**, **Warm-up**, **Posture**, and **Jaw** for simple reference lists you maintain yourself — each has an edit view with add/remove
- Log your height, weight, and body measurements from **Measurements**
- Track your lifting numbers in the **Lift log**, choosing weight (kg) or sets × reps per exercise

## Data & Privacy

All data stays on-device in the browser's `localStorage` — nothing is sent to a server. Clearing your browser data or switching browsers/devices will reset the app, since there is no sync or account system.

## Customization

- **Branding**: the app name and logo live in the top bar; swap the embedded logo image or restyle the wordmark in the `<head>`/CSS
- **Home screen icon**: add an `apple-touch-icon` link tag in `<head>` to make the app installable as a home-screen icon on mobile
- **Color palette**: all colors are defined as CSS custom properties at the top of the stylesheet (`:root`), so the accent color, surfaces, and text tones can be swapped in one place

## License

Add your preferred license here (e.g. MIT) before publishing the repo publicly.
