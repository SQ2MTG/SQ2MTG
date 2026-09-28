# MQTT Sentinel — Technical Reference

## Purpose

MQTT Sentinel is a web dashboard for monitoring MQTT data in real time, exploring discovered topics and creating threshold/missing-data alarms. Alarm notifications can be sent through Pushover.

## Architecture

The current repository implements a React/TypeScript/Vite frontend and a Node.js/Express backend. MQTT.js receives broker messages; Socket.IO transports real-time updates to the browser; `better-sqlite3` provides local persistent storage.

The README documents an architecture in which the MQTT client subscribes to `#`, stores/processes messages through the Express alarm engine and emits real-time events through Socket.IO.

## Features

* real-time MQTT message feed;
* hierarchical topic explorer;
* historical charts for configurable time ranges;
* alarms for values above, below or equal to thresholds;
* alarms for missing data;
* Pushover notifications;
* local SQLite persistence with WAL mode;
* responsive React/Tailwind UI.

## Deployment

Docker Compose exposes the dashboard on port `3000` and persists application data under `./data`. The Compose configuration expects an MQTT broker service and environment variables for MQTT and optional Pushover credentials.

Local development uses:

```bash
npm install
npm run dev
```

The package manifest defines `tsx server.ts` as the development entry point and Vite for the production frontend build.

## Security

MQTT credentials and Pushover credentials must be supplied through environment configuration and must not be copied into documentation or committed to source control. Restrict broker access to the required LAN/VPN scope and protect the dashboard if it is reachable beyond a trusted network.

## Source

Repository: SQ2MTG/mqtt-sentinel
