# Voron-Red Klipper config

Working Klipper overlay from Field Pivot's Voron (shop name: Voron-Red).

This is a **starting point for this machine family**, not a drop-in for your printer. Copy structure and macros. Do not copy the `SAVE_CONFIG` block (Z offset, input shaper, PID, bed mesh). Those are this printer's last tune.

## Hardware this file matches

- Voron 2.4-class CoreXY, 300 mm square, Z max 260 mm
- BTT Octopus Pro (STM32H723) + BTT Nitehawk toolhead MCU
- Stealthburner / Clockwork 2, Bondtech 5 mm gears, 0.4 mm nozzle
- Klicky dockable probe (gantry/frame dock)
- ADXL345 on the toolhead
- Knomi2 status hooks
- Nozzle bucket / scrub (purge disabled)
- Stealthburner + chamber + electrical-bay LEDs

## In this folder now

- `README.md`
- `nitehawk-sbv2.cfg`
- `Knomi2.cfg`
- `Klicky/klicky-probe.cfg`
- `Klicky/klicky-specific.cfg`
- `Klicky/klicky-quad-gantry-level.cfg`

## Still to drop in from the Pi / Voron-Red folder

GitHub web UI: Add file → Upload files.

- `printer.cfg` (main machine + PRINT_START/END + SAVE_CONFIG)
- `nozzle_scrub-2.cfg`
- `LED-Macros-Main.cfg`
- `LED-Effects-Main.cfg`
- `Klicky/klicky-macros.cfg`
- `Klicky/klicky-variables.cfg`
- `Klicky/klicky-bed-mesh-calibrate.cfg`

If you upload `printer.cfg` from the Pi, change `KlickyProbe/` includes to `Klicky/` so it matches this folder, and leave `mainsail.cfg` / `timelapse.cfg` on the Pi.

## Do not copy blindly

- `probe` `z_offset` in SAVE_CONFIG (this machine: 5.50)
- Input shaper frequencies
- PID values
- Bed meshes (`60Temp-9x9-HB` / `90Temp-9x9-HB` names in PRINT_START)
- MCU `serial:` by-id paths

## Credit

- [jlas1/Klicky-Probe](https://github.com/jlas1/Klicky-Probe)
- LED effect pack as used on this printer
- Klipper / Voron Design / BTT Nitehawk pin maps

## License

Klicky files keep their upstream license. Field Pivot additions: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
