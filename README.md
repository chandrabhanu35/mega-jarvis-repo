# Mega Jarvis — Local AI Productivity OS

Mega Jarvis is a unified, open-source productivity suite designed to replicate and extend Google Workspace locally — powered by AI (Ollama/Open WebUI) and fully customizable for personal or team workflows.

## Key goals

- Run essential productivity apps 100% locally and privately.
- Full AI integration for chat, automation, and smart features.
- Modular design: each tool lives in its own folder under /tools.
- Workflow automation via n8n and Node-RED connecting docs, spreadsheets, email, chat, storage.

## Quickstart (developer)

1. Fork or clone the repo.
2. Copy `env.example` to `.env` and edit values.
3. Start services: `docker compose up -d`
4. Edit or add tools under `/tools`. Each tool is a standalone folder with a README and compose snippet.

## Repository layout

- /tools
  - /docs_sheets_slides # e.g., LibreOffice / OnlyOffice integration
  - /storage_collab # e.g., Nextcloud
  - /email # e.g., Mailu, Maddy
  - /chat_meet # e.g., Mattermost, Rocket.Chat, Jitsi Meet
  - /ai_assistant # Open WebUI + Ollama models and adapters
  - /automation # n8n & Node-RED
  - README.md # tool folder guidelines
- docker-compose.yml # unified stack launcher
- env.example # environment template

## Contributing

- Follow the modular approach: add or edit services under /tools and include a README and (optional) Dockerfile.
- Open issues describing the feature or bug; label and link them to PRs.
- If you want me to create or update files in the repo, tell me which repo and I can push a branch and open a PR.

## Security & privacy

- The stack is designed to run locally; treat exposed network ports, firewall, and domain setup carefully.
- Use secure passwords/keys and restrict external access where appropriate.

## License

- Add a license file or tell me which license you prefer (MIT, Apache-2.0, GPL-3.0, etc.).
