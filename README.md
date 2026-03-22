# Learning Terminal

A distraction-free educational game for toddlers (ages 2–4), styled as a retro monochrome CRT terminal.

## Games

- **Spelling** — Spell 3-letter words one letter at a time by selecting the correct letter from four choices.
- **Counting** — Count on-screen dots and pick the matching number.
- **Addition** — Solve single-digit addition problems by choosing the correct answer.

## Design

- High-contrast green-on-black palette with a scanline CRT effect
- All-caps monospace font (Courier New)
- No distracting animations, ads, or external dependencies

## Audio

Synthesized sounds via the Web Audio API — no audio files required:

- **Correct letter** — short ascending two-tone beep
- **Wrong answer** — brief descending buzz
- **Round complete** — four-note ascending fanfare

## Tech Stack

- Vanilla HTML, CSS, and JavaScript (no frameworks, no build step)
- Deployed as a static site via GitHub Pages

## Running Locally

Open `index.html` directly in a browser — no server or install needed.

## Deployment

Pushes to `main` automatically deploy to GitHub Pages via the workflow in `.github/workflows/deploy.yml`.
