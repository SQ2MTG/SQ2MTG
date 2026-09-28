# LoRa Tracker — Technical Reference

## Hardware

SQ2MTG/lora\_tracker is a compact universal ESP32 development board for LoRa modem prototyping.

The README explicitly documents support for **RA-01** and **E22-400M30S** modules. It also supports two ESP32 DevKit variants with different pinouts; the selected pinout is configured through solder pads.

## Firmware target

The board is intended for firmware such as sh123/esp32\_loraprs or other compatible firmware. This repository itself documents the hardware rather than a complete tracker firmware stack.

## Documentation assets

The README references board and assembled-device images. The repository hardware files should be treated as authoritative for:

* schematic and PCB revision;
* exact solder-pad configuration;
* ESP32 DevKit pin mapping;
* module power and signal connections;
* mechanical dimensions and assembly constraints.

## Integration boundary

Firmware-specific behavior, APRS packet handling and radio parameters are not defined by the README and should not be inferred from the board alone.

## Source

Repository: SQ2MTG/lora\_tracker
