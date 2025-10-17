# Storage and Collaboration

## Overview

File storage and collaboration platform for hosting, sharing, and syncing files across devices.

## Recommended: Nextcloud

- **File management**: Upload, organize, and share files
- **Sync clients**: Desktop and mobile apps for seamless sync
- **Collaboration**: File sharing, comments, and permissions
- **Calendar & Contacts**: Built-in CalDAV and CardDAV
- **Office integration**: Edit documents directly in Nextcloud
- **Extensible**: 200+ apps for additional features

## Features

- Self-hosted, privacy-focused file storage
- End-to-end encryption options
- Version control and file recovery
- Activity feeds and notifications
- Group folders and team spaces
- External storage support (S3, SFTP, etc.)

## Setup

### Docker Compose Example

```yaml
nextcloud:
  image: nextcloud:latest
  ports:
    - "8081:80"
  volumes:
    - ./tools/storage_collab/data:/var/www/html
  environment:
    - NEXTCLOUD_ADMIN_USER=${NEXTCLOUD_ADMIN_USER}
    - NEXTCLOUD_ADMIN_PASSWORD=${NEXTCLOUD_ADMIN_PASSWORD}
  restart: unless-stopped

nextcloud-db:
  image: postgres:15
  environment:
    - POSTGRES_DB=nextcloud
    - POSTGRES_USER=${POSTGRES_USER}
    - POSTGRES_PASSWORD=${POSTGRES_PASSWORD}
  volumes:
    - ./tools/storage_collab/db:/var/lib/postgresql/data
  restart: unless-stopped
```

## Usage

1. Access Nextcloud at `http://localhost:8081`
2. Complete the initial setup wizard
3. Install recommended apps (Calendar, Contacts, Talk, OnlyOffice)
4. Download sync clients for your devices

## Integration

- **Office suite**: Integrate with OnlyOffice or Collabora for document editing
- **Email**: Connect email accounts for attachment management
- **Calendar**: Sync with calendar apps via CalDAV
- **Automation**: Use n8n to automate file operations

## Resources

- [Nextcloud Documentation](https://docs.nextcloud.com/)
- [Nextcloud Apps](https://apps.nextcloud.com/)
- [Admin Manual](https://docs.nextcloud.com/server/latest/admin_manual/)
