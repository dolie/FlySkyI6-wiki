# FlySkyI6 Development

## Toolchain ##

The firmware is compiled with `arm-none-eabi` GCC toolchain. Install
`gcc` and `binutils` for `arm-none-eabi` on your system, as well as
`make`.

## Build using `make` ##

* clone the FlySkyI6 repository
* go to the `source/build` directory
* run `make all` or `make all-swe`, depending on the firmware
  version you want to build (for an unmodified hardware or for
Tx with [added SwE switch](HW-Mod-SwE))
* The `fs-i6_updater-MM-DD-HH-MI.bin` or `fs-i6-swe_updater-MM-DD-HH-MI.bin` is the resuilting file for [installing](Install) with mhils' `updater` utility.

## Hacking the C code ##

Note that this is _not_ a project written fully in C.
It is just a bunch of C and ASM routines binary-patched
to the original FlySky binary firmware.

The memory inside the MCU is very tight, and it might well be that the
modification of C code will result in the new version of the binary
code being too big for the dedicated space. In that case, you get the
_sections overlap_ error while linking.

In that case, you might want to modify the placement of the C routines
in the final binary in the linking script `source/MKL16Z64xxx4_flash.ld`.
Have a look at `fs-i6.map` or `fs-i6-swe.map` file in the `source/build`
directory to obtain the sizes of varions code sections.

## ASM ##

_NOTE: this is a copy of the `development.md` file from the code repository_

ASM compilation:

`arm-none-eabi-as.exe -o fsi6.o fsi6.asm -mcpu=cortex-m0plus -mthumb -g3`

`arm-none-eabi-objcopy.exe -O binary fsi6.o fsi6.bin`

Docummented disassembly can be found in ASM/10ch.0x0000

Documentation was created with use modified script 

http://magiclantern.wikia.com/wiki/GPL_Tools/disasm.py

It is also to possibile to compile some parts of modifyed firmware with gcc (all c files are in source directory).
The project was originally compiled with Freescale Kinetics. 

Compiled elements must be replaced later in original file (addresses are described in source/MKL16Z64xxx4_flash.ld)
Current linker script is not able to combine compilation results and old FW.
Command used for compilation (extraced from Freescale Kinetics)

`arm-none-eabi-gcc -mcpu=cortex-m0plus -mthumb -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -Wall  -g -D"CPU_MKL16Z64VLH4" -I../startup -I../board -I../utilities -I../CMSIS -I../drivers -std=gnu99 -MMD -MP -MF"source/file.d" -MT"source/file.o" -c -o "source/file.o" "../source/file.c"`

