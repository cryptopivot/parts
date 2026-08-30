# parts

3D-printed replacement parts and jigs for kiosks, ATMs, lockers, and related field hardware.

Field Pivot does the field work. These files are what we actually print when OEM supply is dead or the wait is worse than making the piece.

Keywords: klipper, voron, voron-2.4, klicky, 3d-printing, stealthburner, nitehawk, field-service.

## Printer configs

- [printers/voron-red](printers/voron-red/) — Klipper overlay for the shop Voron (Octopus Pro + Nitehawk, Klicky, LEDs). Starting point, not a drop-in.

## Rules

- One folder per part, named for the machine and the piece (`redbox-outdoor-belt-guide`, `hub-locker-clip`, not `part1`).
- Each folder gets a `README.md` using [TEMPLATE.md](TEMPLATE.md).
- Publish only models we measured and built, or models we remixed with the original author credited in that folder README.
- No store names, no customer names, no keys, no payment hardware dumps.
- Outdoor parts: say the filament that survived sun and weather. Do not list PLA as outdoor-ready.

## Layout

```
parts/
  TEMPLATE.md
  printers/<printer-name>/
  <machine>-<piece>/
    README.md
    *.stl / *.step
    photos/
```

## License

Unless a folder says otherwise, new original models here are [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Remixes keep the upstream license.

Related: [field-ops](https://github.com/cryptopivot/field-ops) · [Field Pivot](https://fieldpivot.com)
