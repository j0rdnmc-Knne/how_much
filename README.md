# quotehub
A community quote sharing platform built with FastAPI

## Tech Stack
- Python
- FastAPI
- SQLite
- SQLModel

## Features
- Collaborative quote database
- Category tagging and organization
- Moderation system with admin approval
- Infinite scroll pagination
- Community voting and ratings

## Quick Start
Designed for easy deployment on Railway. Also runs locally with minimal setup.

First, configure the application settings (`settings.toml`). `SITE_NAME` appears in browser tabs, while `BRAND_NAME` displays in the site header.

`SECRET_KEY` secures session cookies - generate a strong random string. `MODERATOR_KEY` grants permissions for quote approval and management. No user accounts required for basic functionality.

`WELCOME_MESSAGE` shows on the homepage.

`SITE_NAME` and `BRAND_NAME` can be set via environment variables if left empty in config.

QuoteHub uses SQLite by default. For production, set `DATABASE_URL` to your PostgreSQL connection string. Railway automatically handles this - manual setup only needed for local development.

After configuration, start the server:

```
uvicorn main:app --reload
```

The application checks for `RAILWAY_ENVIRONMENT`; when set to 'production', it runs in optimized mode with debug disabled. The `PORT` environment variable is required and auto-configured on Railway.

First launch initializes the database and creates necessary tables. The application is then ready for use.

All application logs output to stdout, captured by Railway's logging system.

## Interface Preview
![Homepage](http://i.imgur.com/VA4NGw4.png)

![Browse Quotes](http://i.imgur.com/rlyz1Wa.png)

![Categories](http://i.imgur.com/1tMgKkF.png)

![Submit Quote](http://i.imgur.com/BRMsBrU.png)

# PR Merge: 2025-12-01 12:16:44
