# RFID Projects — Technical Reference

## ESP-RFID

The `esp-rfid` repository is an ESP-based RFID project with:

* firmware source;
* prebuilt firmware binaries;
* `esptool` flashing utility;
* Windows batch scripts for flashing and erasing;
* changelog and project documentation.

The repository is therefore suitable both for firmware development and direct device flashing.

## Raspberry Pi RFID

The `Raspberry-Pi-RFID` repository contains a small Node.js/browser-oriented RFID implementation with:

* `rfid.js`;
* `rfid2.html`;
* `package.json`;
* RFID-related image assets.

## Documentation boundary

The two repositories represent separate implementations of RFID functionality. Their exact reader hardware, GPIO mapping and protocol details should be taken from the respective source files before deployment.

## Source

Repositories:

* `SQ2MTG/esp-rfid`
* `SQ2MTG/Raspberry-Pi-RFID`
