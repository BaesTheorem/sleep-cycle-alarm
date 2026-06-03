# Sleep Cycle Alarm (PWA)

A tiny, offline, installable web app that tells you the best time to wake up so
you land at the **end of a sleep cycle** (in light sleep) instead of mid-deep-sleep.
You then set that time as your Fitbit Charge 5's native **Smart Wake** alarm.

**Live:** https://baestheorem.github.io/sleep-cycle-alarm/

## How it works

A sleep cycle averages ~90 min. Waking at a cycle boundary feels far better than
waking mid-cycle. Enter your bedtime; the app shows wake times for 3–7 completed
cycles. The "Set alarm" time is the cycle boundary **+ 15 min**, so the Charge 5's
Smart Wake window (it fires within 30 min *before* the set time) brackets your
light-sleep boundary. The watch handles the actual in-the-moment wake — this app
is the math.

## Personalization

The default cycle length is the textbook 90 min. Your real cycle may differ — set
your own value in the **Your cycle** field and it's saved on your device
(localStorage). **No personal data is stored in this repo or transmitted anywhere**;
it lives only in your browser.

## Install

- **iOS:** open the link in Safari → Share → **Add to Home Screen**.
- **Android/desktop Chrome:** open the link → **Install** prompt (or the Install button).

Fully static — once installed it runs offline, no server.

## Files

- `index.html` — UI + calculator (all logic client-side)
- `manifest.webmanifest`, `sw.js` — PWA install + offline cache
- `icons/` — app icons
