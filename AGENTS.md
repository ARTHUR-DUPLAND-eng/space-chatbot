# AGENTS.md

## Project
Single-file static app: `index.html` (French "SpaceBot" chatbot). No backend, no build step, no package manager. Calls Groq and NASA APIs directly from the browser via fetch.

## Running
`docker compose -f docker-compose.base44.yml up -d` — serves the repo directory with nginx:alpine on host port 3000. `index.html` is bind-mounted read-only, so edits appear on browser refresh (call `reload_preview` after edits if needed).

## Credentials
No server-side secrets required to boot. The Groq API key is entered by the end user in the browser UI and stored in localStorage. NASA calls use the hardcoded `DEMO_KEY`.
