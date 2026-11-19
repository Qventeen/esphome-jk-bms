# Products

My own device configs for the JK-PB2A16S v19 BMS over BLE. The example configs
from upstream stay in the repo root.

## In use

Nothing in this repo. The BMS is now read by the `bps` device (inverter and
BMS on one ESP32-C3). Its config lives in the `esphome-smg-ii` fork:
`products/esp32c3-backup-power-system.yaml`.

## Archive

All files here are BMS-only configs for the device `jk-bms-ble`. That device
does not run any more: `bps` holds the BLE link to the same BMS.

| File | What it was | Why archived |
|---|---|---|
| `archive/esp32-ble-v19-safe-updated.yaml` | Safe config: unsafe switches off, settings shown as read-only sensors | The BMS part of `bps` grew from it. |
| `archive/esp32-ble-v19-safe-updated-no-retrive-update.yaml` | Same, but "Retrieve settings" does not refresh the read-only sensors | An experiment. |
| `archive/esp32-ble-v19-safe.yaml` | Earlier safe config | Replaced by `safe-updated`. |
| `archive/esp32-ble-v19-full.yaml` | Full control config | Replaced by the safe configs. |
| `archive/esp32-ble-v19-example.yaml` | Almost the same as `full` | Differs only in one `output_power` spelling. |
