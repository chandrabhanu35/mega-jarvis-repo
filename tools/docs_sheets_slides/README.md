# Documents, Sheets, and Slides

## Overview

Office suite integration for creating and editing documents, spreadsheets, and presentations locally.

## Options

### LibreOffice
- Full-featured office suite
- Compatible with Microsoft Office formats
- Writer, Calc, Impress, and more

### OnlyOffice
- Modern web-based office suite
- Real-time collaboration
- Microsoft Office compatible
- Document Server for integration

### ONLYOFFICE Docs
- Self-hosted document collaboration
- Integration with file storage services
- Mobile support

## Setup

Choose your preferred office suite and add the service to `docker-compose.yml`.

### Example: OnlyOffice Document Server

```yaml
office_suite:
  image: onlyoffice/documentserver:latest
  ports:
    - "8080:80"
  volumes:
    - ./tools/docs_sheets_slides/data:/var/www/onlyoffice/Data
    - ./tools/docs_sheets_slides/logs:/var/log/onlyoffice
  restart: unless-stopped
```

## Integration

- Integrate with Nextcloud for seamless document editing
- Connect with automation workflows for document processing
- API access for programmatic document generation

## Resources

- [LibreOffice Documentation](https://documentation.libreoffice.org/)
- [OnlyOffice Documentation](https://helpcenter.onlyoffice.com/)
- [ONLYOFFICE Docs](https://github.com/ONLYOFFICE/DocumentServer)
