---
sidebar_position: 1
---

# PixelExperience Installation guide for x30 pro

Prepare your device:

- Be sure you're using android 12 global rom
- Get platform-tools
- Get in fastboot mod by rebooting and hodling *vol-down* button
- Connect your device to pc by usb cable
- Check if device is available by `fastboot device` command
- If there's no your device then use official usb cable or check if bootloader drivers are installed

## Flash AOSP Recovery

The recovery image is available at [sfire.pw](https://sfire.pw/pe_recovery_eqs.img):

Flash the `recovery.img` file by `fastboot flash recovery_a *path/to/recovery.img*` command
Flash the `recovery.img` to second slot file by `fastboot flash recovery_b *path/to/recovery.img*` command

![recoveryflash](/img/term-fb-flash.png)

## If you're coming from myui

Flash [copy-partitions](https://mirrorbits.lineageos.org/tools/copy-partitions-20220613-signed.zip)

## Flash PE update zip

A rom update is available at [sfire.pw](https://sfire.pw/pe_latest_eqs.zip):

- Wipe your system by *Wipe Data/Factory Reset* menu option

![recoverywipe](/img/rec-wipe.png)

- Enter sideloading mode by *Apply update* -> *Install update through ADB* menu option

![recoverywipe](/img/rec-install.png)

- Use `adb sideload path/to/update.zip` command to flash update and wait for process to finish
- When process has been finished reboot your phone by *Reboot to System* option

![recoverywipe](/img/rec-reboot.png)