# Changelog

All notable changes to STALMAS are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
Release notes for testers: [v1.0.0-beta.2](docs/releases/v1.0.0-beta.2.md) ([Español](docs/releases/v1.0.0-beta.2.es.md)).

## [1.0.0-beta.2] — closed testing (Google Play, versionCode 10)

### Added
- **Servers & Security:** direct Portainer (API Key or Username/Password, optional self-signed TLS) and Linux SSH connections (password or `.pem`/`.key` private key with first-connection TOFU host key verification); no accounts or middleman servers. Local SQLCipher (AES-256) database and AES-256-GCM preferences protected by the Android Keystore, PIN and biometric app lock, and encrypted AES-256 Google Drive backup (Pro).
- **Dashboard:** per-environment health overview (healthy, failing and stopped containers, live CPU/RAM, reclaimable space and quick actions), plus Pro customizable layouts, presets and extra cards ("All your servers", "AI diagnosis", "Last 24 h", "Activity", "Trend").
- **Containers & Logs:** start, stop, restart, pause, resume, rename, kill, delete, bulk actions, image updates (with full-stack redeploy option), in-container console (`exec`), live usage charts and processes, 6 h / 24 h / 7 d usage history (Pro), and colorized ANSI logs with search, error/warning filters, date ranges and `.log` export.
- **Stacks & Resources:** create stacks from Compose Editor, Git (Source on Portainer 2.45+ or URL/token on older versions) or templates; edit Compose and environment variables, redeploy, pull Git changes, inspect standalone containers, manage images and volumes, inspect read-only networks, and run safe cleanup (prune).
- **SSH Terminal:** `xterm-256color` emulator with Esc, Tab, Ctrl and arrow keys, command history (50 Free / 500 Pro), snippets (10 Free / unlimited with `{{name}}` variables Pro), customizable key row with cursor pad (Pro), and keep-screen-on option.
- **AI Assistant:** floating STALMAS assistant with cloud Gemini (BYOK, streaming, model selector and 7-day local usage count), Privacy Gatekeeper (automatic masking of IPs, domains, passwords and keys), dangerous command confirmation, response reporting, and Pro features: on-device local AI (LiteRT-LM), Auto/Local-first mode, reversible IP/host pseudonyms, per-server notes, custom skills, one-tap diagnostics for containers/logs/compose/storage, and full searchable/exportable history.
- **Monitoring & Widgets:** Summary home-screen widget (Free), per-container widget with Restart button (Pro), and background container/environment alerts with optional per-container watch (Pro).
- **Themes & Support:** bilingual UI (English / Spanish), Nord theme (Free) and OLED, Catppuccin and STALMAS themes (Pro), 3-sheet onboarding, Reports center (readable errors, "Ask the AI what it means" and reviewable email drafts).
