---
sidebar_position: 1
---

# hOS Installation guide for lavender

Prepare your device:

- Get platform-tools
- Get in fastboot mod by rebooting and hodling *vol-down* button
- Connect your device to pc by usb cable
- Check if device is available by `fastboot device` command
- If there's no your device then use official usb cable or check if bootloader drivers are installed

## Flash AOSP Recovery

The recovery image is available at [holoction.ru](https://holoction.ru):

Flash the `recovery.img` file by `fastboot flash recovery *path/to/recovery.img*` command

![recoveryflash](/img/term-fb-flash.png)

## Flash hOS update zip

A rom update is available at [holoction.ru](https://holoction.ru):

- Reboot to recovery mode by hodling *vol-up* button
- To exit **no command** mode press *power* and *vol-up* buttons
- For selecting menu options use **volume buttons**
- For entering command use **power button**
- Wipe your system by *Wipe Data/Factory Reset* menu option

![recoverywipe](/img/rec-wipe.png)

- Enter sideloading mode by *Install update through ADB* menu option

![recoverywipe](/img/rec-install.png)

- Use `adb sideload path/to/update.zip` command to flash update and wait for process to finish
- When process has been finished reboot your phone by *Reboot to System* option

![recoverywipe](/img/rec-reboot.png)