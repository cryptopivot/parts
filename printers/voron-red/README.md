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

## What was changed for this repo

- Includes point at `Klicky/` in this folder (the Pi copy used `KlickyProbe/`).
- `mainsail.cfg` and `timelapse.cfg` are commented out. They live on the Pi, not here.
- Added an empty `Klicky/klicky-specific.cfg` so the Klicky include chain resolves.

## Do not copy blindly

- `probe` `z_offset` in SAVE_CONFIG (this machine: 5.50)
- Input shaper frequencies
- PID values
- Bed meshes (`60Temp-9x9-HB` / `90Temp-9x9-HB` names in PRINT_START — confirm those profiles exist before a hot start)
- MCU `serial:` by-id paths (your boards will differ)

## Credit

- [jlas1/Klicky-Probe](https://github.com/jlas1/Klicky-Probe) macros
- LED effect pack included as used on this printer
- Klipper / Voron Design / BTT Nitehawk pin maps

Original Field Pivot macros in `printer.cfg`: PRINT_START / PRINT_END, LOAD/UNLOAD_FILAMENT, G32 wiring to Klicky + Knomi + LEDs.

## License

Klicky files keep their upstream license. Field Pivot additions: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
