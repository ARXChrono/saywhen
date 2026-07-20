# Product

## Register

product

## Users

People mid-task with their hands or attention elsewhere: cooking several dishes at once, doing interval workouts, running pomodoro sessions, steeping tea, timing laundry. They set a timer, walk away from the screen, and rely on hearing the alert rather than watching the page.

## Product Purpose

saywhen is a browser-based multi-timer where every timer speaks a custom message aloud when it fires. It exists because generic timer beeps don't tell you *which* timer went off; a spoken "check the oven" does. Success: a user runs three overlapping timers, never looks at the screen, and always knows what just finished. Ships as a single self-contained `index.html` with no backend and no build step.

## Brand Personality

Calm, dependable, unfussy. A utility that disappears into the task. The one flourish is the voice itself, so the UI stays quiet and lets audio carry the personality.

## Anti-references

- Novelty timer sites drowning in ads and cookie walls
- Dashboard-cosplay: hero metrics, gradient cards, decorative charts
- Anything requiring an account, a spinner, or a network connection

## Design Principles

1. **Glanceable at distance**: the countdown is the biggest thing on every card; readable from across a room.
2. **Audio-first**: visual state supports the spoken alert, never substitutes for it.
3. **Zero-friction setup**: a new timer is usable in two clicks (preset + start).
4. **Trust the clock**: drift-free timestamp math; never lie about remaining time, never auto-resume after reload.
5. **One file, forever**: no dependency, build step, or backend may be added without revisiting this document.

## Accessibility & Inclusion

- Full keyboard operability with visible focus states
- `prefers-reduced-motion` respected (no pulse/transitions)
- Text contrast ≥ 4.5:1 on the dark surface
- Status is conveyed by text labels, not color alone
