# RFID Wisp for WT32-SC01 Plus

Standalone firmware for the WT32-SC01 Plus (ESP32-S3, 3.5" touch display)
plus a PN532 RFID module: reads and writes the same QIDI spool tags as the
[RFIDwisp](https://github.com/ThorSc/RFIDwisp) PC app, with Moonraker and
Spoolman integration, over Wi-Fi - no PC needed.

This repo holds **releases only** (prebuilt firmware binaries). The source
is developed in a private repository and published here automatically when
a version is released.

## Downloads

See the [latest release](../../releases/latest) for the current firmware
build. Each release contains:

| File | Purpose |
|------|---------|
| `bootloader.bin`, `partitions.bin`, `boot_app0.bin`, `firmware.bin` | The four files to flash - see `FLASHING.md` in the release for the exact `esptool.py` command and flash offsets. |
| `FLASHING.md` | Step-by-step flashing instructions. |
| `lang.example.json` | Optional UI string overrides (see the file's own comments / the source repo's README for how to use it). |

## What it does

- Reads and writes the 16-byte QIDI spool tag (MIFARE Classic 1K) with a
  PN532 reader.
- Shows a QIDI box's material slots live from Moonraker.
- Creates/links Spoolman spools when writing a tag.
- Supports several printers, configured via a Wi-Fi captive portal on first
  boot plus an on-device settings screen.

## Wiring and setup

See `FLASHING.md` in each release for flashing, and the source repository's
README for wiring (display/touch/PN532 pin assignments) and first-boot Wi-Fi
setup.
