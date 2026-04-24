# Water Alarm

Home Assistant automation blueprint for critical water leak alerts with repeating notifications and optional smart plug power-off.

## Features

- Critical mobile push notifications
- Repeating alerts until the sensor is dry again
- Supports multiple Home Assistant mobile_app devices
- Configurable repeat interval
- Optional switch / smart plug power-off
- Useful for dishwasher, washing machine, sink cabinet, or basement monitoring

## Tested with

- Tuya Smart Water Leak Sensor Flood Model CB32

## Files

- `critical_water_leak_alarm.yaml` — automation blueprint

## Import into Home Assistant

1. Open **Settings**
2. Go to **Automations & scenes**
3. Open **Blueprints**
4. Click **Import Blueprint**
5. Paste this URL:

```text
https://raw.githubusercontent.com/kemoxi/haos-blueprints/main/water-alarm/critical_water_leak_alarm.yaml
```

## Inputs

- **Water sensor** — the binary sensor that reports water
- **Mobile devices to notify** — one or more phones with the Home Assistant Companion App
- **Alarm title** — title of the first alert
- **Alarm message** — message of the first alert
- **Repeat message** — repeated alert text while water is still detected
- **Repeat interval** — how often the alert repeats
- **Optional switch to turn off** — for example a smart plug powering a dishwasher

## Example use case

Use this blueprint to detect water near a dishwasher, send critical alerts to multiple iPhones, and optionally cut power to the dishwasher smart plug.

## Notes

- Critical alerts must be allowed on iPhone / iOS
- The Home Assistant Companion App must be installed on each target device
- The generated `notify.mobile_app_*` service depends on the Companion App device name
- If a selected phone does not receive alerts, verify its mobile app notification service in Home Assistant

## Repository

GitHub repository:

- https://github.com/kemoxi/haos-blueprints
