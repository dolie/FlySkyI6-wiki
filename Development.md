# FlySkyI6 Development

## Toolchain ##

The firmware is compiled with `arm-none-eabi` GCC toolchain.

## Build using `make` ##

The firmware can be buid with `make all` and `make all-swe`
(the [SwE](HW-Mod-SwE) version) executed in the `source/build` directory.
The result should be the firmware files for mhils' updater (`*_updater_*.bin`)
and some other files (`*.map`, for example).

## ASM ##

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

