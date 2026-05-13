# P1MeterKit V1

Hardware version V1 is based on the **ESP8266 (D1 Mini)**.

## Specifications

| Component | Details |
|-----------|---------|
| **MCU** | ESP8266 (D1 Mini) |
| **Connectivity** | WiFi |
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
| **p1meterkit.yaml** | Standard local WiFi firmware |

## Installation via ESPHome Dashboard

```yaml
packages:
  p1meterkit: github://smarthomeshop/p1meterkit/p1meterkit-v1/p1meterkit.yaml@main
```

## Easy Setup

V1 supports WiFi setup via:
- **Captive Portal**: Connect to the `p1meterkit` hotspot and configure WiFi
- **ESPHome Dashboard**: Configure WiFi during adoption or source-based installation

## OTA Updates

Firmware updates are done via the ESPHome Dashboard in Home Assistant:
1. Go to Settings -> Add-ons -> ESPHome
2. Your P1MeterKit will show when an update is available
3. Click "Update" to flash the new firmware wirelessly

For initial flashing or recovery, use our web-based flash tool:
- https://smarthomeshop.io/en/firmware

Published Web Tools manifest:
- `https://smarthomeshop.github.io/p1meterkit/p1meterkit-v1-manifest.json`
