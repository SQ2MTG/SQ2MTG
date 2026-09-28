# RadiationBase — technical reference

## Purpose

RadiationBase / PAA Radiation Portal is a full-stack application for visualizing environmental gamma-radiation measurements in Poland.

## Architecture

Documented stack:

* React 19 frontend
* Vite 6
* Tailwind CSS 4
* Leaflet / React Leaflet
* Motion
* Node.js + Express backend
* MQTT.js
* in-memory aggregation
* TypeScript/esbuild

The frontend polls the backend every 10 seconds and renders a geographic station map plus current measurements.

## MQTT ingestion

The README documents subscriptions to:

* `soloz/promieniowanie/imgw/#`
* `soloz/promieniowanie/pms/#`

The backend parses values such as `0.082 µSv/h` into numeric values and exposes them through `/api/radiation/data`.

The README documents an MQTT broker endpoint used by the project. Treat broker credentials and network access as deployment configuration rather than documentation constants.

## API/data model

The documented output groups stations under `imgw` and `pms`, with station name, numeric value, timestamp and source.

## Map handling

Stations with overlapping coordinates are visually separated using a golden-angle spiral offset. This is a presentation-layer technique and does not modify the underlying station coordinates.

## Deployment

The documented development workflow uses Node.js 20+, `npm install`, environment variables and `npm run dev`. Production uses the compiled frontend/server artifacts.

## Security

The project uses environment variables for MQTT and other service configuration. MQTT credentials and API keys must stay outside source control. If the dashboard is exposed outside a trusted network, protect the backend and restrict MQTT access.
