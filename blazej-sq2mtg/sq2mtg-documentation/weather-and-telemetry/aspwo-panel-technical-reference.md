# ASPWO Panel — technical reference

## Purpose

ASPWO Panel is a Flask-based real-time web dashboard for the SR5WXW station. It monitors local hardware, external service reachability and selected ASPWO logs.

## Stack

* Python
* Flask
* psutil
* HTML5/CSS3
* vanilla JavaScript
* DS18B20/1-Wire sensor support
* Linux `ping` utility

## Data flow

The browser polls Flask endpoints for JSON data. The backend reads local hardware metrics, performs ICMP checks against configured services and parses the ASPWO log file.

Documented refresh intervals:

* system statistics and logs: 3 seconds
* external service checks: 10 seconds

## API

The README documents:

| Endpoint       | Method | Purpose                         |
| -------------- | ------ | ------------------------------- |
| `/api/stats`   | GET    | temperatures, RAM and disk      |
| `/api/servers` | GET    | external service status/latency |
| `/api/log`     | GET    | most recent relevant log block  |

The default HTTP port is 80; a non-privileged port such as 8080 can be configured in the backend.

## Monitored services

The documented defaults include SOLOZ, the ASPWO node, Onet Pogoda, OpenWeatherMap, IMGW-PIB, PAA, Airly and GIOS air quality services.

## Hardware

The panel can read DS18B20 through Linux 1-Wire. The sensor identifier is installation-specific and must be configured accordingly.

## Operational security

The application is intended for station infrastructure. If exposed beyond a trusted LAN/VPN, add appropriate authentication and network controls. The log endpoint can expose operational information and should not be publicly reachable without review.
