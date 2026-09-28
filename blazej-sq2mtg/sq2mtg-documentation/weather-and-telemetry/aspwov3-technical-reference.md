# ASPWOv3 — technical reference

## Purpose

ASPWOv3 (Automatyczna Stacja Pogodowa Wczesnego Ostrzegania) is a modular Raspberry Pi platform for collecting weather/environmental telemetry and generating Polish spoken radio announcements.

The documented pipeline is:

`cron/manual start → sr0wx.py → data modules → message sequence → local OGG playback → GPIO PTT → RF transmission → logging`.

## Runtime

* Python 3.9+
* Raspberry Pi OS Bookworm / Debian 12–13
* Raspberry Pi Zero WH / 3 / 4 / 5 class hardware
* Apache License 2.0

## RF and GPIO interface

The README documents:

* physical pin 32: PTT output, normally LOW, HIGH during transmission
* physical pin 33: buzzer/Roger Beep output
* PyGame for local OGG playback
* 1000 ms transmitter stabilization delay before playback
* 70 ms end-of-transmission buzzer pulse

These mappings are source-documentation facts and should be verified against the deployed hardware before wiring.

## Data modules

Documented modules include OpenWeatherMap, GIOS air quality, Radioactive@Home, Meteoalarm, local sunrise/sunset calculation, HF propagation data, and station activity-map telemetry.

The module architecture is based on the `SR0WXModule` contract.

## Audio generation

ASPWOv3 does not use cloud TTS during normal operation. It builds messages from prerecorded Polish `.ogg` phonetic/audio segments. Missing vocabulary falls back to `beep.ogg`.

## Installation

`configurator.sh` is a privileged provisioning script. The README states that it performs system update/package installation, builds WiringPi, registers watchdogs and restarts the SBC after a short delay.

Review the script before production execution because it modifies the operating system and hardware-facing configuration.

## Configuration and security

Station identity, coordinates, active modules and API configuration are stored in `config.py`. API credentials should be supplied as secrets and never committed to the repository.

The README contains only placeholder API-key material; no secret is reproduced here.
