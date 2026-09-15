# Hardware Source

This directory contains the supplied KiCad project files for the current RF backscatter tag design.

| File | Purpose |
|---|---|
| `Backscatter_Tag_First_Version.kicad_pro` | KiCad project configuration |
| `Backscatter_tag_First_Version.kicad_sch` | Schematic source |
| `Backscatter_Tag_First_Version.kicad_pcb` | PCB layout source |

The schematic title is `RF_Backscatter_Tag_250_MHz`.

## Before editing

The schematic references custom antenna libraries:

- `My_custom_symbols_1:Ant_smd_RF1`
- `my_custom_footprints:Antenna_Pad`

The supplied archive did not contain those library files. Add them to the project and configure `sym-lib-table` / `fp-lib-table` before making a manufacturing revision.

## Manufacturing archive

The supplied ODB archive is stored separately under `../manufacturing/` so that source design files and manufacturing artifacts remain clearly separated.
