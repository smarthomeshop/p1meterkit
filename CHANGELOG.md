# Changelog

All notable customer-facing firmware changes for P1MeterKit are tracked in this file.

This changelog starts on 2026-05-13. Earlier firmware versions existed before that date, but they were not tracked in a customer-facing changelog.

## [Unreleased]

- Add customer-facing changes here before the next release is published.

## [P1MeterKit V3 3.2] - 2026-05-13


- P1MeterKit V3 now routes serial logging and Improv Serial over `UART0`, matching the WaterMeterKit ESP32-C6 provisioning setup used by the web flasher.
- P1MeterKit V3 now uses the device name as both fallback hotspot SSID and password.
- P1MeterKit V3 has been simplified to a single WiFi-only configuration file, matching the WaterMeterKit V3 package layout.


## [P1MeterKit V3 3.1] - 2026-05-13


- Initial P1MeterKit V3 firmware track has been added for the ESP32-C6 hardware revision.
- P1MeterKit V3 now includes local DSMR reading, HDC1080 temperature/humidity sensing, Improv BLE, Improv Serial, and HTTP OTA update support.
- P1MeterKit V3 uses the ESP32-C6 pinout from the validated local test build: status LED GPIO1, green LED GPIO7, I2C GPIO6/GPIO5, DSMR RX GPIO4, and DSMR request GPIO0.
- P1MeterKit V3 is published as a local-only firmware without SmartHomeShop cloud registration, MQTT telemetry, or cloud reset controls.
- Firmware publishing now matches the shared SmartHomeShop release flow with changelog validation, automatic version tags, gh-pages manifests, and GitHub Releases.


## [P1MeterKit V2 2.3] - 2026-05-13

### Added

- Customer-facing version history now lives in this repository.
- GitHub Releases will now be published for future firmware versions.

## [P1MeterKit V1 1.3] - 2026-05-13

### Added

- Customer-facing version history now lives in this repository.
- GitHub Releases will now be published for future firmware versions.
