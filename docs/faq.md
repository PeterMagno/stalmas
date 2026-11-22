# Frequently Asked Questions (FAQ)

[Español](faq.es.md)

### 1. Is STALMAS free?
Yes. **STALMAS Free** has no ads and no time limit. It includes up to **3 servers** in total (Portainer and Linux SSH, split however you like), full container and stack actions, logs, SSH terminal (`xterm-256color`), Summary home-screen widget, PIN/biometric lock and the cloud Gemini AI assistant (with your own API key).

### 2. What does Pro include? Is it a subscription?
**No — STALMAS Pro is a one-time payment** ($14.99 USD base on Google Play; price varies by country), with no subscription and no renewal.

Pro unlocks:
- **Unlimited servers**;
- **On-device local AI** (offline Gemma models) + Auto / Local-first routing, reversible IP/host pseudonyms, per-server notes, custom skills, 20-message cloud memory and full searchable/exportable chat history;
- **One-tap AI diagnostics** for failing containers, filtered logs, compose files (with editor apply) and storage cleanup;
- **Background container & environment alerts** and per-container watch ("Alert me if it fails");
- **Custom dashboard & usage history** (6 h / 24 h / 7 d CPU/RAM charts, All servers, AI diagnosis, Last 24 h, Activity and Trend cards);
- **Single-container home-screen widget** with Restart button;
- **Pro terminal**: 500-command history view, unlimited snippets with `{{name}}` variables, customizable key row with cursor pad and 16,000 characters of AI screen context;
- **Encrypted AES-256 Google Drive backup** and **OLED, Catppuccin & STALMAS brand themes**.

See the full breakdown in [Free vs Pro](free-vs-pro.md).

### 3. Does it work with Portainer CE and BE?
Yes. STALMAS connects to both **Portainer CE** and **Portainer BE** using Portainer's public API. On Portainer 2.45+, creating stacks from Git supports Portainer Git Sources; on older versions, it uses repository URL and token.

### 4. Do I need to open ports?
No. STALMAS connects **directly from your phone** to your Portainer and SSH servers with no middleman servers. To reach your servers from outside your local network without opening ports to the public internet, use a **VPN** (such as WireGuard or Tailscale) or an encrypted tunnel.

Note that plain `http://` connections are blocked for public hosts and allowed only on private or local networks (`localhost`, `.local`, `10.x.x.x`, `172.16.x.x–172.31.x.x`, `192.168.x.x`).

### 5. Where are my credentials stored?
Only on your phone. STALMAS has no user accounts and no central servers. Server credentials, SSH keys, Portainer tokens, history and your Gemini API key are stored locally in an encrypted **SQLCipher (AES-256)** database and **AES-256-GCM** encrypted preferences protected by the Android Keystore. Android's automatic cloud backup is disabled.

### 6. Does the AI see my data?
Before anything is sent to Gemini in the cloud, STALMAS runs a **Privacy Gatekeeper** that automatically hides IPv4/IPv6 addresses, domains, URLs, passwords, tokens, keys and connection strings (and tells you how many items were hidden). On **Pro**, reversible pseudonyms let Gemini see placeholders like `[IP_1]` while displaying your real IPs locally (secrets are never restored), or you can use **Local AI** so queries never leave your phone.

*Important:* automated redaction is a safeguard, not a guarantee — avoid pasting secrets directly in chat.

### 7. Do I need a Gemini API key?
Yes, if you want to use **cloud AI** (both Free and Pro use **BYOK — Bring Your Own Key** from Google AI Studio, subject to your key's quota). If you use **Pro** with an on-device **Local AI** model on a compatible device, no Gemini API key or internet connection is needed for inference.

### 8. What phone do I need for local AI?
You need **Android 12+** and a **64-bit CPU** (`arm64-v8a` or `x86_64`), plus:
- **6 GB RAM** minimum for Gemma 4 E2B, or **8 GB RAM** for Gemma 4 E4B;
- Enough **free storage** (model size + 500 MB).

*Available features depend on your device's hardware.* If a phone lacks 64-bit support, RAM or space, the app disables or blocks incompatible downloads with an explanation.

### 9. Is there an iOS version?
Not for now. STALMAS is built for **Android 12 or later**.

### 10. Is it open source?
No. STALMAS is closed-source commercial software by **Peter Magno**. This public repository exists so the community can report bugs, propose ideas, discuss usage questions and follow release notes.

### 11. How do I report a bug?
Two ways:
1. Open a [Bug report](../../../issues/new?template=bug_report.yml) in this repository with your app version, device, Android version and steps to reproduce. **Never paste passwords, API tokens, SSH keys, real IPs or private domains.**
2. Inside the app, go to **Settings → About & legal → Report a problem**. STALMAS prepares a reviewable email draft to `report@stalmas.app` with sensitive data automatically hidden.

### 12. How do I request deletion of my data?
There is no account or central database to delete:
- **On your phone:** uninstall STALMAS or go to Android **Settings → Apps → STALMAS → Storage → Clear data**.
- **Google Drive backup (Pro):** delete it from Cloud Backup settings inside the app, or from your Google account (**Manage app data → STALMAS → Delete data**).
- **Emails, reports or tester sign-up:** email **support@stalmas.app** from the address you used to contact us.

Full instructions: [stalmas.app/en/delete-data/](https://stalmas.app/en/delete-data/).
