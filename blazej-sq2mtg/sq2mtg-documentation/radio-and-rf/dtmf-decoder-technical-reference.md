# DTMF Decoder — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/DTMF-Decoder`
* Language: shell
* License: GPLv3
* Default branch: `main`
* Last recorded update: 2024-08-10

## Function

The project implements a lightweight DTMF command decoder on Linux. The documented processing chain uses `arecord` to capture audio and `multimon-ng` to decode DTMF tones.

## Command processing

The documented implementation maintains a three-digit DTMF command buffer and dispatches an action after a complete command is received.

A production deployment should validate decoded input before executing any action. Do not treat arbitrary DTMF input as trusted control-plane data.

## Runtime dependencies

* ALSA `arecord`
* `multimon-ng`
* shell environment and the commands/scripts invoked by the decoder

Exact audio device parameters, command mappings and action scripts should be verified from the current repository source.

## Operational security

If DTMF commands can trigger privileged actions, run the decoder with the minimum required OS privileges and use an allowlist for commands. Keep externally supplied or radio-derived input separated from shell command construction.
