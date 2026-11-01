# Medstudy — Your Study Space

A local-first, offline-friendly medical school study companion.

## Included
- Dashboard with study totals, due cards, streak, and recent activity
- Flashcard decks and cards with simple spaced-repetition scheduling
- Multiple-choice quizzes with saved scores and attempts
- Subject folders and searchable notes
- Pomodoro focus timer with recorded completed sessions
- Progress statistics and a 7-day study chart
- JSON backup and restore
- IndexedDB storage on the current browser/device
- PWA manifest and service worker for offline app-shell caching

## Run locally

For the service worker and install/offline features, serve this folder from `localhost` or an HTTPS host. Opening `index.html` directly with `file://` will still show the app, but browsers do not allow service workers in that mode.

With Python installed, from this folder run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser. Visit once while online, then reload once so the service worker can cache the app shell. After that, the app shell and your saved records are available offline in that browser.

## Deploy

Upload the contents of this folder to any static HTTPS host (for example, GitHub Pages, Netlify, or Vercel). No database or account is required. Once loaded online, the service worker caches the app shell. Your records remain local to that browser and device; they are not synced to other devices.

## Important storage note

Study data is saved in the browser's IndexedDB. Clearing browser site data, using a different browser/profile, or changing devices can make that local data unavailable. Use **Backup & restore → Download backup** regularly and keep the `.json` file somewhere safe. Restoring a backup merges records by ID, replacing matching records.

## Privacy

This app does not send study records to a server. Google Fonts are referenced for typography when online; the app falls back to system fonts offline. All app features and study data work without the font service.
