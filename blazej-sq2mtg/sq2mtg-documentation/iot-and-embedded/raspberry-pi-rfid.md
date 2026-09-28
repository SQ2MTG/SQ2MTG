# Raspberry Pi RFID

Simple Raspberry Pi + RC522 RFID web-login/access project.

## Scope

The repository is a historical fork of `luigifcruz/Raspberry-Pi-RFID`. The README describes a minimal RFID web-login interface using a Raspberry Pi and RC522 reader.

## Provenance

* Original project: Luigi Freitas Cruz.
* License: MIT.
* Historical tutorial/video links are included in the upstream README.

## Documentation boundary

The README is intentionally minimal and does not define the complete runtime stack, GPIO mapping, database/storage model, web routes or authentication semantics.

Those details should be taken from the source before deploying the project as an access-control system.

## Security

RFID UID-based systems should not be treated as strong authentication by default. For any real access-control deployment, add appropriate authorization, credential protection, network isolation and audit controls.
