# Little Desk
Cozy pastel study dashboard: reminders, Pomodoro, Quran routine reminders, PDF extraction, flashcards, quizzes, AI chat, notes, themes/fonts, and animated cat corner.

## Deploy
1. Upload the contents of this folder to a GitHub repository.
2. Import the repository into Vercel.
3. In Vercel → Project Settings → Environment Variables, add `OPENAI_API_KEY` with a private API key. Optional: `OPENAI_MODEL` (defaults to `gpt-4.1-mini`).
4. Redeploy. Keep the key server-side only. Never paste it into `app.js`, `index.html`, or GitHub.
5. API use may incur charges. Ask a parent/guardian to help with account and billing setup if needed.

## Notes
- Without AI configuration, PDF text is extracted in-browser and simple local practice prompts are generated. AI chat and better AI-generated cards/quizzes require the server endpoints and internet.
- Scanned PDFs need OCR; this version extracts selectable text.
- Tasks, notes, reminders and settings use browser localStorage on this device/browser. Export a backup from Customize. Clearing browser data can erase saved information.
- Service worker caches the app shell after the first HTTPS visit. AI requires internet.
- Quran reminders are user-created prompts, not an authoritative Quran text/tafsir source. Browser notifications need permission and may not run while browser/device is closed.
- Avoid uploading patient-identifiable or other sensitive information. AI study tools can make mistakes; verify against course materials and trusted references.
