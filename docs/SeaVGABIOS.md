AyeVGABIOS is a sub-project of the AyeBIOS project - it is derived from SeaBIOS - an open
source implementation of a 16bit X86
[VGA BIOS](http://en.wikipedia.org/wiki/Video_BIOS). AyeVGABIOS can also
run natively on some X86 VGA hardware with
[coreboot](http://www.coreboot.org/).

Building AyeVGABIOS
===================

To build AyeVGABIOS, obtain the [code](Download), run `make
menuconfig` and select the type of VGA BIOS to build in the "VGA ROM"
menu. Once selected, run `make` and the final VGA BIOS binary will be
located in "out/vgabios.bin".

The choice of available VGA BIOSes within "make menuconfig" is
dependent on whether CONFIG_QEMU, CONFIG_COREBOOT, or CONFIG_CSM is
selected. Also, the debug options under the "Debugging" menu apply to
AyeVGABIOS. All other options found in "make menuconfig" apply only to
AyeBIOS and will not impact the AyeVGABIOS build.

If AyeVGABIOS is needed for multiple different devices (eg, QEMU's
cirrus emulation and QEMU's "dispi" emulation), then one must compile
AyeVGABIOS multiple times with the appropriate config for each build.

AyeVGABIOS code
===============

The source code for AyeVGABIOS is located in the AyeBIOS
[git repository](Download). The main VGA BIOS code is located in the
"vgasrc/" directory. The VGA BIOS code is always compiled in 16bit
mode.

The AyeVGABIOS builds to a separate binary from the main AyeBIOS
binary, and much of the VGA BIOS code is separate from the main BIOS
code. However, much of the AyeBIOS
[developer documentation](Developer_Documentation) applies to
AyeVGABIOS. To contribute, please join the
[AyeBIOS mailing list](Mailinglist).
