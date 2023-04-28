---
sidebar_position: 2
---

# OnePlus Ace general rom installation

## Very general warn
After these steps you'll get worse experience than stock and should wait till everything fixed.
Returning to stock may be hard but possible, I may write a script for this but for now there's no easy way to do this!

## Prepare your pc
- Just be sure you installed latest platform-tools and can access `adb` and `fastboot` commands.

## Prepare your device

- Be sure you installed OxygenOS 13 (c.15, c.18, c.19) on both slots
- - Just Install through local update the same version (yeah it works)
- - If you updated from OxygenOS 12 just reflash same version again.
- Ensure your bootloader is unlocked
- Connect your phone to pc and enbable adb through developer options
- After your adb authed run `adb reboot bootloader` command.

### Warning!!! These steps are dangerous and can brick your device, so be sure you are prepared

- Install rom provided vendor_boot on both slots `fastboot flash --slot=all vendor_boot vendor_boot.img`
- Reboot to rom recovery by `fastboot reboot recovery`
- ???
- Done!

## ROM Installation process

- Wipe your system by *Wipe Data/Factory Reset* menu option
- Enter sideloading mode by *Install update through ADB* menu option
- Be sure you're connected to your PC
- Run `adb sideload *path/to/flashing/zip/file*`
- Wait till process done
- ???
- Reboot and enjoy custom ROM experience (づ ◕‿◕ )づ

![hcopption](/img/hctionoppo.png)