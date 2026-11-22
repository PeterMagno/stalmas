# Privacy summary

[Español](privacy.es.md) · [Full Privacy Policy](https://stalmas.app/en/privacy/) · [Data deletion](https://stalmas.app/en/delete-data/)

STALMAS has **no user accounts** and **no servers of our own storing your data**. Everything lives on your phone, encrypted, and the developer (**Peter Magno**) cannot see it.

## What goes where

| Data | Where it lives | Does the developer receive it? |
|---|---|---|
| Servers, SSH keys, passwords, tokens, history, AI chats | Your phone, encrypted (SQLCipher AES-256 + AES-256-GCM preferences via Android Keystore; OS auto-backup disabled) | **No** |
| Google Drive backup (optional, Pro) | Hidden private folder in your Google Drive (`drive.appdata`), encrypted with your password | **No** (if you forget the password, it cannot be recovered) |
| Gemini AI queries (optional) | Google's servers, using your own API key (BYOK) | **No** |
| Local AI model downloads (optional, Pro) | Downloaded directly from Hugging Face (anonymous catalog fetch from `stalmas.app`) | **No** |
| Support emails, problem reports and AI response reports | Our mailbox (`support@stalmas.app` / `report@stalmas.app`) | **Yes, only what you choose to send** (from your own email app as a reviewable draft) |
| Tester sign-up (email + alias) | Our mailbox (`testers@stalmas.app`) and Google Play tester list | **Yes, only for the closed test** (deleted max 30 days after the test ends) |
| Purchases | Google Play | **No** (we never see your card) |

## Key safeguards
- **No analytics, ads, tracking, profiling or data sales.**
- **Direct server connections:** your phone talks directly to your Portainer and SSH hosts; plain HTTP is restricted to private/local networks.
- **Privacy Gatekeeper:** before sending prompts to Gemini, STALMAS masks IPs, domains, URLs, passwords, keys and connection strings (and also before building problem/AI report drafts). Automated masking is a safeguard, not a guarantee — always review text before sending.
- **Minimal Android permissions:** Internet & network state, notifications (model downloads and container monitoring), and `dataSync` foreground service (finishing local model downloads). No access to location, contacts, photos, camera or microphone.

For full legal details, retention periods and regional rights, read the [Privacy Policy](https://stalmas.app/en/privacy/).
