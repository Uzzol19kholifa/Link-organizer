# Link Dedup & Batcher — Telegram Bot

x.com লিংক deduplicate ও batch করার Telegram bot।

## Features

- x.com status link extract করে (bare `x.com/...` সহ)
- Duplicate link বাদ দেয় (status ID দিয়ে match করে)
- ৫টা করে batch করে আলাদা message এ পাঠায়
- Reaction দিলে batch message delete হয়ে যায়

## Deploy on Render

### 1. Blueprint (recommended)

1. GitHub এ এই repo connect করো Render এ
2. **New → Blueprint** select করো — `render.yaml` automatically detect হবে
3. `BOT_TOKEN` environment variable set করো (Render dashboard → Environment)
4. Deploy!

### 2. Manual

1. **New → Background Worker** → Docker select করো
2. Repository connect করো
3. Environment variable add করো: `BOT_TOKEN` = তোমার Telegram bot token
4. Deploy!

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
