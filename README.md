# Link Dedup & Batcher — Telegram Bot

x.com লিংক deduplicate ও batch করার Telegram bot।

## Features

- x.com status link extract করে (bare `x.com/...` সহ)
- Duplicate link বাদ দেয় (status ID দিয়ে match করে)
- ৫টা করে batch করে আলাদা message এ পাঠায়
- Reaction দিলে batch message delete হয়ে যায়

## Deploy on Render (Free Tier — Web Service)

1. **+ New → Web Service** select করো
2. GitHub repo connect করো (`Uzzol19kholifa/Link-organizer`)
3. Runtime: **Docker** select করো
4. Instance Type: **Free** select করো
5. Environment variable add করো: `BOT_TOKEN` = তোমার Telegram bot token
6. **Create Web Service** click করো — Deploy!

## Local Development

```bash
pip install -r requirements.txt
BOT_TOKEN=your_token python link_dedup_bot.py
```

## Commands

| Command | Description |
|---------|-------------|
| `/start` | Welcome message |
| `/help` | ব্যবহার বিধি |
| (text with links) | Dedup + batch reply |
