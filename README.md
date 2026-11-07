# PAKISTAN: STATECRAFT — prototype 0.1.0

A mobile-first, single-player government simulation prototype. It is a game concept, not official government software and not a source of real-world intelligence.

## Current playable features
- Prime Minister dashboard with eight fictional national indicators.
- Six cabinet ministers with expertise, confidence and advisory statements.
- Intelligence room with five fictional opening briefings and meaningful policy choices.
- Decision effects update the game state immediately.
- Advance through a 30-day first-term scenario; periodic service-delivery events appear.
- End-of-month performance report.
- Local save in browser storage; no account or backend required.
- Responsive layout and offline-capable PWA shell.
- Capacitor Android wrapper configuration and GitHub Actions debug-APK workflow.

## Run locally
Requires Node.js 20+.

```bash
npm install
npm run start
```

Open the local Vite URL in a browser. To build static web assets:

```bash
npm run build
```

## Install on Android before an APK is built
Deploy the `dist` folder to an HTTPS static host (for example, GitHub Pages with an appropriate base path, Cloudflare Pages, or Netlify). Open the deployed site in Chrome on Android, then use **⋮ → Add to Home screen** or **Install app**. Browser support and wording vary.

## Build an APK using GitHub Actions
1. Create a new GitHub repository and upload this project.
2. Push the default branch as `main`.
3. Open the repository's **Actions** tab.
4. Run **Build Android APK** (or let it run after a push).
5. Open the successful workflow run and download the `pakistan-statecraft-debug-apk` artifact.
6. Extract the artifact and install `app-debug.apk` on your Android device. Android may ask you to allow installation from that source.

This produces a **debug APK** for testing, not a Play Store release. A signed release requires a private signing key and a separate secure signing configuration. Never commit a keystore or passwords to the repository.

## Current limitations
- Single-player, local-only prototype; no multiplayer, accounts, cloud saves or live news ingestion.
- Scenario reports are explicitly fictional. The game does not fetch or claim to verify real news.
- Economy and diplomacy are simplified 0–100 game indices, not real forecasts or official data.
- No detailed constitutional law, parliamentary seat simulation, court system, elections, military operations or province-level budgets yet.
- Game balance, accessibility, security review and extensive device testing are still required.

## Suggested next milestones
1. Add backend accounts and cloud save (with privacy/security review).
2. Add a deterministic simulation service and event scheduler.
3. Add an OSINT ingestion pipeline with source links, dates and verification labels; never allow generated text to invent sources.
4. Expand parliament, provinces, elections, public services and foreign relations.
5. Add closed-beta analytics and balance testing before any multiplayer or monetisation.
