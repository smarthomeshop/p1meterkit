# P1MeterKit V2

Hardware version V2 is based on the **ESP32-C3**.

## Specifications

| Component | Details |
|-----------|---------|
| **MCU** | ESP32-C3 |
| **Connectivity** | WiFi with Improv BLE/Serial |
| **P1 Interface** | DSMR v4/v5 compatible |
| **Sensors** | HDC1080 (Temp/Humidity) |
| **Status LED** | GPIO10 |
| **Green LED** | GPIO1 |

## GPIO Pinout

| Function | GPIO |
|----------|------|
| Status LED | GPIO10 |
| Green LED | GPIO1 |
| I2C SDA | GPIO5 |
| I2C SCL | GPIO4 |
| DSMR RX | GPIO3 |
| DSMR Request | GPIO0 |

## Firmware Variants

| Variant | Description |
|---------|-------------|
| **p1meterkit.yaml** | Standard WiFi firmware with Improv |

## Installation via ESPHome Dashboard

```yaml
packages:
  p1meterkit: github://smarthomeshop/p1meterkit/p1meterkit-v2/p1meterkit.yaml@main
```

## Easy Setup

V2 supports easy WiFi setup via:
- **Captive Portal**: Connect to the hotspot and configure WiFi
- **Improv BLE**: Configure via Bluetooth with the Home Assistant app
- **Improv Serial**: Configure via USB connection

## OTA Updates

Firmware updates are automatically made available via:
- `https://smarthomeshop.github.io/p1meterkit/p1meterkit-v2-manifest.json`

Updates are directly available in Home Assistant when a new version is released.
