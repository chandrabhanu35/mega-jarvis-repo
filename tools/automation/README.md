# Automation

## Overview

Workflow automation services using n8n and Node-RED for connecting tools and building custom workflows.

## Features

- **Visual workflow builder**: Drag-and-drop interface for creating automation
- **Pre-built integrations**: Connect with hundreds of services and APIs
- **Custom nodes**: Create your own integrations
- **Scheduling**: Trigger workflows on schedules or events
- **Data transformation**: Process and transform data between services

## Included Services

### n8n
- Modern workflow automation platform
- 200+ integrations
- Self-hosted and privacy-focused
- Access at `http://localhost:5678`

### Node-RED (optional)
- Flow-based programming for IoT and automation
- Visual wiring of devices and APIs
- Extensive node library

## Setup

1. Services are defined in the main `docker-compose.yml`
2. Create the data directory:
   ```bash
   mkdir -p tools/automation/n8n
   ```
3. Set credentials in `.env`:
   ```
   N8N_BASIC_AUTH_ACTIVE=true
   N8N_USER=your_username
   N8N_PASSWORD=your_password
   ```
4. Access n8n at `http://localhost:5678`

## Use Cases

- **Email automation**: Auto-respond, filter, and organize emails
- **Document processing**: OCR, conversion, and organization
- **AI integration**: Connect AI assistant with other tools
- **Notifications**: Send alerts based on events
- **Data sync**: Keep data synchronized across services
- **Backup automation**: Scheduled backups of important data

## Example Workflows

1. **AI-powered email assistant**: Process incoming emails with AI and auto-respond
2. **Document pipeline**: Convert uploaded documents and store in Nextcloud
3. **Meeting scheduler**: Integrate calendar with video conferencing
4. **Monitoring**: Track system health and send notifications

## Resources

- [n8n Documentation](https://docs.n8n.io/)
- [n8n Templates](https://n8n.io/workflows/)
- [Node-RED Documentation](https://nodered.org/docs/)
