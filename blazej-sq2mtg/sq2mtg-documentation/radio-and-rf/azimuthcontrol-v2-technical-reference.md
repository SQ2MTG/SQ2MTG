# Azimuthcontrol v2 — Technical Reference

## Purpose

`Azimuthcontrol_v2` is an ESP8266/NodeMCU antenna-rotator controller with a web interface.

The README documents:

* drive control,
* azimuth calculation from an analogue angle sensor,
* QTH-locator-based azimuth calculation,
* rotation to a target azimuth,
* drive inertia handling,
* timeout protection,
* bounds protection,
* Wi-Fi access-point/client operation,
* web configuration,
* calibration,
* persistent settings.

## Hardware

Documented controller: NodeMCU based on ESP8266.

Documented connections:

| NodeMCU pin | Function                      |
| ----------- | ----------------------------- |
| D0 / GPIO16 | Drive left                    |
| D1 / GPIO5  | Drive right                   |
| D2 / GPIO4  | Wi-Fi-connected status        |
| D3 / GPIO0  | Low-RSSI status               |
| A0          | Rotation-angle sensor voltage |
| Vin         | Module supply                 |
| GND         | Ground                        |

The drive outputs are described as controlling relay circuitry through transistors.

## Angle Measurement

The controller measures a voltage proportional to antenna position and converts it into azimuth.

The ESP8266 analogue input must remain within the documented input limit; the README describes using a voltage divider so the sensor range presented to A0 remains within the safe ADC range.

Calibration stores minimum and maximum sensor values corresponding to the mechanical endpoints and derives volts-per-degree. An inversion option is available when sensor voltage decreases as azimuth increases.

## Safety / Motion Limits

The README documents protective behavior for:

* drive timeout if the target azimuth is not reached,
* azimuth below `-5°`,
* azimuth above `365°`.

These values should be retained as implementation constraints until source verification changes them.

## Network / Web Interface

The controller can operate as:

* Wi-Fi access point,
* Wi-Fi client.

The historical default AP setup described in the README uses:

* SSID: `ESPAP`
* default AP address: `192.168.4.1`

The README also describes uploading web-interface files through the integrated FTP server.

**Security note:** the historical README contains default access credentials. They are intentionally not reproduced here. If this firmware is still deployed, all default passwords should be changed and FTP access should be restricted or removed where possible.

## Software Dependencies

The README documents Arduino IDE and:

* `ESP8266FtpServer.h`
* `ESP8266WiFi.h`
* `ESP8266WebServer.h`
* `FS.h`
* ArduinoJson 5.13.5

This is a historical dependency set; modern Arduino/ESP8266 environments may require compatibility adjustments.

## Verification Status

README inspected on 2026-09-28. The page records documented behavior and hardware mapping while deliberately excluding historical default credentials.
