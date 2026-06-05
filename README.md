# Scarface Discord Join Scraper

Self-bot join tracker for **zee_co2** — all servers that account is in. Forwards captures to **Scarface Auto save** group DM.

## Quick config (`.env`)

```env
USER_TOKEN=          # zee_co2 token — never commit
CHAT_ID=1511500822872195195
CLIENT_NAME=Scarface
CAPTURE_MODE=all
DISPLAY_TIMEZONE=Africa/Lagos
DEBUG=false
TEST_CAPTURE=false
SEND_STARTUP_PING=true
```

## Local run

```powershell
cd C:\Users\HP\Downloads\scraper-scarface
pip install -r requirements.txt
python bot.py
```

Run **one** instance per token (local **or** Render, not both).

## Push to GitHub

```powershell
cd C:\Users\HP\Downloads\scraper-scarface
git init
git add bot.py requirements.txt README.md .env.example .gitignore render.yaml runtime.txt
git commit -m "Scarface join tracker for zee_co2"
git branch -M main
git remote add origin https://github.com/okwujiaku/scraper-scarface.git
git push -u origin main
```

Create the empty repo `scraper-scarface` on GitHub first if it does not exist.

## Render

1. **New → Background Worker** → connect `okwujiaku/scraper-scarface`
2. Build: `pip install -r requirements.txt` · Start: `python bot.py`
3. Set env vars (see `render.yaml`) — add **`USER_TOKEN`** in dashboard
4. Ensure `PYTHON_VERSION=3.11.9` and `DISPLAY_TIMEZONE=Africa/Lagos`

Self-botting violates Discord ToS; use at your own risk.
