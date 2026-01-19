# P1MeterKit for Home Assistant / ESPHome

![P1MeterKit](images/p1meterkit-shop.png)

P1MeterKit is a compact smart meter sensor designed to monitor your electricity and gas consumption in real-time. It integrates seamlessly with Home Assistant via ESPHome and runs fully local (no cloud required).

## How it works

The P1MeterKit connects directly to the P1 port of your DSMR smart meter using an RJ12 cable. It reads the DSMR telegrams and exposes real-time energy data to Home Assistant. Compatible with DSMR/SMR v4 and v5 smart meters.

👉 **Check compatibility for your smart meter**: https://p1meterkit.nl/en

## Key features

- **Energy monitoring**: Real-time electricity consumption and production tracking (3-phase support).
- **Gas monitoring**: Gas consumption via MBus connection.
- **Environment sensing**: Temperature and humidity measurement.
- **Connectivity**: Wi-Fi with captive portal fallback, Improv BLE/Serial.
- **Local only**: Works without cloud services (100% local); OTA supported via manifest on GitHub Pages.

## Variants

We publish firmware variants for two hardware versions. Each variant is a dedicated YAML in the version folder and ships with a matching Web Tools manifest on the `gh-pages` branch.

| Hardware | Variant | Description |
|----------|---------|-------------|
| V1 (ESP8266) | WiFi | Standard WiFi connectivity |
| V2 (ESP32-C3) | WiFi | WiFi with Improv BLE/Serial and OTA updates |

## Getting started

1. **Hardware**: Connect the P1MeterKit to your smart meter using the included RJ12 cable.
2. **Flash firmware**:
   - Use our web-based flash tool at https://smarthomeshop.io/en/firmware to flash or re-flash your kit.
   - Or compile/flash locally with ESPHome CLI.
3. **Onboarding**:
   - Connect to the `p1meterkit` hotspot if WiFi is not configured.
   - V2: Use Improv BLE or Improv Serial for provisioning.

Please check for full documentation our quick start guide: https://smarthomeshop.io/quick-start-p1meterkit

## Repository layout

- `p1meterkit-v1/` — ESPHome configurations for V1 (ESP8266)
- `p1meterkit-v2/` — ESPHome configurations for V2 (ESP32-C3)
- `.github/workflows/` — CI to build and publish artifacts/manifests to `gh-pages`
- `gh-pages` branch — public firmware and manifests (for OTA and ESP Web Tools)

## Sensors

| Sensor | Description |
|--------|-------------|
| Energy Consumed Tariff 1/2 | Total energy consumed per tariff (kWh) |
| Energy Produced Tariff 1/2 | Total energy produced per tariff (kWh) |
| Power Consumed | Current power consumption (kW) |
| Power Produced | Current power production (kW) |
| Voltage Phase 1/2/3 | Voltage per phase (V) |
| Current Phase 1/2/3 | Current per phase (A) |
| Gas Consumed | Total gas consumption (m³) |
| Temperature | Environment temperature (°C) |
| Humidity | Environment humidity (%) |
| WiFi Signal | WiFi signal strength |

## Contributing

PRs and issues are welcome. Please keep changes modular and follow ESPHome best practices.

## Support

- Product info and guides: https://p1meterkit.nl/en
- Store: https://smarthomeshop.io
- Community & support (Discord): https://smarthomeshop.io/discord

## License

This project is released under the MIT License (see `LICENSE`).
