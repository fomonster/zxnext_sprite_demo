# Demonstration of zxnext_sprite

The **zxnext_sprite_demo** project contains a simple example program demonstrating
how to use the [zxnext_sprite](https://github.com/stefanbylund/zxnext_sprite) C
hardware sprite API for the Sinclair ZX Spectrum Next.

## Download

The latest version of this program can be downloaded **[here](build/zxnext_sprite_demo.zip)**.
This download contains the following binaries and resources:

* zxnext_sprite_demo/zxnext_sprite_demo.tap
* zxnext_sprite_demo/zxnext_sprite_demo.sna
* zxnext_sprite_demo/zxnext_sprite_demo.c
* zxnext_sprite_demo/readme.txt

The included readme.txt file explains how to start the program.

If you want to build the zxnext_sprite_demo program yourself, see the "How to Build"
section below.

## How to Build

If you want to build the zxnext_sprite_demo program yourself, follow the steps
below:

1. On Windows, you need [MinGW](http://www.mingw.org/),
[UnxUtils](https://sourceforge.net/projects/unxutils/) or
[Cygwin](https://www.cygwin.com/) for the basic Unix commands. Add the chosen
set of Unix commands to your path.

2. Install the latest version of [z88dk](https://github.com/z88dk/z88dk) and the
[ZEsarUX](https://sourceforge.net/projects/zesarux/) or
[CSpect](https://dailly.blogspot.se/) emulator.

3. Download [zxnext_sprite](https://github.com/stefanbylund/zxnext_sprite/blob/master/build/zxnext_sprite.zip)
and unpack it in a suitable place.

4. Download the zxnext_sprite_demo repository either as a ZIP archive using the
"Clone or download" button at the top of this page or with Git using the
following command:

> git clone https://github.com/stefanbylund/zxnext_sprite_demo.git

5. Make sure the zxnext_sprite and zxnext_sprite_demo directories are located in
a common parent directory.

6. Go to the zxnext_sprite_demo directory and enter the following command to
build a TAP file or an SNA file if BUILD_SNA=true is specified:

> make all [BUILD_SNA=true]

7. Run the zxnext_sprite_demo/bin/\<compiler-flavour\>/zxnext_sprite_demo.tap
file in the ZEsarUX emulator or the
zxnext_sprite_demo/bin/\<compiler-flavour\>/zxnext_sprite_demo.sna file in the
CSpect emulator.

**Note:** Since the Sinclair ZX Spectrum Next is still under development and all
tools need to catch up with the latest specs, it is important to use the latest
version of zxnext_sprite, z88dk and ZEsarUX or CSpect.

**Tip:** If you don't care for makefiles or don't want to install
MinGW/UnxUtils/Cygwin on Windows, you can build zxnext_sprite_demo manually
by using the z88dk command-line invocation located in the header of the
zxnext_sprite_demo.c source file.

**Tip:** To start the ZEsarUX emulator directly in Sinclair ZX Spectrum Next
mode, start it with the following options:

> zesarux --machine tbblue --enable-mmc --enable-divmmc-ports --mmc-file tbblue.mmc --quickexit

**Tip:** To start the CSpect emulator directly in Sinclair ZX Spectrum Next
mode, start it with the following options:

> CSpect -zxnext -mmc=<zxnext_sprite_demo_folder> zxnext_sprite_demo.sna

## License

This software is licensed under the terms of the MIT license.
