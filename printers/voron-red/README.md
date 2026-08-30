# Voron-Red Klipper config

Working Klipper overlay from Field Pivot's Voron (shop name: Voron-Red).

This is a **starting point for this machine family**, not a drop-in for your printer. Copy structure and macros. Do not copy the `SAVE_CONFIG` block (Z offset, input shaper, PID, bed mesh). Those are this printer's last tune.

Klicky files live in `KlickyProbe/` so they match the includes in `printer.cfg` and `nozzle_scrub-2.cfg`.

## Hardware this file matches

- Voron 2.4-class CoreXY, 300 mm square, Z max 260 mm
- BTT Octopus Pro (STM32H723) + BTT Nitehawk toolhead MCU
- Stealthburner / Clockwork 2, Bondtech 5 mm gears, **0.6 mm** nozzle
- Klicky dockable probe (gantry/frame dock)
- ADXL345 on the toolhead (`axes_map: x,z,y`)
- Knomi2 status hooks
- Nozzle bucket / scrub
- Stealthburner + chamber + electrical-bay LEDs
- Pi camera via Crowsnest / spyglass (IMX708)

## Still to drop in from the project folder (web upload)

These are large and were not pushed through this hook:

- `led-test.cfg` (included by `printer.cfg`)
- `mainsail.cfg`
- `timelapse.cfg`

## Do not copy blindly

- `probe` `z_offset` in SAVE_CONFIG (this machine: 5.42)
- Input shaper frequencies, PID, bed meshes
- MCU `serial:` by-id paths
- KlipperScreen lock PIN is stripped in this repo. Set it only on the Pi.

## Credit

- [jlas1/Klicky-Probe](https://github.com/jlas1/Klicky-Probe)
- LED effect pack as used on this printer
- Klipper / Voron Design / BTT Nitehawk / Mainsail Crew pin maps and service configs

## License

Klicky and Mainsail-crew files keep their upstream licenses. Field Pivot additions: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
