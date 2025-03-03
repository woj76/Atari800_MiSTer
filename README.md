# Atari [5200](https://en.wikipedia.org/wiki/Atari_5200) and [Atari 800/800XL/65XE/130XE](https://en.wikipedia.org/wiki/Atari_8-bit_family) for [MiSTer Platform](https://github.com/MiSTer-devel/Main_MiSTer/wiki)

### This is the port of [Atari 800XL core by Mark Watson](http://www.64kib.com/redmine/projects/eclairexl)

### Installation
* Copy the *.rbf file to the root of the system SD card.
* Copy the files to Atari800/Atari5200 folder

## Usage notes

### System ROM
You can supply other A800 XL OS ROM as games/ATARI800/boot.rom. 
Alternative Basic ROM can be placed to games/ATARI800/boot1.rom. 
Alternative A800 OS-A ROM as games/ATARI800/boot2.rom.
Alternative A800 OS-B ROM as games/ATARI800/boot3.rom.

Integrated OS ROMs include SIO turbo patch (fast disk loading). Note that the single fact that this patch is present can break some titles, especially the timing sensitive ATX disk based ones.

Turbo ROM has hot keys to control the turbo mode:
* SHIFT+CONTROL+N    Disable highspeed SIO (normal speed)
* SHIFT+CONTROL+H    Enable highspeed SIO 
  
Additionally, you can control the speed of turbo loading in OSD menu.

### Disks
A800: After mounting the disk, press F10 to boot.
Some games don't like the Basic ROM. Keep F8(Option) pressed while pressing F10 to skip the Basic.
You can also boot a disk directly from the D1: drive using the first menu entry, the F10 Reset and F8 Option keys are applied automatically, any mounted carts are unmounted.
For ATX disk titles that are timing sensitive, you may also want to try to change the emulated drive timing between the older 810 disk drive, and the XL line 1050 one (this does not apply at all to non-ATX titles, the option has no effect). Moreover, some ATX titles will only load on the PAL or NTSC machine only, depending on which system they were designed for.

### Executable files
A800: There is an entry to directly load the Atari OS executable files (the so called XEX files) using a high-speed direct memory access loader.
If a title does not load, you may want to try to switch the loader location in Atari memory (Standard - it sits at 0x700, Stack - it is located at the bottom of the stack area at 0x100).

### Classic Atari 800 mode
When selecting OS-B in the Machine/BIOS menu option, the core works in the classic Atari 800 mode, and different memory layouts are available / activated. Note that the 52KB memory layout is not compatible with the stock 800 OS-A/B system, it freezes the boot process. This is not a core bug, but an Atari 800 legacy.

### Differences from original version
* Joystick/Paddle mode switched by joystick. Press **Paddle1/2** to switch to paddle mode (analog X/Y). Press **Fire** to switch to joystick mode (digital X/Y).
* Use ` key as a **Brake** on reduced keyboards.
* Cursor keys are mapped to Atari cursor keys.
* PAL/NTSC mode switch in settings menu (A800)
* Video aspect ratio switch in settings menu
* Switchable side clipping of the video output to hide the GTIA "garbage". 
* An option to turn off the hi-res Antic extension from the original core, which brakes some titles.
* Some optimizations and tweaks in file selector and settings menu navigation.
* Standard OSD menu for cartridge/disk selection.
* Mouse emulates analog joystick(Atari 5200) and paddles(Atari 800).
* Fire 2 and Fire 3 on joystick.

### Disable Basic ROM by Joystick.
Fire 2 on joystick acts as an OPTION key while reboot. It's valid only 2 seconds after reboot. After that Fire 2 doesn't affect the OPTION key.

### More info
See more info in original [instructions](https://github.com/MiSTer-devel/Atari800_MiSTer/tree/master/instructions.txt)
and original [manual](https://github.com/MiSTer-devel/Atari800_MiSTer/tree/master/manual.pdf).

## Download precompiled binaries
Go to [releases](https://github.com/MiSTer-devel/Atari800_MiSTer/tree/master/releases) folder.
