# HSBUV Board with Nuvoton NPCM7mnx RunBMC module Quick (Standalone) Setup Guide 

# Table of Contents
- [Module Overview](#module-overview)
- [Quick Setup](#quick-setup)
  * [Power-On and Reset](#power-on-and-reset)
  * [USB-to-UART5 for BMC debug console](#usb-to-uart5-for-bmc-debug-console)
  * [Terminal](#terminal)
  * [VGA Display](#vga-display)
- [Build OpenBMC](#build-openbmc)
- [OpenBMC WebUI](#openbmc-webui)
- [FUP Mode for Emergency Firmware Update](#fup-mode-for-emergency-firmware-update)

# Module Overview

<img align="center" width="100%" src="https://raw.githubusercontent.com/linkunfa/TestRepo/main/module_overview.png">

# Quick Setup
## Power-On and Reset

1. Connect the 12V power supply to power jack J301. The power supply should be 12V and at least 2A; the jack should be 2.5 x 5.5 x 9.5mm in diameter.
2. Press and release Power-On-Reset (SW1801) push-button.

## USB-to-UART5 for BMC debug console

1. Download and install the USB-to-UART driver according to the host OS ([http://www.ftdichip.com/Drivers/VCP.htm](http://www.ftdichip.com/Drivers/VCP.htm)).
2. Connect a mini-USB cable between the PC host and HSBUV Micro USB UART5 J2001 (which connects to BMC serial interface 2, uboot and kernel terminal messages are sent through this port).
3. Wait for FTDI driver to be installed automatically and the COM port number will be assigned once installation done.
4. Check and verify D2008 LED light is ON.

## Terminal

1. Open a terminal (e.g., Tera Term) and set the correct COM port number assigned by the FTDI driver, then configure the COM port to 115200 Kbps, 8 data bits, 1 stop bit, no parity and no flow control.

<img align="center" width="35%" src="https://raw.githubusercontent.com/linkunfa/TestRepo/main/teraterm.png">

2. Press and release Power-On-Reset (SW1801) push-button.
3. Hit any key to stop autoboot and enter into uboot environment.

<img align="center" width="35%" src="https://raw.githubusercontent.com/linkunfa/TestRepo/main/uboot.png">

## VGA Display

# Build OpenBMC

# OpenBMC WebUI

# FUP Mode for Emergency Firmware Update
