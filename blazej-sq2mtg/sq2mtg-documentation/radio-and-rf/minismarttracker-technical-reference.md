# MiniSmartTracker — Technical Reference

## Function

MiniSmartTracker is an APRS tracker implementing **SmartBeaconing**. The project is derived from a QAPRS-based tracker design and contains modifications to the original circuit.

## Firmware components

The README documents:

* Arduino/QAPRS heritage for APRS functionality;
* TinyGPS++ for GPS data processing;
* SmartBeaconing logic derived from stanleyseow/ArduinoTracker-MicroAPRS;
* temperature-sensor support;
* supply-voltage measurement.

The README attributes the temperature and voltage measurement functions to RA4FHE.

## Hardware documentation

The current schematic is referenced in the repository's pic directory. Exact MCU, radio/modem, GPS electrical interface and GPIO assignments should be taken from the repository schematic/source rather than inferred from the README.

## Configuration

Initial configuration is performed by editing config.h, specifically the section marked “User defined part”.

## Verification boundary

SmartBeaconing thresholds, packet formatting, serial interfaces, timing values and pin mappings are not fully specified in the README. They require direct source/schematic verification before being documented as fixed implementation details.

## Source

Repository: SQ2MTG/MiniSmartTracker
