# Shorts Discord Bridge — Technical Reference

## Runtime flow

```
YouTube channel
      |
      v
YouTube Data API v3
      |
      v
5-minute polling
      |
      v
Shorts detection
      |
      v
Discord bot
      |
      v
Configured Discord thread
```

## Dependencies

The README explicitly names:

```
discord.py
google-api-python-client
```

## Configuration contract

| Variable          | Purpose                    |
| ----------------- | -------------------------- |
| `DISCORD_TOKEN`   | Discord bot authentication |
| `YOUTUBE_API_KEY` | YouTube Data API access    |
| `CHANNEL_ID`      | Source channel             |
| `THREAD_ID`       | Discord destination        |

Credentials should be supplied through the environment or another secret store.

## Polling model

The documented implementation checks every 300 seconds. This is simple but introduces detection latency and consumes API quota. Any change to the interval should account for YouTube API quota limits.

## Operational boundary

The repository is archived. Exact API request parameters, Shorts filtering logic, Discord permissions/intents and message formatting should be source-verified before modernization.
