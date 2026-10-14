# Discord Product Management Bot

A lightweight Discord bot written in Python (`discord.py` and `SQLite`) designed for managing, validating, and tracking product links via Slash Commands.

*Note: This codebase was generated with AI assistance.*

## Features

- **Slash Commands & Autocomplete**: Built-in search, listing, and management commands with fuzzy matching (`difflib`) for product queries.
- **Database Backend**: SQLite storage utilizing WAL mode, connection context managers, and automated schema migrations.
- **Security**: URL sanitization with basic SSRF protection (blocking private/reserved IP addresses) and LIKE-injection mitigation.
- **Audit Logging**: Tracks administrative actions (additions, updates, deletions, and imports).
- **Import/Export**: Supports exporting and importing data across `.xlsx`, `.csv`, `.json`, and raw `.db` formats.
- **Link Health Checker**: Background asynchronous task (`aiohttp`) that checks database links for availability and reports broken endpoints.

## Requirements

- Python 3.10+
- `discord.py`
- `python-dotenv`
- `aiohttp`
- `openpyxl` (optional, for Excel exports)

## Installation & Configuration

1. Clone the repository and install dependencies:
```bash
pip install -r requirements.txt

2. Create a .env file in the root directory based on this structure:
DISCORD_TOKEN=your_bot_token
WEBHOOK_URL=your_webhook_url
GUILD_ID=your_discord_guild_id
ADMIN_CHANNEL_ID=your_admin_channel_id
STATUS_CHANNEL_ID=your_status_channel_id
DB_PATH=database.db

3. Run the bot:
python bot.py

License
This project is licensed under the MIT License. See the LICENSE file for details.