# MiniSmartTracker

**Repository:** `SQ2MTG/MiniSmartTracker`\
**Project domain:** APRS / GPS / embedded radio tracker.

## Purpose

MiniSmartTracker is an APRS tracker project intended for mobile/portable operation. The documented firmware architecture combines GPS position reporting with **SmartBeaconing** and telemetry.

## Main functions

The source documentation identifies:

* GPS position acquisition;
* APRS packet generation;
* SmartBeaconing-based transmission timing;
* temperature telemetry;
* supply-voltage telemetry;
* QAPRS / TinyGPS++-related firmware components;
* configurable parameters in `config.h`.

## Hardware / firmware boundary

The exact MCU, GPS wiring and radio interface must be taken from the source revision being built. The GitBook documentation avoids inventing a hardware variant where the repository does not establish it clearly.

## Technical reference

See **MiniSmartTracker — Technical Reference** for the documented firmware and configuration details.
