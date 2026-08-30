# Voron-Red Klipper config

Working config pack from Field Pivot's Voron (shop name: Voron-Red).

This is a **starting point for this machine family**, not a drop-in. Copy structure and macros. Do not copy the `SAVE_CONFIG` block. That is this printer's last tune.

## Hardware this pack matches

- Voron 2.4-class CoreXY, 300 mm square, Z max 260 mm
- BTT Octopus Pro (STM32H723) + BTT Nitehawk toolhead MCU
- Stealthburner / Clockwork 2, Bondtech 5 mm gears, 0.6 mm nozzle
- Klicky dockable probe (gantry / frame dock)
- ADXL345 on the toolhead (`axes_map: x,z,y`)
- Knomi2 status hooks
- Nozzle bucket / scrub
- Stealthburner + chamber + electrical-bay LEDs
- Pi camera via Crowsnest / spyglass (IMX708)

## In this folder

- `printer.cfg` — main machine file, macros, SAVE_CONFIG
- `nitehawk-sbv2.cfg` — toolhead MCU, extruder, probe, ADXL
- `Knomi2.cfg`
- `nozzle_scrub-2.cfg`
- `LED-Macros-Main.cfg`
- `LED-Effects-Main.cfg`
- `crowsnest.conf`
- `KlipperScreen.conf` — lock PIN stripped; set it only on the Pi
- `KlickyProbe/` — probe macros and this machine's dock numbers

`printer.cfg` also includes `mainsail.cfg`, `timelapse.cfg`, and `led-test.cfg`. Those, plus `moonraker.conf`, stay on the Pi. They are not part of this pack.

## Do not copy blindly

- `probe` `z_offset` in SAVE_CONFIG (this machine: 5.42)
- Input shaper frequencies, PID, bed meshes (`60Temp-9x9-HB` / `90Temp-9x9-HB`)
- MCU `serial:` by-id paths
- KlipperScreen lock PIN

## Credit

- [jlas1/Klicky-Probe](https://github.com/jlas1/Klicky-Probe)
- LED effect pack as used on this printer
- Klipper / Voron Design / BTT Nitehawk / Mainsail Crew

## License

Klicky and Mainsail-crew files keep their upstream licenses. Field Pivot additions: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
