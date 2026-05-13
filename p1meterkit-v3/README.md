# P1MeterKit V3

Hardware version V3 is based on the **ESP32-C6**.

## Specifications

| Component | Details |
|-----------|---------|
| **MCU** | ESP32-C6 |
| **Connectivity** | WiFi with Improv BLE/Serial |
| **P1 Interface** | DSMR v4/v5 compatible |
| **Sensors** | HDC1080 (Temp/Humidity) |
| **Status LED** | GPIO1 |
| **Green LED** | GPIO7 |
| **Flash** | 4MB |

## GPIO Pinout

| Function | GPIO |
|----------|------|
| Status LED | GPIO1 |
| Green LED | GPIO7 |
| I2C SDA | GPIO6 |
| I2C SCL | GPIO5 |
| DSMR RX | GPIO4 |
| DSMR Request | GPIO0 |

## Firmware Variants

| Variant | Description |
|---------|-------------|
| **p1meterkit.yaml** | Standard local WiFi firmware for the ESP32-C6 hardware revision |

## Installation via ESPHome Dashboard

```yaml
packages:
  p1meterkit: github://smarthomeshop/p1meterkit/p1meterkit-v3/p1meterkit.yaml@main
```

## Notes

- Initial onboarding is handled through captive portal, Improv BLE, or Improv Serial.
- HTTP OTA updates are exposed through the firmware update entity.
- Serial logging and Improv Serial use `UART0`, matching the ESP32-C6 USB-to-UART bridge used by the web flasher.
- The fallback access point uses the device name as SSID and password.
- This firmware is local-only and does not include SmartHomeShop cloud, MQTT telemetry, or HTTP registration.

## OTA Updates

Firmware updates are automatically made available via:
- `https://smarthomeshop.github.io/p1meterkit/p1meterkit-v3-manifest.json`
