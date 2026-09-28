# WxUno — Technical Reference

## Repository

* Repository: `SQ2MTG/WxUno`
* Public fork
* Default branch: `master`
* Historical Arduino weather-station project

## Purpose

WxUno is an Arduino UNO weather station that reports weather data to APRS/CWOP.

The repository README is concise and does not define the complete sensor, network or packet implementation.

## Historical Project Context

The project should be treated as a legacy embedded weather-telemetry implementation.

Before rebuilding it, verify directly from source:

* sensors and their electrical interfaces,
* Arduino pin mapping,
* Ethernet/network hardware,
* APRS/CWOP packet construction,
* station configuration,
* update interval,
* required libraries,
* watchdog behavior.

## Verification Status

README inspected on 2026-09-28. Only the project purpose is directly established by the README; detailed implementation claims require source-level verification.
