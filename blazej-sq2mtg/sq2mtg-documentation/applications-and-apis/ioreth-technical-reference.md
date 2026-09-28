# Ioreth — technical reference

## Purpose

Ioreth is described by its upstream README as a very experimental APRS bot. The SQ2MTG repository is a fork of `ittner/ioreth`.

## Domain

The repository is associated with:

* APRS
* AX.25
* amateur radio
* APRS-IS
* Python

The README explicitly warns that transmitting on amateur-radio APRS bands requires the appropriate amateur-radio authorization and compliance with local regulations. It also notes regulatory implications of connecting to APRS-IS as a mechanism for operating remote transmitters.

## License and provenance

The upstream project is GNU GPLv3-or-later. The SQ2MTG fork retains that declared license metadata.

The fork is an older snapshot, so current upstream behavior should be checked before relying on it for deployment.

## Documentation boundary

The upstream README itself calls the project very experimental and notes that documentation is incomplete. Exact client-library APIs, bot-server behavior, AX.25/APRS packet handling, configuration, network endpoints, and runtime dependencies require direct source inspection.

No credentials or operational radio configuration are reproduced here.
