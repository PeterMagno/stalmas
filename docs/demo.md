# Demo server guide

[Español](demo.es.md)

Try STALMAS without exposing your own infrastructure. We provide a public Portainer demo server with fictitious data and simulated actions — nothing real is affected.

## Credentials

| Field | Value |
|---|---|
| **Server type** | Portainer |
| **Server URL** | `demo.stalmas.app` (keep `https://` selected) |
| **Authentication Method** | Username / Password |
| **Username** | `demo` |
| **Password** | `stalmas-demo` |

## Step-by-step setup

1. Open STALMAS. On the welcome screens, tap **Skip** (or swipe through and tap **Get started**).
2. On **Servers**, tap **Add Server** (or `+` → **Add New Server**) and choose **Portainer**.
3. Fill in the connection form:
   - **Alias:** any name you want (for example, `Demo`).
   - **Server URL:** `demo.stalmas.app` (keep the `https://` prefix selected).
   - **Authentication Method:** select **Username / Password**.
   - **Username:** `demo`
   - **Password:** `stalmas-demo`
4. Tap **Save & Connect**.
5. Tap your demo server to list its environments.

## What is inside the demo

- **2 environments** (including **`homelab`**) populated with fictitious stacks, containers, images, volumes and networks.
- One container named **`worker`** is **intentionally unhealthy / failing** so you can inspect a real troubleshooting flow.
- Actions in the demo are simulated: starting, stopping or inspecting containers does not affect any real system.

> Note: Linux SSH connections require an SSH server you control. For security reasons, there is no public demo SSH shell.

## What to try

1. **Explore the overview:** open the **`homelab`** environment and browse **Dashboard**, **Containers**, **Stacks** and **Resources** (Images, Volumes, Networks).
2. **Inspect the failing `worker` container:**
   - Open **Containers** (filter by **Problems** or look under **Need attention**), or find it in **Stacks**.
   - Tap `worker` to view **Summary** (failure reason, restarts, ports) and switch to **Logs** to search or filter **Errors only**.
3. **Ask the AI assistant why `worker` fails:**
   - Tap the floating **STALMAS** bubble at any time to ask about `worker`.
   - If you have **Pro** active (for example during the closed test), tap **Explain** on the failing container or **Why does worker fail?** in **Stacks** to send the filtered error logs directly to the AI.
   - On **Free**, open **Logs**, copy the error lines and paste them into the AI chat.
   - *Tip:* Cloud AI uses your own Gemini API key (**Settings → AI Integration**). With Pro on a compatible 64-bit phone (6–8 GB RAM), you can also download a local Gemma 4 model and run the analysis completely offline.

Found something unexpected or have a suggestion? Check [How to contribute](../CONTRIBUTING.md) or [open an issue](https://github.com/PeterMagno/stalmas/issues/new/choose).
