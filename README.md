# P1MeterKit for Home Assistant / ESPHome

![P1MeterKit](images/p1meterkit-shop.png)

P1MeterKit is a compact ESPHome-based smart meter reader for Home Assistant. It reads DSMR telegrams from the P1 port and exposes electricity, gas, and environmental data locally without cloud dependencies.

Product page: https://p1meterkit.nl/en

## How It Works

P1MeterKit connects directly to the P1 port of a DSMR smart meter with an RJ12 cable. It reads incoming DSMR telegrams and publishes the data locally to Home Assistant through ESPHome.

## Key Features

- Real-time electricity consumption and production monitoring
- Gas monitoring through the meter's M-Bus data
- Voltage and current monitoring per phase
- Temperature and humidity sensing with HDC1080
- WiFi onboarding with captive portal fallback
- Fully local operation with Home Assistant and ESPHome

## Hardware Versions

| Version | Chip | Connectivity | Description |
|---------|------|--------------|-------------|
| V1 | ESP8266 | WiFi | Original compact P1MeterKit hardware |
| V2 | ESP32-C3 | WiFi | Updated hardware with Improv BLE and Improv Serial provisioning |
| V3 | ESP32-C6 | WiFi | ESP32-C6 hardware with local firmware and Improv provisioning |

## Variants

We publish one customer-facing local WiFi firmware variant per hardware revision.

| Hardware | Variant | Description |
|----------|---------|-------------|
| V1 (ESP8266) | WiFi | Standard local WiFi firmware |
| V2 (ESP32-C3) | WiFi | Standard local WiFi firmware with Improv BLE and Improv Serial |
| V3 (ESP32-C6) | WiFi | Standard local WiFi firmware with Improv BLE and Improv Serial |

## Getting Started

1. Connect the kit to the smart meter with the included RJ12 cable.
2. Flash the firmware with the web flasher or ESPHome CLI.
3. If WiFi is not configured yet, connect to the fallback hotspot.
4. On V2 and V3 hardware, you can also use Improv BLE or Improv Serial for provisioning.
5. Add the discovered ESPHome device to Home Assistant.

Web flasher: https://smarthomeshop.io/en/firmware
Quick start guide: https://smarthomeshop.io/quick-start-p1meterkit

## Version History

- Customer-facing release notes: [CHANGELOG.md](CHANGELOG.md)
- GitHub Releases: https://github.com/smarthomeshop/p1meterkit/releases

## Repository Layout

```text
p1meterkit/
├── p1meterkit-v1/          # V1 ESP8266 ESPHome configurations
├── p1meterkit-v2/          # V2 ESP32-C3 ESPHome configurations
├── p1meterkit-v3/          # V3 ESP32-C6 ESPHome configurations
├── .github/workflows/      # Build and release automation
├── CHANGELOG.md            # Customer-facing firmware notes
└── images/
```

## Firmware Downloads

Pre-built firmware manifests are published on the `gh-pages` branch.

- V1 WiFi: `p1meterkit-v1-manifest.json`
- V2 WiFi: `p1meterkit-v2-manifest.json`
- V3 WiFi: `p1meterkit-v3-manifest.json`

## Sensors

| Sensor | Description |
|--------|-------------|
| Energy Consumed Tariff 1/2 | Total energy consumed per tariff |
| Energy Produced Tariff 1/2 | Total energy returned per tariff |
| Power Consumed | Current electricity usage |
| Power Produced | Current electricity production |
| Voltage Phase 1/2/3 | Voltage per phase |
| Current Phase 1/2/3 | Current per phase |
| Gas Consumed | Total gas consumption |
| Temperature | Environment temperature |
| Humidity | Environment humidity |
| WiFi Signal | WiFi signal strength |

## DSMR Notes

P1MeterKit supports DSMR v4/v5 style P1 telegrams. The gas meter M-Bus channel can differ per installation; V3 defaults to M-Bus ID 2 to match the ESP32-C6 hardware test configuration.

## Contributing

PRs and issues are welcome. Please keep changes modular and follow ESPHome best practices.

## Support

- Product info and guides: https://p1meterkit.nl/en
- Store: https://smarthomeshop.io
- Community and support: https://smarthomeshop.io/discord

## License

This project is released under the CC BY-NC 4.0 license.
