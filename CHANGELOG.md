# Changelog

All notable customer-facing firmware changes for P1MeterKit are tracked in this file.

This changelog starts on 2026-05-13. Earlier firmware versions existed before that date, but they were not tracked in a customer-facing changelog.

## [Unreleased]

- Add customer-facing changes here before the next release is published.

## [P1MeterKit V2 2.8] - 2026-07-17


- Added a CPU temperature diagnostic sensor, also synced to SmartHomeShop Cloud, and updated the built-in web interface to version 3.



## [P1MeterKit V3 3.7] - 2026-07-17


- Added a CPU temperature diagnostic sensor, also synced to SmartHomeShop Cloud, and updated the built-in web interface to version 3.



## [P1MeterKit V2 2.7] - 2026-07-17


- Fixed cloud firmware restarting every 15 minutes when Home Assistant is not connected: the no-client reboot of the native API is now disabled on cloud firmware, so cloud-only setups run uninterrupted.



## [P1MeterKit V3 3.6] - 2026-07-17


- Fixed cloud firmware restarting every 15 minutes when Home Assistant is not connected: the no-client reboot of the native API is now disabled on cloud firmware, so cloud-only setups run uninterrupted.



## [P1MeterKit V3 3.5] - 2026-07-11


- Added the P1MeterKit V3 Thread package, matching the WaterMeterKit Thread workflow. It connects locally to an existing Thread network, uses Home Assistant over IPv6, and reads DSMR data every 5 seconds to limit Thread traffic.


## [P1MeterKit V2 2.6] - 2026-07-07


- Added the branded SmartHomeShop setup portal to P1MeterKit V2 and V3 WiFi and cloud firmware: connecting to the fallback hotspot now opens a SmartHomeShop setup page to pick your WiFi network, choose the local or SmartHomeShop App firmware variant, and see clear next steps for Home Assistant or the app.
- Added a Firmware Variant selector to P1MeterKit V2 and V3 so the built-in updater can switch between the local and SmartHomeShop App (cloud) firmware manifests.
- Added the P1MeterKit V3 Thread package, matching the WaterMeterKit Thread workflow. It connects locally to an existing Thread network, uses Home Assistant over IPv6, and reads DSMR data every 5 seconds to limit Thread traffic.


## [P1MeterKit V3 3.4] - 2026-07-07


- Added the branded SmartHomeShop setup portal to P1MeterKit V2 and V3 WiFi and cloud firmware: connecting to the fallback hotspot now opens a SmartHomeShop setup page to pick your WiFi network, choose the local or SmartHomeShop App firmware variant, and see clear next steps for Home Assistant or the app.
- Added a Firmware Variant selector to P1MeterKit V2 and V3 so the built-in updater can switch between the local and SmartHomeShop App (cloud) firmware manifests.


## [P1MeterKit V1 1.5] - 2026-06-11


- Cloud firmware variants are now published for P1MeterKit V1, V2, and V3 with SmartHomeShop HTTP cloud registration and telemetry sync.
- GitHub Actions now builds and publishes separate cloud binaries and Web Tools manifests for V1, V2, and V3.
- P1MeterKit V2 keeps a legacy MQTT cloud package filename online for existing imports, while using the HTTP cloud telemetry module.
- P1MeterKit V3 now has a cloud firmware option in addition to the local-only WiFi firmware.


## [P1MeterKit V2 2.5] - 2026-06-11


- Cloud firmware variants are now published for P1MeterKit V1, V2, and V3 with SmartHomeShop HTTP cloud registration and telemetry sync.
- GitHub Actions now builds and publishes separate cloud binaries and Web Tools manifests for V1, V2, and V3.
- P1MeterKit V2 keeps a legacy MQTT cloud package filename online for existing imports, while using the HTTP cloud telemetry module.
- P1MeterKit V3 now has a cloud firmware option in addition to the local-only WiFi firmware.


## [P1MeterKit V3 3.3] - 2026-06-11


- Cloud firmware variants are now published for P1MeterKit V1, V2, and V3 with SmartHomeShop HTTP cloud registration and telemetry sync.
- GitHub Actions now builds and publishes separate cloud binaries and Web Tools manifests for V1, V2, and V3.
- P1MeterKit V2 keeps a legacy MQTT cloud package filename online for existing imports, while using the HTTP cloud telemetry module.
- P1MeterKit V3 now has a cloud firmware option in addition to the local-only WiFi firmware.


## [P1MeterKit V1 1.4] - 2026-06-01


- P1MeterKit V1 now enables 115200 baud serial live logging and Improv Serial WiFi provisioning over USB.
- P1MeterKit V2 now routes serial live logging over `UART0`, matching the USB-UART provisioning path used by the web flasher.
- P1MeterKit V2 now uses the device name as both fallback hotspot SSID and password.
- P1MeterKit V1 and V2 now expose DSMR current average demand and WiFi MAC diagnostics.
- P1MeterKit V1 and V2 now keep their hardware pinout in substitutions, matching the V3 configuration structure without changing the actual pins.


## [P1MeterKit V2 2.4] - 2026-06-01


- P1MeterKit V1 now enables 115200 baud serial live logging and Improv Serial WiFi provisioning over USB.
- P1MeterKit V2 now routes serial live logging over `UART0`, matching the USB-UART provisioning path used by the web flasher.
- P1MeterKit V2 now uses the device name as both fallback hotspot SSID and password.
- P1MeterKit V1 and V2 now expose DSMR current average demand and WiFi MAC diagnostics.
- P1MeterKit V1 and V2 now keep their hardware pinout in substitutions, matching the V3 configuration structure without changing the actual pins.


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
