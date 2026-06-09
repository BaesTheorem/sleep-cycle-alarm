# Sleep Cycle Alarm (PWA)

A tiny, offline, installable web app that tells you the best time to wake up so
you land at the **end of a sleep cycle** (in light sleep) instead of mid-deep-sleep.
You then set that time as your Fitbit Charge 5's native **Smart Wake** alarm.

**Live:** https://baestheorem.github.io/sleep-cycle-alarm/

## How it works

A sleep cycle averages ~90 min. Waking at a cycle boundary feels far better than
waking mid-cycle. The "Set alarm" time is the cycle boundary **+ 15 min**, so the
Charge 5's Smart Wake window (it fires within 30 min *before* the set time)
brackets your light-sleep boundary. The watch handles the actual in-the-moment
wake — this app is the math.

It plans both directions:

- **Going to bed at…** — enter your bedtime; see wake times for 3–7 completed
  cycles and the alarm to set for each.
- **Must be up by…** — enter a hard wake-by time; it becomes the alarm's upper
  bound, and the app works backward to the bedtimes that land N full cycles just
  before it. Pick the row with the sleep you want and go to bed at that time.

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
