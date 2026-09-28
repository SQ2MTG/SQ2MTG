# AutoWX2 — Technical Reference

## Repository

* Repository: `SQ2MTG/autowx2`
* Fork of `filipsPL/autowx2`
* Default branch: `master`
* Historical SDR/satellite automation project

## Purpose

AutoWX2 is a modular collection of programs and scripts for scheduling SDR recordings of satellite and ground transmissions.

Documented use cases include:

* NOAA weather-satellite APT,
* METEOR-M2,
* ISS voice transmissions,
* ISS SSTV,
* Fox-1B,
* fixed-time FM recordings,
* radiosonde observations,
* APRS decoding/iGate operation,
* ADS-B with `dump1090`.

The project uses separate modules/plugins for recording and processing different transmission types.

## Architecture

The main scheduler is:

```
autowx2.py
   |
   +--> autowx2_conf.py
   |
   +--> scheduled modules
          +--> NOAA
          +--> ISS
          +--> METEOR-M2
          +--> radiosonde
          +--> FM
          +--> other scripts
```

The README emphasizes modularity and configurable scheduling.

## Scheduling

Satellite recordings can be triggered from pass predictions. Fixed-time recordings can use cron-style schedules.

The configuration includes concepts such as:

* satellite name,
* receive frequency,
* processing module,
* recording priority,
* fixed recording time,
* fixed duration.

Lower priority numbers are documented as higher priority when recordings overlap.

## SDR / Hardware

Documented hardware is based on USB DVB-T/RTL-SDR dongles such as RTL2832-based devices and a suitable antenna.

The historical installation notes include Linux udev configuration and blacklisting the DVB USB kernel module.

The README warns that the bundled installation script should be inspected and adapted before execution.

## Modules

Documented modules include:

* `modules/noaa` — recording and processing NOAA APT.
* `modules/iss` — voice/IQ/WAV/MP3 recording.
* `modules/meteor-m2` — METEOR-M2 processing.
* `modules/radiosonde` — radiosonde monitoring.
* `modules/fm` — FM recording.

Auxiliary scripts cover APRS decoding, iGate operation, SDR calibration, Kepler/TLE updates and transit-plan generation.

## Web Interface

The project contains a Flask web interface. The README documents a default local endpoint on port `5010`, with the port configurable through the project configuration.

Static pages can also be generated from module output and served from the configured web directory.

## Installation / Operations

The documented workflow is:

1. obtain the source;
2. inspect and adapt `install.sh`;
3. install dependencies;
4. edit `autowx2_conf.py`;
5. schedule TLE/Kepler updates;
6. run `autowx2.py`.

This project is historical. Modern RTL-SDR drivers, Python packages, WxtoImg availability and satellite-processing dependencies should be verified before deployment.

## Security / Operational Notes

* Treat `install.sh` as privileged system-changing code and inspect it before execution.
* Run the scheduler with only the permissions it needs.
* Do not expose the Flask interface publicly without access controls.
* Keep external API/service credentials out of configuration committed to Git.

## Verification Status

README inspected on 2026-09-28. Exact module command lines and current dependency compatibility should be verified against the fork and upstream repository before a new deployment.
