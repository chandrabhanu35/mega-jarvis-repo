# Email

## Overview

Self-hosted email server for managing email accounts, sending/receiving messages, and email automation.

## Options

### Mailu
- Complete email server solution
- Web admin interface
- Webmail client included
- Anti-spam and anti-virus
- Easy Docker deployment

### Maddy
- Modern, lightweight email server
- Simple configuration
- SMTP and IMAP support
- Built-in filtering

### Mailcow
- Full-featured mail server suite
- SOGo webmail
- Comprehensive admin panel
- Advanced security features

## Features

- **Multiple domains**: Host email for multiple domains
- **Webmail**: Access email through web interface
- **SMTP/IMAP**: Standard email protocols
- **Anti-spam**: Built-in spam filtering
- **Anti-virus**: Email scanning for malware
- **Aliases**: Email forwarding and aliases
- **Auto-responders**: Out-of-office replies

## Setup

### Example: Mailu

```yaml
email:
  image: mailu/admin:latest
  ports:
    - "25:25"    # SMTP
    - "143:143"  # IMAP
    - "587:587"  # Submission
    - "993:993"  # IMAPS
  volumes:
    - ./tools/email/data:/data
    - ./tools/email/mail:/mail
  environment:
    - DOMAIN=${DOMAIN}
    - HOSTNAMES=${EMAIL_HOSTNAMES}
    - SECRET_KEY=${EMAIL_SECRET_KEY}
  restart: unless-stopped
```

## Configuration

1. Set your domain name in `.env`
2. Generate a secret key for encryption
3. Configure DNS records (MX, SPF, DKIM, DMARC)
4. Create email accounts through admin interface

## DNS Requirements

- **MX record**: Points to your mail server
- **SPF**: Sender Policy Framework
- **DKIM**: DomainKeys Identified Mail
- **DMARC**: Domain-based Message Authentication

## Integration

- **Automation**: Connect with n8n for email workflows
- **Contacts**: Sync with Nextcloud contacts
- **Calendar**: Email invites and reminders
- **AI Assistant**: AI-powered email responses

## Resources

- [Mailu Documentation](https://mailu.io/)
- [Maddy Documentation](https://maddy.email/)
- [Mailcow Documentation](https://mailcow.email/)
