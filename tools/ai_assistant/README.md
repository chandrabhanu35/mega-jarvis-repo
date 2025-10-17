# AI Assistant

## Overview

This tool provides local AI capabilities using Open WebUI integrated with Ollama models.

## Features

- **Local LLM hosting**: Run models like Llama, Mistral, CodeLlama, etc. entirely offline
- **Chat interface**: Web-based UI for interacting with AI models
- **Multi-model support**: Switch between different models based on your needs
- **API access**: REST API for programmatic access to AI capabilities
- **Privacy-first**: All data stays on your machine

## Setup

1. Ensure the service is defined in the main `docker-compose.yml`
2. Create the required directories:
   ```bash
   mkdir -p tools/ai_assistant/models
   mkdir -p tools/ai_assistant/config
   ```
3. Pull desired Ollama models (after starting the service):
   ```bash
   docker exec -it <container-name> ollama pull llama2
   ```
4. Access the UI at `http://localhost:3000`

## Configuration

- **TZ**: Timezone setting (default: UTC)
- **MODEL_PATH**: Directory for storing AI models
- Models are stored in `./tools/ai_assistant/models`
- Configuration persists in `./tools/ai_assistant/config`

## Usage

1. Open the web interface at `http://localhost:3000`
2. Select or pull a model
3. Start chatting with your local AI assistant
4. Use the API for automation and integrations

## Integration

This service can be integrated with:
- n8n workflows for AI-powered automation
- Document processing pipelines
- Custom scripts via the REST API

## Resources

- [Open WebUI Documentation](https://docs.openwebui.com/)
- [Ollama Models](https://ollama.ai/library)
- [API Reference](https://github.com/open-webui/open-webui)
