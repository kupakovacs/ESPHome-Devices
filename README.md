# ESPHome Devices

This repository contains ESPHome configurations for multiple DIY devices, organized as one YAML file per device.

## Included configurations

- `/home/runner/work/ESPHome-Devices/ESPHome-Devices/bme280-sensor.yaml` – Outdoor BME280 temperature, humidity, and pressure sensor (ESP8266).
- `/home/runner/work/ESPHome-Devices/ESPHome-Devices/watch-winder.yaml` – Stepper-driven watch winder controller (ESP32 + ULN2003).
- `/home/runner/work/ESPHome-Devices/ESPHome-Devices/esp-relay.yaml` – Fairy lights serial-controlled switch (ESP8266).

## Safe to publish

All sensitive values have been moved to `!secret` references.
To use these configs, create a `secrets.yaml` file (not committed) next to the device YAML files.

You can start from `secrets.example.yaml`:

1. Copy `secrets.example.yaml` to `secrets.yaml`.
2. Replace every placeholder value with your real credentials and keys.
3. Flash using ESPHome as usual.

## Typical ESPHome workflow

Use the file you want to deploy:

- `esphome run bme280-sensor.yaml`
- `esphome run watch-winder.yaml`
- `esphome run esp-relay.yaml`
