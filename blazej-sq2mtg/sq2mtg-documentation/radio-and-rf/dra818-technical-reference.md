# DRA818 — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/dra818`
* Public fork of `darksidelemm/dra818`
* Default branch: `master`
* License metadata: GPL-3.0
* Repository snapshot is historical; last push is from 2017.
* Description: DRA818U/V Radio Module Arduino Library.

## Project scope

Arduino library for controlling DRA818U/V radio modules. The fork should be treated as a historical snapshot; the upstream project remains the primary reference for changes after the fork.

## Integration model

The library is intended to provide a microcontroller-side interface to DRA818 radio modules. The repository documentation establishes the module/library relationship, while exact serial commands, configuration fields, timing, supported module variants and API calls should be verified against the source before implementation.

## Hardware considerations

DRA818 modules use low-voltage digital interfaces. Verify logic-level compatibility between the MCU and module before wiring TX/RX or control signals. Do not assume that a 5 V MCU can be connected directly to every module signal.

## Maintenance

For new designs, compare this fork against the upstream repository and verify the exact Arduino API and hardware requirements from the current source. This page deliberately avoids presenting unverified pinouts or command tables as current facts.
