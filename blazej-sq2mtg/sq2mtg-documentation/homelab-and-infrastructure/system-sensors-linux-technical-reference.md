# System Sensors Linux — Technical Reference

## Repository status

* GitHub repository: `SQ2MTG/system-sensors-linux`
* Language: Shell
* Default branch: `main`
* Public repository
* No license metadata declared
* Last push: 2026-09-05
* Purpose: read Linux hardware sensor values and publish them to MQTT on a LAN.

## Sensor stack

The project uses Linux hardware-monitoring utilities including:

* `lm-sensors`
* `smartmontools`
* `mosquitto-clients`
* `pciutils`
* `fancontrol`
* optional NVIDIA/ROCm-related monitoring

The documented installation target is `/opt/system-sensors`, with a service and local `data.log`.

## MQTT model

Published telemetry follows the documented topic pattern:

`pc-sensors/<hostname>/<category>/<sensor_name>`

This provides a stable hierarchy for dashboards and MQTT consumers while separating hosts and sensor categories.

## Deployment

The repository is an operational shell toolkit. Installation can create files, install packages, configure services and interact with hardware-monitoring subsystems. Review scripts before execution and test on a non-critical host first.

## Security

MQTT credentials, broker addresses and privileged service configuration should be externalized rather than hard-coded. Restrict the broker to the LAN/VPN required by the deployment.
