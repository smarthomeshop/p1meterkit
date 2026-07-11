# P1MeterKit V3

Hardware version V3 is based on the **ESP32-C6**.

## Specifications

| Component | Details |
|-----------|---------|
| **MCU** | ESP32-C6 |
| **Connectivity** | WiFi with Improv BLE/Serial or local Thread |
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
| **p1meterkit-cloud.yaml** | WiFi firmware with SmartHomeShop cloud registration and telemetry sync |
| **p1meterkit-thread.yaml** | Local Home Assistant firmware over an existing Thread network |

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
- The standard firmware is local-only; the separate cloud variant adds SmartHomeShop HTTP registration and telemetry sync.
- The Thread variant is local-only and requires the Active Dataset TLVs from an existing Thread network. It reads one DSMR telegram every 5 seconds to keep Thread traffic low.

## Thread Installation

Use the dedicated package in ESPHome and replace the dataset placeholder with
the Active Dataset TLVs from Home Assistant:

```yaml
substitutions:
  thread_dataset: "PASTE_YOUR_ACTIVE_DATASET_TLVS_HERE"

packages:
  remote_package:
    url: https://github.com/smarthomeshop/p1meterkit
    ref: main
    files: [p1meterkit-v3/p1meterkit-thread.yaml]
    refresh: 1d
```

The first installation must be done over USB. Thread firmware has no WiFi
fallback hotspot and no SmartHomeShop cloud connection.

## OTA Updates

Firmware updates are automatically made available via:
- `https://smarthomeshop.github.io/p1meterkit/p1meterkit-v3-manifest.json`
- `https://smarthomeshop.github.io/p1meterkit/p1meterkit-v3-cloud-manifest.json`
