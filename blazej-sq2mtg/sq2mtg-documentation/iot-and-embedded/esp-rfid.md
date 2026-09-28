# ESP RFID

ESP8266-based RFID access-control project supporting MFRC522, PN532 and Wiegand readers.

## Hardware

The README documents:

* ESP8266, including WeMos D1 mini / NodeMCU 1.0;
* at least 32 Mbit flash / 4 MB;
* MFRC522 or PN532 RFID/NFC reader;
* Wiegand readers;
* relay output.

ESP32 is explicitly not supported by the documented project version.

## Features

* Web-based configuration.
* RFID user management.
* WebSocket communication.
* JSON data exchange.
* NTP time synchronization.
* MQTT support.
* Mobile/desktop web UI.
* Up to approximately 1,000 users in the documented test.

## Build

The project uses PlatformIO:

```bash
platformio run
platformio run -e nodemcu -t upload
platformio run -t clean
```

## Typical MFRC522 wiring

| Signal     | WeMos D1 mini | NodeMCU |
| ---------- | ------------: | ------: |
| SPI SS/SDA |            D8 |      D8 |
| MOSI       |            D7 |      D7 |
| MISO       |            D6 |      D6 |
| SCK        |            D5 |      D5 |

Wiegand D0/D1 are configurable; the documented defaults are GPIO-4 and GPIO-5.

## Security status

The project explicitly describes itself as hobby-grade and warns that UID-only RFID identification is not strong authentication. It should not be used as a high-assurance access-control system without additional security controls.

## License

The repository documents the Unlicense.
