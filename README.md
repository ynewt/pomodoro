# Pomodoro Timer

A small Pomodoro timer that runs in the browser, served by a minimal Flask app. All the timer logic lives in the page itself (`templates/index.html`); Flask just serves it.

## Features

- **Three modes:** Work (25 min), Short Break (5 min) and Long Break (15 min).
- **Automatic cycling:** after each finished work session it switches to a short break, and every 4th session to a long break.
- **Session counter** showing how many work sessions you've completed.
- **Countdown in the browser tab title** (e.g. `24:13 - Pomodoro`), so you can see it from other tabs.
- **Desktop notifications** when a timer ends (the browser asks for permission the first time).
- **Celebration screen** with an animation when a work session finishes.
- **Settings (⚙):** change each mode's length (in minutes) and color. Settings are saved in the browser's `localStorage`, so they persist between visits.

## Running it

Requires Python 3 and Flask.

```bash
pip install -r requirements.txt
python app.py
```

Then open http://localhost:5001.

## Files

| File | Purpose |
|---|---|
| `app.py` | Flask app that serves the page on port 5001 |
| `templates/index.html` | The whole timer UI: HTML, CSS and JavaScript |
| `requirements.txt` | Python dependencies (`flask`) |
