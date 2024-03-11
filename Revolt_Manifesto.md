# Revolt Manifesto

## Design principles

### Enough keys to be single layer friendly

Keyboards smaller than Ergodox/Redox/Ergodash can’t fit many of the keys needed for every day use, forcing the users to rely on layers and dual-function keys. Working with a single layer 95% of the time allows you to use Revolt for anything you need it for, without crafting and memorizing shortcuts or being careful with dual-function keys.

That’s not to say you can’t use a layered setup you like - QMK allows for many layers and advanced functions, as you can see in the [configurator](https://config.qmk.fm/#/redox/rev1/base/LAYOUT).

I personally use layer 2 mainly for function keys and media keys in my Redox.

I’d argue this also has a positive impact on the typing speed. Many people argue that the main factor in the typing speed is not having to move your fingers much (with fewer keys, more layers and possibly something like the Colemak layout). I believe having to use key combos or different behaviour on key tap and key hold to input characters slows down your typing. The mental load to keep up with a complicated setup doesn’t help either. 

### Ease of adoption

People adopting Revolt can leverage their muscle memory with minimal changes, thanks to the `CTRL` and `META/WIN/CMD` keys in their regular locations and the flexibility of QMK.  

### Ergonomics

This one might seem pretty obvious, but hear me out.

The reason I first got into ergonomic keyboards was the RSI I was getting from long hours of coding early in my career - I was getting terrible wrist pain after hours of coding early in my career. I got a [Microsoft Sculpt Ergonomic Keyboard](https://www.google.com/search?q=microsoft+sculpt+ergonomic+keyboard&tbm=isch), which instantly made the problem go away.

I had a number of those throughout the years (5 keyboard+mouse sets?) and I loved them, but they kept on breaking. I got better at fixing them, cleaning and replacing the key stabilizers, but I kept having to buy new ones - and I think the keyboard is out of production by now…

This made it obvious to me I needed a mechanical keyboard that still had the ergonomics I was looking for - a stable keyboard with split layout with tenting and a good amount of keys.

I built myself a custom Redox and bought some wristpads for it - I still use it to this day. But I’d still prefer a lower profile keyboard with a pointer device in the middle (a touchpad, a trackball, or a Thinkpad-style trackpoint). 

This is where Revolt comes in - I hope I can have it all (and more) with this design

I’m trying to achieve good ergonomics with:

- Case designed with tenting in mind
- Keys closer together thanks to smaller footprints of Kailh Choc keycaps
- Keys closer to the desk surface (again thanks to Kailh Choc switches and a purpose-designed case)
- A more aggressive pinky stagger than some of the other designs

### Bang for buck

I wanted to keep the build affordable and simple, without sacrificing any of the other priorities. The simplest non-hotswap version should be doable for around 80 EUR, with not much more cost for a version with 3d-printed tenting case.

I want the design to lend itself to higher end versions, with hot-swap sockets and a top plate, integrated touchpad, and possibly 2 microcontrollers with wireless communication (all hopefully to come in future versions)

### Easy to build/fix

I’ve had keyboards in the past where the failure mode was the USB socket breaking, and replacing the microcontrollers (or reconfiguring the keyboard to connect from the other half) was more of a pain than I would like.

Similarly, there are some designs which are difficult to fix when a single component fails.

I like the idea of a “forever keyboard” that will serve you for decades with minimal maintenance. The microcontroller being on a separate PCB and easily swappable makes the whole setup quick and easy to fix in the future.

All the solder joints should be easy to access, solder or desolder without special tools. The case should be easy to make with any 3d printer.

### Function over form

Many keyboard designs prioritize minimalistic wireless aesthetics over ergonomics or other aspects of the build.

Revolt is aiming for the best long-term experience for the keyboard’s users, builders and developers while sporting an unapologetically utilitarian look.

### Easy to iterate on and (partially) upgrade

Usually the keyboard you first build/buy is the keyboard you’re stuck with, with the exception of changing switches or keycaps.

With Revolt you can keep the sides to experiment with different pointing devices in the center part, or keep the center part and play with different layouts in your left/right parts while keeping the center part that works for you. All that with minimal effort and cost.

With a standardized connection between the commander board and the input parts it’s easier, quicker and cheaper to iterate on the individual aspects of the keyboard. Want to try a new pointing device? Make some small changes to the commander board and solder it together without changing your input parts. Got an idea for a better key layout? You can make a revision of the input pcb without ever touching the microcontroller.

### Ease of layout changes / firmware programming

With most split keyboards, when you update your layout, you need to flash the firmware in both halves of the keyboard, which can be a pain and require some cable juggling. And you will be messing with the layout when you first get the keyboard :D

With a single microcontroller you don’t need to reconnect anything, you just reset the keyboard, flash it, and you’re done!

### Open source

It took a lot of open source work (KiCad, QMK, footprint libraries, microcontrollers) to make designing keyboards as easy and fun as it is right now. I’d like to pay it forward by reducing the barrier of entry for people to make a keyboard they’ll love using.

I might consider selling pre-made Revolt components, but the designs will always be open-source and anyone will be able their own unit from scratch.

## How is it different from Sofle/Lily58/Corne?

1. It has 68 keys (as opposed to 42 in Corne, 58 in Sofle and Lily58). It allows for `CTRL` and `META/WIN/CMD` keys in their regular location, arrow keys in the first layer and basically all of TKL ISO 104 keys, minus the function row and some of the  `HOME` / `END` / `PGUP` / `PGDOWN` keys
2. It has more thumb keys, in easy to reach locations
3. It uses just one microcontroller, making it easier to change the the layout/firmware

## How is it different from Redox?

1. It can be lower profile since the microcontroller isn’t mounted under the PCBs and Revolt v1 is designed with Kailh Choc switches in mind
2. It uses exclusively 1u keys, making it easier and cheaper to buy a keycap set for it. The 1.5u keys in Redox don’t have much of a benefit, but they make the overall keyboard dimensions bigger.
3. The pinky keys are placed lower to make them easier to reach - I struggle to press `Q` with my pinky on my Redox
4. All solder joints are accessible without the need to desolder the microcontroller
5. It uses just one microcontroller, making it easier to change the the layout/firmware

### How is it different from Zodiark?

> ⚠️ TODO
