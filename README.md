# Pain Tracker

A personal, mobile-first web app for logging sacral / SI-joint pain, built to capture an honest, timestamped record to share with a rheumatologist. Deliberately NOT a diagnostic tool — it only captures and visualizes data.

## What it does

- Log — fast Tier 1 quick entry (pain intensity, position, interventions) plus a once-daily Tier 2 summary (morning stiffness, night pain, sleep, steps, training, symptom detail).
- History — chronological list of all entries, editable and deletable.
- Insights — pain-over-time chart with adjustable windows (7/14/30/all), toggleable marker layers (NSAID, training, yoga, preceding stillness), morning-stiffness and night-pain bands, and summary stats. Designed to make the inflammatory-vs-mechanical signal visible at a glance.
- CSV export — for sharing with a doctor; CSV import as backup.

## Tech stack

- Single index.html — vanilla JS, inline CSS/JS, no frameworks
- Firebase Authentication (Google sign-in)
- Cloud Firestore (data sync across devices, owner-only security rules)
- Firebase Hosting (Spark / free plan)

## Run / deploy

The app is a single static file backed by Firebase. Deploy with the firebase deploy command.

Live at: https://pain-tracker-a0f0d.web.app

## Design conventions

- Stats are descriptive, never diagnostic.
- "Logged None" and "no data" are always visually distinct (a blank must never imply "no symptom").
- Severity fields store an ordered numeric rank alongside text, so charts color-code by rank.

## Status

Live and functional. Open items: mobile scroll fix (Samsung S25 / Chrome), confirm cross-device sync, optional PWA add-to-home.
