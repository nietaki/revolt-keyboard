# revolt-keyboard

## TODO

- [x] ERC, DRC rules from JLC
- [x] relative path footprint library for portable projects
- [x] reversible IDC14 connector footprint
- [x] dimension check for connector
- [ ] add extra space on left and right to facilitate hotswap sockets in the future
- [ ] move the rotated diodes for the same reason
- [ ] LEDs in the schematic
- [ ] port the manifesto to the repo
- [ ] open source the repo (license: https://creativecommons.org/licenses/by-sa/4.0/ I guess, because of the footprints)

## Workflow

1. Build matrix, outline and pcb in yml
2. generate kicad pcb
3. Create the kicad project
4. Replace the kicad pcb file with the generated one
5. Replace the switch footprints with the ones from keyswitch library
5. Create the matrix schematic by hand, with the diode numbers matching the swich numbers from pcb
6. **change the diode numbers in the pcb to line up with the switch numbers in the pcbnew**
  - this can be automated together with the switch numbers, I think
7. Add hierarchical net names
7. Update the schematic from the pcb band the other way until stuff is consistent.
8. ...
8. Draw the rest of the owl

## Special thanks

Projects that helped or inspired me:

- https://github.com/mattdibi/redox-keyboard
- https://github.com/daprice/keyswitches.pretty/ - adapted some footprints from this brilliant library
- https://flatfootfox.com/ergogen-introduction/
- https://github.com/labtroll/KiCad-DesignRules/tree/main
- https://docs.ergogen.xyz/
