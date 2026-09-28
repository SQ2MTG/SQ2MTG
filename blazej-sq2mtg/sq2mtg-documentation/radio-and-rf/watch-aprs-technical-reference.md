# Watch APRS — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/watch-aprs`
* Public fork of `trasukg/watch-aprs`
* Default branch: `master`
* License: Apache-2.0
* Fork is a historical snapshot; the upstream repository is the authoritative source for current development.
* Upstream description: command-line utility for monitoring APRS packets from a KISS-over-TCP source.

## Function

The project is a command-line APRS monitor. Its documented input transport is KISS over TCP, making it suitable for observing packet traffic from a compatible KISS/TCP source.

## APRS integration

The project belongs to the APRS/RF tooling layer. Exact CLI options, packet display format, TCP defaults and runtime dependencies should be taken from the source rather than inferred from the repository name.

## Maintenance

Because the SQ2MTG repository is a fork/snapshot, verify changes and current behavior against the upstream project before deployment.

## Operational considerations

Treat APRS input as untrusted network data. If the monitor is exposed beyond a trusted LAN/VPN, restrict the KISS/TCP listener path and avoid unnecessary network privileges.
