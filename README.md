# P1MeterKit for Home Assistant

![P1MeterKit Logo](images/P1MeterKit-logo.png)

With the P1MeterKit, you can gain real-time insights into both your electricity and gas consumption. This kit is fully integrated with Home Assistant and DSMR Reader. Measure your electricity and gas consumption down to the minute and then visualize it per hour, day, month, or year in Home Assistant. Additionally, the kit also measures the temperature and humidity in the room where the meter is installed.

Check our website to see if your smart meter is compatible: https://P1MeterKit.nl/en

## Features

- **Direct Power Monitoring:** Connect directly to smart meters to monitor power usage in real-time.
- **Compatibility:** Specifically designed for smart meters (DSMR/SMR v4 and v5).
- **Easy Installation:** Simple setup, just plug the RJ12 Cable in the kit and enjoy.
- **Integrated Home Assistant Support:** Fully integrates with Home Assistant Energy Dashboard, providing seamless automation and monitoring.

## Firmware variants

- **P1MeterKit v1 (ESP8266 / `p1meterkit-v1`):** targets the original hardware revision based on the ESP8266. This build remains available through the legacy package URL so existing installations keep working without changes.
- **P1MeterKit v2 (ESP32-C3 / `p1meterkit-v2`):** optimized for the refreshed hardware featuring the ESP32-C3 and backed by automated firmware builds and version bumps via GitHub Actions.

Always flash the firmware variant that matches your hardware. We recommend using v2 for all new projects, while v1 ensures long-term support for legacy kits already in the field.

## What's in the box:

- P1Meter Kit: The main unit that directly connects to your DSMR P1 port for real-time monitoring of your energy consumption.
- RJ12 Cable: Seamlessly connects your P1Meter Kit to your energy meter, ensuring an effortless setup. 
- Manual: A step-by-step guide that walks you through the quick and easy installation process.

## Installation

For a complete installation guide and tips on integrating with Home Assistant, visit our website at [SmartHomeShop.io](https://smarthomeshop.io/en).

## Contributing

We welcome contributions to improve the P1MeterKit. If you have suggestions or improvements, please submit a PR.

## Support

Join our [Discord community](https://smarthomeshop.io/discord) for support, to ask questions, and to connect with other smart home enthusiasts.

## License

This project is open-sourced under the [MIT License](LICENSE).
