# Tools

This directory contains all modular tool integrations for Mega Jarvis.

## Structure

Each tool is self-contained in its own folder with:
- A `README.md` explaining what the tool does and how to configure it
- (Optional) A `Dockerfile` for custom builds
- (Optional) A `docker-compose.yml` snippet or config files

## Available Tools

### /ai_assistant
Open WebUI integration with Ollama for local AI models and chat interfaces.

### /automation
n8n and Node-RED workflow automation engines.

### /docs_sheets_slides
Office suite integration (LibreOffice, OnlyOffice, or ONLYOFFICE Docs).

### /storage_collab
Nextcloud or similar file storage and collaboration platform.

### /email
Local email server (Mailu, Maddy, or similar).

### /chat_meet
Team chat and video conferencing (Mattermost, Rocket.Chat, Jitsi Meet).

## Adding a New Tool

1. Create a new folder under `/tools` with a descriptive name
2. Add a `README.md` explaining the tool, its purpose, and setup instructions
3. (Optional) Add a `Dockerfile` or custom configs
4. Update the main `docker-compose.yml` with the service definition
5. Document any required environment variables in `env.example`

## Contributing

Contributions are welcome! Please ensure:
- Each tool has clear documentation
- Service names follow the existing convention
- Environment variables are properly documented
- Docker images are from official or well-maintained sources
