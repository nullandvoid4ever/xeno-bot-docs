---
title: Configuration
description: Xeno Bot is configured via a YAML file (`config.yml`) placed at the project root or specified with `--config`.
tags:
  - config
  - setup
  - instructions
  - self-hosting
keywords:
  - xeno
  - bot
  - config
  - documentation
author: Devvyyxyz
image: assets/images/faq-og.png
date: 2026-03-04
permalink: /configuration/
toc: true
icon: material/server
aliases:
  - /config/
  - /configuration/
---

Xeno Bot is a scalable and customizable Discord bot built with `discord.js`. Configuration is managed through a mix of environment variables and JSON files. This guide will walk you through setting it up efficiently.

---

## Configuration Files

The bot relies on the following JSON configuration files:

### `config/config.json`
This file contains general bot settings, such as:
- The command prefix
- The owner's user ID

**Example**:
```json
{
  "prefix": "!",
  "owner": "YOUR_USER_ID"
}
```

!!! note
    Ensure you replace `"YOUR_USER_ID"` with your Discord user ID to enable owner-specific commands.

### `config/bot.public.json`
This file stores public bot metadata. The bot token is not stored here but is instead read from the `TOKEN` environment variable.

### `config/bot.dev.json`
This file is similar to `bot.public.json` but is used for the development profile. By default, the development bot reads the token from the `TOKEN_DEV` environment variable.

!!! warning
    Avoid committing sensitive values like bot tokens or user IDs to version control. Use `.gitignore` and secret management tools.

---

## Environment Variables

The **`.env` file** is critical for storing sensitive information and runtime configurations. Start by copying `.env.example` to `.env` and updating values accordingly.

### General Settings

```env
TOKEN=YOUR_BOT_TOKEN
CLIENT_ID=YOUR_BOT_CLIENT_ID
GUILD_ID=123456789012345678  # Optional for testing commands in a single guild
```

- **`TOKEN`**: Your bot's authentication token.
- **`CLIENT_ID`**: The client ID of your Discord bot.
- **`GUILD_ID`** *(Optional)*: A test guild where commands are registered immediately during development.

!!! note
    The `GUILD_ID` value allows faster development by limiting slash command updates to a single test server.

---

### Logging Settings

```env
LOG_LEVEL=info
```

- **`LOG_LEVEL`**: Adjusts logging verbosity. Acceptable values:
  - `info`: Displays informational messages (default).
  - `debug`: Shows detailed logs during development.
  - `warning`: Logs potential issues that may need attention.
  - `error`: Logs critical problems.

!!! note
    Use `LOG_LEVEL=debug` while debugging issues during development. Switch back to `info` in production environments.

---

### Database Configuration

```env
DATABASE_URL=postgres://user:password@host:port/database
DB_POOL_MAX=20
DB_POOL_MIN=2
```

- **`DATABASE_URL`**: The connection string for your Postgres database.
- **`DB_POOL_MAX`**: Sets the maximum number of database connections in the pool.
- **`DB_POOL_MIN`**: Configures the minimum number of idle database connections.

!!! tip
    For local development, Xeno Bot uses an SQLite database (`data/dev.sqlite`) by default. To use Postgres, set `DATABASE_URL`. The bot automatically migrates the database schema on startup.

---

### Rate Limiting

```env
RATE_LIMIT_ENABLED=true
RATE_LIMIT_GENERAL=10
RATE_LIMIT_EXPENSIVE=3
RATE_LIMIT_TRANSACTIONS=5
```

Rate limiting prevents spamming commands:
- **`RATE_LIMIT_ENABLED`**: Enables/disables rate limiting globally.
- **`RATE_LIMIT_GENERAL`**: Sets the limit for general commands (e.g., 10 commands every 10 seconds).
- **`RATE_LIMIT_EXPENSIVE`**: Limits commands with heavy computations (e.g., 3 commands every 10 seconds).
- **`RATE_LIMIT_TRANSACTIONS`**: Limits transaction-related commands (e.g., 5 commands every 30 seconds).

!!! important
    Consider adjusting rate limits based on your server's scale to maintain performance while preventing abuse.

---

### Optional Features

#### Telemetry (Crash Reporting)
```env
SENTRY_DSN=https://example@sentry.io/project-id
```
- **`SENTRY_DSN`** *(Optional)*: Enables [Sentry](https://sentry.io) integration for tracking errors and crashes.

!!! note
    Sentry is optional but highly recommended for monitoring production environments.

#### Caching
```env
CACHE_MAX_SIZE=10000
CACHE_DEFAULT_TTL=300000
```
- **`CACHE_MAX_SIZE`**: Maximum number of items that the bot can store in cache.
- **`CACHE_DEFAULT_TTL`**: Time-to-live for cached items, in milliseconds (e.g., 5 minutes).

#### Performance Monitoring
```env
LOG_PERFORMANCE=true
METRICS_INTERVAL=300000
```
- **`LOG_PERFORMANCE`**: Logs performance metrics when enabled.
- **`METRICS_INTERVAL`**: Specifies the interval (in ms) for logging performance metrics.

---

## Running Xeno Bot

### Development Mode

Use the following commands to test or deploy Xeno Bot:

- **Install Dependencies**:  
  ```bash
  npm install
  ```

- **Deploy Commands**:  
  ```bash
  npm run deploy-commands
  ```

- **Start the Bot in Development**:  
  ```bash
  npm run start:dev
  ```

!!! note
    This runs the bot in development mode, where commands are registered only in the test guild (if `GUILD_ID` is set).

### Production Mode

To run the bot in production:
```bash
npm start
```

---

## Example Configuration Setup

Here's an example `.env` file with all configurations in use:

```env
# Bot Settings
TOKEN=your-token-here
CLIENT_ID=your-client-id-here
GUILD_ID=your-guild-id-here

# Logging
LOG_LEVEL=info

# Database
DATABASE_URL=postgres://user:password@host:port/database
DB_POOL_MAX=20
DB_POOL_MIN=2

# Caching
CACHE_MAX_SIZE=10000
CACHE_DEFAULT_TTL=300000

# Rate Limiting
RATE_LIMIT_ENABLED=true
RATE_LIMIT_GENERAL=10
RATE_LIMIT_EXPENSIVE=5
RATE_LIMIT_TRANSACTIONS=8

# Monitoring & Telemetry
LOG_PERFORMANCE=true
METRICS_INTERVAL=300000
SENTRY_DSN=https://example@sentry.io/project-id
```