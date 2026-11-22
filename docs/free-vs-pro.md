# Free vs Pro

[Español](free-vs-pro.es.md) · [Web version](https://stalmas.app/en/docs/free-pro/)

> **Available features depend on your device's hardware.**

**STALMAS Free** covers complete day-to-day administration of up to **3 servers in total** (Portainer and SSH, split however you like) with zero ads and no time limit.

**STALMAS Pro** is a **one-time purchase of $14.99 USD** base on Google Play — **no subscriptions and no renewals** (price varies by country and is displayed in your local currency on Google Play). Pro users can also leave an optional tip in *About* (unlocks no extra features).

## Connections

| Feature | Free | Pro |
|---|---|---|
| Portainer and Linux SSH servers (password or `.pem`/`.key` private key) | 3 in total, split however you like | Unlimited |
| UP/DOWN status of each server | Yes | Yes |
| Allow self-signed TLS certificate (per Portainer server) | Yes | Yes |

## Portainer: dashboard, containers and stacks

| Feature | Free | Pro |
|---|---|---|
| Fixed card dashboard: Health, Live resources (CPU/RAM/images), Top usage, Storage (reclaimable space), Quick access | Yes | Yes |
| Custom dashboard: edit (reorder, hide, add cards), Health/Operations presets, "Containers by stack" card | Locked | Yes |
| Pro dashboard cards: "All your servers" (health of every saved server) and "AI diagnosis" | Locked | Yes |
| Pro cards: "Last 24 h" (host CPU/RAM with peak), "Activity" (background monitoring findings even while closed), "Trend" (container approaching its memory limit fastest), "Activity" preset | Locked | Yes |
| Usage history: store CPU/RAM for up to 30 containers per environment on each check (7 days, encrypted, opt-in in Monitoring) | Locked | Yes |
| Container detail history: 6 h / 24 h / 7 d CPU and RAM charts with min, avg and max (tracks the container even if recreated) | Locked | Yes |
| Start, stop, restart, pause and resume containers | Yes | Yes |
| Container detail: color status header, link to its stack, Restart · Stop/Start · Console · Processes actions; Summary · Logs · Usage · Config tabs | Yes | Yes |
| Summary: failure reason (healthcheck output, Out of memory with limit, explained exit code) with Restart / View errors; copyable IP, ports, restarts & policy, uptime, CPU/RAM | Yes | Yes |
| Summary: "Alert me if it fails" per-container watch (alerts even when general monitoring is off; managed in Monitoring) | Locked | Yes |
| Summary: "Add to home screen" (preconfigured widget for that container) | Locked | Yes |
| Config: General, Resources, Healthcheck, Network and ports (tappable network → Networks), Volumes, Environment (secrets masked) and Labels | Yes | Yes |
| Rename container | Yes | Yes |
| Update container to latest image: pulls, compares and recreates with the same configuration; if part of a Portainer stack, offers redeploying the entire stack with fresh images | Yes | Yes |
| Kill and delete container, confirming by name | Yes | Yes |
| Live usage: CPU/RAM, network, disk and PIDs charts; process list | Yes | Yes |
| Multi-select: start, restart or stop multiple containers | Yes | Yes |
| Containers: tappable filter counts (All / Healthy / Problems / Stopped), search by name, image or port, Priority ("Need attention") and By stack views, CPU/RAM per row | Yes | Yes |
| Containers: "Explain" button on each issue (opens AI diagnosis with its logs) | Locked | Yes |
| Background alerts: notifies when a container stops, restarts unexpectedly, turns unhealthy, enters a restart loop, or an environment goes down (checks every 15–60 min, not real-time) | Locked | Yes |
| Home-screen widgets: Summary (running / stopped / problems; active server) | Yes | Yes |
| Home-screen widgets: single container with Restart and Refresh buttons, last-updated time and pick any saved server | Locked | Yes |
| Logs: ANSI colors, search, highlighted errors & warnings; toolbar icons: live stream, filters (20 to 10,000 lines, preset or date range, timestamps), All / Errors / Warnings counts, copy, export `.log` / share, go to first error | Yes | Yes |
| In-container console (`exec`) | Yes | Yes |
| One-tap AI log analysis: sends ONLY the currently filtered lines (max 100) and states what was sent; "Explain" in Summary and lists filters Errors and analyzes | Locked (paste manually in Free) | Yes |
| View stacks and their compose/ENV (read-only) | Yes | Yes |
| Stacks: real container health bar, tappable filter counts (All / Problems / Healthy / Inactive), in-place fix action, redeploy (confirmed), start, stop (confirmed) and delete stack (confirm by name), logs and "Containers without a stack" | Yes | Yes |
| Stacks: "Why does X fail?" button (opens AI diagnosis of the failing container) | Locked | Yes |
| Stack detail: Summary / Compose / Variables; Git (pull changes, configuration) | Yes | Yes |
| Create new stacks (Editor) | Yes | Yes |
| Create stack from Git (Source on Portainer 2.45+, URL and token on older versions) | Yes | Yes |
| New stack from template (Portainer and custom) | Yes | Yes |
| Analyze compose with AI and apply improvements to the editor | Locked | Yes |
| Storage: images and volumes (view, what uses them, delete, free space, pull latest version) | Yes | Yes |
| "What is safe to delete?" (AI) | Locked | Yes |
| Resources tab: disk usage card, Clean up (prune images, volumes, networks and build cache) and shortcuts to Images, Volumes and Networks | Yes | Yes |
| Networks (read-only): search by network or container, All / Unused filter, copyable subnet, gateway, scope and member containers (also from container Config) | Yes | Yes |

## Terminal (SSH and container console)

| Feature | Free | Pro |
|---|---|---|
| `xterm-256color` emulator with Esc/Tab/Ctrl and arrow keys | Yes | Yes |
| Copy last result | Yes | Yes |
| Command history per server (stores up to 500) | Views latest 50 | Views all 500 |
| Saved snippets | Up to 10, no variables | Unlimited, with `{{name}}` variables |
| Customizable shortcut key row with touch cursor pad | Locked | Yes |
| Keep screen on | Yes | Yes |
| AI reads your terminal screen | Up to 4,000 characters | Up to 16,000 characters (cloud) · 1,500 (local) |

## AI Assistant

### Shared core (Free and Pro)
| Feature | Limit / detail |
|---|---|
| Floating STALMAS assistant (character): movable bubble, visible by default and rising above the keyboard; resizable non-modal anchored panel; in-panel history; reply preview with ▶ / Apply; collapses automatically on run/apply | Up to 6 messages of recent memory (3 exchanges) |
| Cloud Gemini chat with your own key (BYOK), streaming, with stop button and retry status | Subject to your key's quota |
| Choose Gemini model with free/paid badge, dynamic list from your key, estimated tier checker and today's usage | 7-day local count |
| Privacy Gatekeeper ("redact and send"): IPv4/IPv6, domains, passwords, keys, connection strings; notice with redacted count and "view what was redacted" | Included |
| Copy reply & code blocks; regenerate; edit last question; retry after error | Included |
| Engine label on each reply | `CLOUD:` or `LOCAL:` |
| Temporary chat (not saved) | Included |
| Chat history, title search and configurable automatic retention | Title search only in Free |
| Server-isolated chats (tied to their server or environment, never mixed) | Included |
| Mandatory confirmation for dangerous commands (`rm -rf`, `docker system prune`…), even with auto-run | Included |
| Report an AI response | Flag button on every reply |
| Paste stacks or logs manually into chat | Included |

### Pro-only AI features
| Feature | Limit / detail |
|---|---|
| On-device local AI and model downloads (verified catalog & Hugging Face), preload and **Auto** accelerator by default (one-time GPU vs CPU probe per phone and model) or manual GPU/CPU | 4,000 shared characters total (`maxNumTokens <= 4,000`); min. 6/8 GB RAM depending on model |
| Auto mode: routes prompts with private data to the phone when a local model is installed; "Local AI first" option | Included |
| Reversible cloud pseudonyms: Gemini sees `[IP_1]`, you see your real values (**secrets are never restored**) | Included |
| Per-server or per-environment notes and "Local AI only" rule | Max 1,500 characters of notes |
| Custom skills (`SKILL.md`) | Included |
| Automatic stack or log reading ("Sees this screen" chip) and one-tap analysis | Stacks: max 16,000 chars (head); logs: last 100 filtered lines & max 16,000 chars (tail) in cloud; local max 1,500 chars; notice in chat if truncated |
| 20 messages of cloud memory (Free: 6) | 20 messages in cloud (10 exchanges); local up to 6 messages within 40% of local budget |
| Full history: full-text search inside messages, filter by server, pin, rename, export to Markdown | Included |
| Chats, notes and rules included inside encrypted backup | Included |

## Settings, security and data

| Feature | Free | Pro |
|---|---|---|
| 3-sheet welcome onboarding on first launch (skippable; replayable in About) | Yes | Yes |
| Language (English / Spanish) | Yes | Yes |
| Nord theme (default) | Yes | Yes |
| OLED, Catppuccin and STALMAS brand themes | Locked | Yes |
| PIN and biometric lock | Yes | Yes |
| Encrypted backup & sync (AES-256) to Google Drive | Locked | Yes |
| App Logcat viewer | Yes | Yes |
| Report a problem / error collection | Yes | Yes |
| About, open-source licenses, legal notices and support | Yes | Yes |
| Support development (optional tip, 3 amounts; unlocks no features) | — | Yes |

## Device hardware requirements

| Feature | Device requirement | App behavior if missing |
|---|---|---|
| STALMAS app | **Android 12+** (API 31 or higher) | Google Play restricts installation to supported devices. |
| Local AI (engine & models) | **64-bit CPU** (`arm64-v8a` or `x86_64`), **6 GB RAM** min (Gemma 4 E2B) or **8 GB RAM** (Gemma 4 E4B), and free storage (model size + 500 MB) | Without 64-bit, disables catalog, search, import and activation with a notice; blocks incompatible downloads or reverts to the previous valid model. |
| Biometric lock | Biometric sensor with enrolled fingerprint or face unlock | Biometric switch is disabled with an explanation; PIN unlock stays available. |
| Google Drive backup | **Google Play Services (GMS)** | Drive link/upload/restore actions disabled with a notice; encrypted local file backup remains available. |
| Background alerts | Notification permission (`POST_NOTIFICATIONS`) and unrestricted background battery settings | Requests permission on enable; aggressive vendor battery limits may delay periodic checks. |
| Home-screen widgets | Launcher that supports pinning widgets | Hides or disables pin shortcut when unsupported by the launcher. |
