# DTMF SSTV — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/dtmf_sstv`
* Language: Python
* Default branch: `main`
* Repository has no declared license metadata.
* Last repository push: 2025-10-26.

## System concept

This project implements a Raspberry Pi-based DTMF-triggered SSTV station. The documented hardware/software concept combines:

* DTMF input decoding
* MT8870 DTMF decoder hardware
* camera capture
* SSTV image generation/transmission
* PTT control for the radio

The intended sequence is effectively: DTMF command -> command handling -> image capture -> SSTV audio generation -> PTT/radio transmission.

## Hardware integration

The design includes an MT8870 interface, camera and radio PTT path. Exact GPIO assignments, audio routing, commands and timing must be verified from the current source and wiring documentation.

Radio interfaces require attention to electrical isolation and logic/audio levels. Do not connect GPIO directly to a radio PTT or audio path without confirming voltage, current and ground requirements.

## Operational model

A deployment should separate command reception from privileged radio-control actions and validate every DTMF command before execution.

## Licensing and maintenance

No license is declared in the repository metadata. Treat the code as all-rights-reserved unless a license file or explicit permission establishes otherwise. Exact implementation details remain source-verified rather than inferred.
