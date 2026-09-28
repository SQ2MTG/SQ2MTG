# Shorts Discord Bridge

Python Discord bot that monitors a selected YouTube channel and forwards newly detected Shorts to a Discord thread/channel.

## Stack

* Python
* discord.py
* Google API client
* YouTube Data API v3
* Discord bot API

## Configuration

The documented configuration consists of:

* `DISCORD_TOKEN` — Discord bot token;
* `YOUTUBE_API_KEY` — YouTube Data API key;
* `CHANNEL_ID` — monitored YouTube channel;
* `THREAD_ID` — destination Discord thread.

Never commit these values to source control.

## Polling

The README documents a 300-second polling interval. The bot checks for new Shorts and sends a message to the configured Discord destination.

## Run

```bash
pip install discord.py google-api-python-client
python bot.py
```

## Status

The repository is archived/historical. Treat the documented API workflow as a reference and verify current Discord/YouTube API requirements before deployment.
