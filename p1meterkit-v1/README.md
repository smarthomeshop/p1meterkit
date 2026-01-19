# P1MeterKit V1

Hardware version V1 is based on the **ESP8266 (D1 Mini)**.

## Specifications

| Component | Details |
|-----------|---------|
| **MCU** | ESP8266 (D1 Mini) |
| **Connectivity** | WiFi only |
| **P1 Interface** | DSMR v4/v5 compatible |
| **Sensors** | HDC1080 (Temp/Humidity) |
| **Status LED** | GPIO16 |
| **Green LED** | GPIO12 |

## GPIO Pinout

| Function | GPIO |
|----------|------|
| Status LED | GPIO16 |
| Green LED | GPIO12 |
| I2C SDA | GPIO4 |
| I2C SCL | GPIO5 |
| DSMR RX | GPIO13 (D7) |
| DSMR Request | GPIO14 (D5) |

## Firmware Variants

| Variant | Description |
|---------|-------------|
| **p1meterkit.yaml** | Standard WiFi firmware |

## Installation via ESPHome Dashboard

```yaml
packages:
  p1meterkit: github://smarthomeshop/p1meterkit/p1meterkit-v1/p1meterkit.yaml@main
```

## OTA Updates

Firmware updates are automatically made available via:
- `https://smarthomeshop.github.io/p1meterkit/p1meterkit-v1-manifest.json`
