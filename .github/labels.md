# Suggested repository labels

Run these commands with the GitHub CLI (`gh`) to create the repository labels:

| Label | Color | Description |
|---|---|---|
| `bug` | `#d73a4a` | Something isn't working as expected |
| `idea` | `#a2eeef` | Feature request or improvement idea |
| `ai` | `#fbca04` | AI assistant (cloud Gemini or local models) |
| `portainer` | `#0075ca` | Portainer containers, stacks, logs or resources |
| `ssh` | `#0e8a16` | SSH terminal, host keys or snippets |
| `ui` | `#d876e3` | User interface, themes or copy |
| `tablet` | `#5319e7` | Tablet or large-screen layout |
| `translation` | `#c5def5` | English or Spanish wording issues |
| `good first report` | `#7057ff` | Helpful first report or easy verification |
| `wontfix` | `#ffffff` | Not planned for now |
| `duplicate` | `#cfd3d7` | Already reported elsewhere |

```bash
gh label create "bug" --color "d73a4a" --description "Something isn't working as expected" --force
gh label create "idea" --color "a2eeef" --description "Feature request or improvement idea" --force
gh label create "ai" --color "fbca04" --description "AI assistant (cloud Gemini or local models)" --force
gh label create "portainer" --color "0075ca" --description "Portainer containers, stacks, logs or resources" --force
gh label create "ssh" --color "0e8a16" --description "SSH terminal, host keys or snippets" --force
gh label create "ui" --color "d876e3" --description "User interface, themes or copy" --force
gh label create "tablet" --color "5319e7" --description "Tablet or large-screen layout" --force
gh label create "translation" --color "c5def5" --description "English or Spanish wording issues" --force
gh label create "good first report" --color "7057ff" --description "Helpful first report or easy verification" --force
gh label create "wontfix" --color "ffffff" --description "Not planned for now" --force
gh label create "duplicate" --color "cfd3d7" --description "Already reported elsewhere" --force
```
