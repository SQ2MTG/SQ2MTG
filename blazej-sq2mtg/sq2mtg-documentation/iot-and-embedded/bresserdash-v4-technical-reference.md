# BresserDash v4 — Technical Reference

## Purpose

BresserDash-v4 is a lightweight static HTML/JavaScript dashboard for visualizing weather data from a Bresser 5-in-1 weather station decoded by `rtl_433`.

The documented input is JSON/NDJSON produced by `rtl_433`.

## Data Flow

```
Bresser 5-in-1
      |
      v
   RTL-SDR
      |
      v
   rtl_433
      |
      +--> JSON / NDJSON
                |
                v
         BresserDash-v4
                |
                +--> current metrics
                +--> history
                +--> charts
```

## Documented Metrics

The dashboard is intended to visualize:

* temperature,
* humidity,
* wind,
* rainfall,
* dew point,
* signal level,
* battery state.

The project README also mentions wind-rose visualization and metric cards.

## History

The README documents:

* browser `localStorage`,
* optional `history.json`,
* current/latest-record input and historical data.

## Deployment

Because the application is a static frontend, the README identifies generic static hosting options such as GitHub Pages, Netlify and Vercel.

A simple HTTP server can also be used during local testing.

## RTL-SDR Input

The README documents examples such as:

```bash
rtl_433 -F json
rtl_433 -F json >> /path/to/history.json
rtl_433 -F json | tee -a /path/to/history.json
```

The exact expected JSON fields and endpoint/file naming should be verified against the current frontend source before integrating a new telemetry producer.

## Verification Status

README inspected on 2026-09-28. The documented architecture and supported data flow are verified; exact JavaScript parsing rules and metric field mappings require source inspection.
