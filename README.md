[![Website](https://img.shields.io/website?url=https%3A%2F%2Fntkstudio.net%2Fproducts%2Frevolt-keyboard%2F)](https://ntkstudio.net/products/revolt-keyboard/)
![GitHub License](https://img.shields.io/github/license/nietaki/revolt-keyboard?color=green)
[ ![Discord](https://img.shields.io/discord/1435326750799433919?logo=discord&color=%235865F2)](https://discord.gg/myEkxF7rhV)
[![Shopify](https://img.shields.io/badge/Shopify-7AB55C?logo=shopify&logoColor=fff)](https://ntkstudio.net/products/revolt-keyboard/#buy)

# Revolt Keyboard

> **Revolt** - a split ergonomic keyboard prioritising ease of adoption, flexibilty, easy build+repair, and partial upgrades
> 

![final result](./images/main.jpg)

## Why call it “Revolt”?

1. It’s heavily inspired by [Redox](https://github.com/mattdibi/redox-keyboard), an amazing open-source keyboard, that is still my daily driver
2. It’s revolting against the popular design philosophy of keybords like Sofle, Lily58 or Corne, which prioritise a compact footprint over other qualities
3. Some might find it “revolting”, since its looks are secondary to its features

More info on the design philosophy behind revolt in the [Revolt Manifesto](./Revolt_Manifesto.md)


## TL;DR

It’s a 68(+3) key, wired, choc-based split ergonomic keyboard running QMK. Instead of being split into 2 halves, it’s split into 3 parts: left input, right input and the center one called “commander”


![input board](./images/revolt_3d_render.png)

![commander board](./images/commander_3d_render.png)

The left and right input parts are “dumb”, and contain only the switches and diodes to make 7x5 matrix work, plus optional LEDs under home keys.

The case will be made with low profile + tenting in mind (with multiple tenting angles possible), with two versions: for soldered switches without a top plate and hotswap with a top plate.

The commander board should lend itself to experimenting with different pointing devices. 
Current has connectors for a PSP 3000 joystick. It should be easy to create versions that support other pointing devises, like a trackball, a Cirque touchpad or other joysticks.

## How To...

### ...build the keyboard?

Follow the [build video](https://www.youtube.com/watch?v=ghhF0bAFxww). You can find more support under the links [here](https://ntkstudio.net/products/revolt-keyboard/#support).

### ...make the cases?

The case files are available on [Printables](https://www.printables.com/model/1439208-revolt-keyboard-cases-rev1) and [Thingiverse](https://www.thingiverse.com/thing:7166363).

### ...compile the firmware?

```bash
$ cd /path/to/qmk_firmware
$ qmk compile -kb revolt/rev1 -km default
#  It should generate the firmware file
$ stat ./revolt_rev1_default.uf2
```
### ...flash the firmware?

1. Unplug the commander board
1. Push the `bootsel` button on the RP2040
1. While having the button pushed in, connect the commander board to the computer

A virtual drive (?) for the rpi should be discovered by the computer. 
Drag the compiled firmware file into it. 
RPi will reboot and run the firmware.


## FAQ

### Why do you hate Sofle/Lily58/Corne?

I don’t! They’re beautiful keyboards, designed with love and forethought, all of them with passionate communities. They just don’t fit the criteria of what I’m looking for in an ergonomic keyboard that can be used just as easily for programming and gaming, especially for people coming from “regular” keyboards. I wanted to make a keyboard that’s perfect for me and other like-minded people.

### No wireless version?

I’m not ruling out a wireless version in the future. I’d like to perfect the wired version to my liking and see what kinds of compromises make sense.

But with Revolt being open source, there’s no reason for anyone interested not to take a crack at it themselves.

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
- https://github.com/sol/KiCad-RP-Pico

## License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a>

[Revolt Keyboard](https://github.com/nietaki/revolt-keyboard)© 2024 by [@nietaki](https://nietaki.com/) is licensed under [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1)
