# revolt-keyboard

## Workflow

1. Build matrix, outline and pcb in yml
2. generate kicad pcb
3. Create the kicad project
4. Replace the kicad pcb file with the generated one
5. Replace the switch footprints with the ones from keyswitch library
5. Create the matrix schematic by hand, with the diode numbers matching the swich numbers from pcb
6. **change the diode numbers in the pcb to line up with the switch numbers in the pcbnew**
7. Update net names from pcb into the schematic
8. ...
