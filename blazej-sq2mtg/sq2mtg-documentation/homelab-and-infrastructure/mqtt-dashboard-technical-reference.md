# MQTT Dashboard — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/MQTT-Dashboard`
* Public JavaScript repository
* Default branch: `main`
* License: MIT
* Repository is archived
* Description: Dashboard & Pushover API

## Function

Historical web dashboard project combining MQTT-oriented monitoring with a Pushover API integration.

Because GitHub marks the repository as archived, treat it primarily as a reference/snapshot rather than an actively maintained application.

## Integration

The documented project scope connects:

* MQTT telemetry
* browser/dashboard presentation
* Pushover notification delivery

Exact MQTT topic names, payload formats, broker configuration, API endpoints and frontend behavior require direct source inspection.

## Maintenance

Do not assume historical dependencies remain current. Before deployment, review package versions, browser APIs, MQTT connectivity and Pushover credentials.

## Security

Pushover tokens and other notification credentials must remain outside source control. Restrict MQTT broker access to the required LAN/VPN boundary.
