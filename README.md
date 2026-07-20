# saywhen

Browser-based multi-timer app with text-to-speech alerts. Name a timer, start it, and walk away: when time is up, your browser speaks the timer's name out loud.

- Multiple independent timers, each with its own name and duration; the alert speaks the name
- **Repeat** switch: off fires a single time, on re-arms and repeats (with a fire counter)
- Microwave-style **+10s / +30s / +1m / +5m** buttons, which also extend a running countdown
- Drift-free timing based on target timestamps, not tick counting
- Voice picker, speech rate and volume sliders, and an optional chime before each announcement
- **Pop out** button floats the whole app in an always-on-top window (Document Picture-in-Picture, Chromium browsers)
- Everything saved to `localStorage`, plus JSON export/import for backups
- No build step, no backend, no dependencies: one self-contained HTML file

## Run it

Open `index.html` in a browser. That's it.

Or serve it statically if you prefer:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

Works on any static host (GitHub Pages, Netlify, an S3 bucket, a USB stick).

## Notes

- Speech uses the browser's built-in `SpeechSynthesis` API, so available voices depend on your OS and browser.
- Most browsers require one interaction (e.g. clicking Start or Test voice) before audio is allowed to play.
- Running timers are restored **paused** after a reload, never auto-resumed.
