# Setup Guide

## Prerequisites
- An [InfinityFree](https://infinityfree.net/) hosting account
- A Serper API key (for search features)
- A Groq API key (for AI features)
- *(Optional)* A Discord webhook URL for notifications

## Steps

### 1. Configure credentials
Copy the example config file and fill in your details:

```bash
cp api/config.php.example api/config.php
```

Then open `api/config.php` and replace every `REPLACE_WITH_…` placeholder with your real values:

| Constant | Where to find it |
|---|---|
| `DB_HOST` | InfinityFree Control Panel → MySQL Databases |
| `DB_NAME` | InfinityFree Control Panel → MySQL Databases |
| `DB_USER` | InfinityFree Control Panel → MySQL Databases |
| `DB_PASS` | InfinityFree Control Panel → MySQL Databases |
| `SERPER_KEY` | [serper.dev](https://serper.dev/) dashboard |
| `GROQ_KEY` | [console.groq.com](https://console.groq.com/) |
| `DISCORD_WEBHOOK` | Discord channel settings → Integrations → Webhooks (leave `""` to disable) |
| `ADMIN_PASSWORD` | Choose a strong password for the admin panel |

### 2. Upload to InfinityFree
Upload all project files to your InfinityFree hosting via FTP or the File Manager in the control panel.

### 3. First run / database setup
The application will automatically create the required database tables the first time it detects they are missing.

## Security

> **Important:** Do **not** push `api/config.php` to GitHub — it contains your real credentials.  
> It is already listed in `.gitignore` to prevent accidental commits.  
> Only commit `api/config.php.example` (which contains placeholder values).
