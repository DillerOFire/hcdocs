# Basic guides about Ace 3V & Nord 4

**Please save this [OneDrive link](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp), because you can't bookmark the page to access it again due to Microsoft.**

Sometimes open the readme html file directly in OneDrive webpage might cause photos and videos failed to load, download & open the html file locally to solve this problem.

This readme might be updated if something worthy happens
The whole article is based upon the assumption that you readers are not familiar with Android stuff, so I'm trying to tell everything you need to know

It's quite important to **gather all information before action**, **panic will always lead to brick\!**

**For those guys already fucked up:**
**READ README FILES NEXT TIME\!\!\!**
[Go to Unbrick chapter](https://www.google.com/search?q=%23unbrick)

\<details\>\<summary\>About the author\</summary\>
Hi I'm [invalid URL removed], a literally nobody
Comparing to **REAL DEVS** like [invalid URL removed], [invalid URL removed] or [是小菜菜吖](https://www.google.com/search?q=https://t.me/oxygenports), I'm doing literally nothing. Do remember to subscribe these guys\!

Those devs might have a bad temper, might be rude talking, but they're doing something, which is much better than me.

Respect.

\</details\>

\<details\>\<summary\>CC BY-NC-SA License that nobody cares XD\</summary\>
[Basic guides about Ace 3V & Nord 4](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp) © 2025 by [invalid URL removed], [꽉스레](https://www.google.com/search?q=https://t.me/quxngisoverparty), [Kks](https://www.google.com/search?q=https://t.me/Kx2sK), [invalid URL removed], [invalid URL removed], [invalid URL removed] and lot more other helpers, is licensed under [invalid URL removed]
\</details\>

-----

## Chat groups of Ace 3V

**YAAP** for Ace 3V already has several releases. It supports fingerprint now, though still lacks some feature & has some minor bugs sometimes.
There's two groups in Telegram, [Holoction Ace 3V](https://www.google.com/search?q=https://t.me/sfiercht) and [Holoction audi (abandoning)](https://www.google.com/search?q=https://t.me/yaapaudi), join the group to have a chat\! 😘

> \<s\>update 2024-09-10: dev of YAAP for Ace 3V is paused due to dev's real life issue, hopefully it'll continue in 1 \~ 2 months\</s\>
> \<s\>update 2024-11-08: YAAP continues to update since 2024-10-27, but fingerprint issues hasn't solved yet\</s\>, NFC issues fixed
> update 2025-02-19: fingerprint solved, but some minor bugs still exists - already quite okay for daily use
> update 2025-03-18: zero- soft reboot bug fixed

**"** Official **"** [Telegram group](https://t.me/OnePlusNord4_Official) of Ace 3V / Nord 4

> Note: Not an official channel of OPlus actually, it's just the chat's name though

**TWRP** for audi, **ColorOS Pro** and the very first OxygenOS port (has lotta bugs although) are made by [@color597 from Telegram](https://www.google.com/search?q=https://t.me/color597), you can find him in [CoolAPK](https://www.google.com/search?q=http://www.coolapk.com/u/642425) too.

## Model Info

| device name | code name | model         | cROMs                                       |
| :---------- | :-------- | :------------ | :------------------------------------------ |
| Ace 3V      | audi      | PJF110        | YAAP(usable) PixelOS(declared to build?)    |
| Nord 4      | avalon    | CPH2661 or CPH2663 | LOS & other (not yet published?)            |

2025-03-13: [quxng](https://www.google.com/search?q=https://t.me/sfiercht/26895) might gonna build another cROM (PixelOS) for Ace 3V?

-----

## Practical tips & Instructions

> This part is still remain to be done, [contact me](https://www.google.com/search?q=https://t.me/lazaruX512) if you have any suggestions\!
> Personal Message might not replied, you can find me in [YAAP group](https://www.google.com/search?q=https://t.me/sfiercht) too

### File system of Android & some basic info of root

**Extract** all **partitions** from a ROM pack is important for us to understand the Android system, and kinda same if you simply want to **root** your device.
To do this, I would recommend **Daxiaamu's Super Payload Dumper Py**.
I've put it in [my OD (OneDrive) repo](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp), you can access his [original post](https://optool.daxiaamu.com/super_payload_dumper) too
(download from his page seems required to login Baidu Netdisk)

\<iframe src="[invalid URL removed]" width="580" height="320" frameborder="0" scrolling="no" allowfullscreen=""\>\</iframe\>

This video above shows you how to extract - drag your zip pack to `unpack.exe` - easy to use.
You can also rename the `unpack.exe` as `(partition name).exe` to extract a specific partition you want.
For example, `init_boot.exe` will extract `init_boot` partition - this partition is important to root your devices, more on that later.

-----

Windows 10/11 has only 3 partitions if you make a fresh install on a new hard disk.
Comparing to Windows, Linux (e.g.: Android), has quite a lot partitions.

This screenshot above shows how many partitions are there in YAAP for Ace 3V, partitions such as `modem` is critical to communicate.
Some others might related to performance, for example, `vendor_boot` will be modified if you use **KonaBess** to tune GPU frequency and voltage.

> KonaBess is a software to fine tuning **GPU frequency** & **voltage** just for **Qualcomm Adreno**.
> Thou you **can't overclocking** your GPU **since Snapdragon 870**. You can still **undervolte** your GPU to **reduce heat** and **power drain**. It's an useful app for gamers pushing their devices for extreme.
> KonaBess can be found on [GitHub](https://github.com/libxzr/KonaBess).
> If not unfamiliar with it, you can find an example of KonaBess tune **[at here](https://www.google.com/search?q=https://t.me/nrk3x/52)**.
> Thanks to [米饭菌 @ CoolAPK](https://www.google.com/search?q=https://www.coolapk.com/feed/59266258) for providing another KonaBess ref tune for me.

For devices like Ace 3V running on Android later than 13, while using [KernalSU](https://github.com/tiann/KernelSU/releases), **`init_boot`** is the partition to patch
But on Android 12 (or older), patch `boot` partition instead

Anyway, let's keep talking about file system.

Motorola is different than OnePlus, as this zip extraction from official ROM file of Moto Edge 20 Pro, some brands won't provide a regular upgrade pack.

However, this shows your the another aspect of Android file system, some important partitions are missing, such as `system`, `product`, `vendor` ...
It seems quite different than YAAP's dump.

Actually, some partitions are inside a large dynamic partition - `super`, this'll help a relativly new Android device to upgrade system easier.

> In TWRP for Ace 3V, "flash image to `system`" option isn't provided, you can only flash image to `super` instead - which makes GSI flashing in this TWRP not so easy.
> Also, ADB sideload function of TWRP seems have problem working, at least you can't sideload the YAAP zip pack on it
> **recovery of YAAP** could be a solution if you screw up - you can find it on my [OD repo](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp) too.

### Install drivers & ADB

> Before entering bootloader & unlock, we need to install driver and ADB kit.

  * Install drivers
    > Any Android driver should be okay. They should be compatible, no matter the brand.
    > I would personally recommend [Motorola Android drivers](https://en-us.support.motorola.com/app/usb-drivers)
    > **If you unable to detect device in bootloader mode, go install drivers**
  * Install ADB kit
      * [Download the file](https://www.google.com/search?q=https://developer.android.com/tools/releases/platform-tools%23downloads) & unzip
      * \<details\>\<summary\>Add ADB folder to system path \<b\>(click to expand)\</b\>\</summary\>
        Settings -\> About -\> Advanced System Settings
        System Properties -\> Advanced -\> Environmental Variables
        System Variables -\> Path -\> Edit
        type in your adb folder
        \</details\>

### Unlock Bootloader

\<details\>\<summary\>Check lists\</summary\>

1.  Driver & ADB installed ([invalid URL removed])
    \</details\>

2.  Turn on developer options

3.  Settings -\> System -\> Developer options -\> OEM unlocking

4.  reboot to bootloader (either way)

      * ADB command
        1.  `adb reboot bootloader`
      * button combo
        1.  turn off
        2.  volume down + power button

5.  unlock uncritical

    1.  `fastboot flashing unlock`
    2.  select yes via volume button & choose via power button

6.  unlock critical

    1.  `fastboot flashing unlock_critical`
    2.  select yes via volume button & choose via power button

### Install TWRP (optional / not recommend for YAAP)

\<details\>\<summary\>Check lists\</summary\>

1.  Driver & ADB installed ([invalid URL removed])

2.  Bootloader unlocked ([invalid URL removed])
    \</details\>

3.  Download from [Telegram orginal posts](https://t.me/colorospro/331) or my [OD repo](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp)

4.  enter bootloader `adb reboot bootloader`

5.  `fastboot flash recovery TWRP_rec_file_name`

### Install YAAP (hoping for more cROMs)

> [Video instruction by 霖夕Linx](https://www.google.com/search?q=https://www.bilibili.com/video/BV1UukpYWELP)（Bilibili）

\<details\>\<summary\>Check lists\</summary\>

1.  Driver & ADB installed ([invalid URL removed])

2.  Bootloader unlocked ([invalid URL removed])
    \</details\>

3.  Download YAAP update pack & recovery (either way)

      * Download from my [OD repo](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp)
        > By this way you can save server fee for VSRP : )
          * find recovery and update pack from `\Ace 3V\YAAP by VSRP`,
            older build can be found under `obsolete` folder
      * Download from [holoction.ru](http://holoction.ru)
          * YAAP recovery file name be like `yaap_audi-recovery.img`
          * YAAP update pack file name be like `yf_audi-ota.zip`

4.  Install recovery

    1.  reboot to bootloader `adb reboot bootloader`
    2.  `fastboot flash recovery yaap_rec_img_name`

5.  enter recovery & install YAAP

    1.  reboot to recovery (either way)
          * choose `reboot to recovery` in bootloader menu
          * `fastboot reboot recovery`
    2.  choose `Apply update from ADB` in recovery
    3.  `adb sideload yaap_update_pack_name`

6.  Enjoy\!

### Back to ColorOS

  * backup your data
  * download 14.1.0 downgrade pack from [OneDrive repo](https://www.google.com/search?q=https://1drv.ms/f/s!AoleZooDdfAx5QuFC1oYTZ2VuuJp) `\Ace 3V\Official ROM`
  * find a USB drive, put downgrade pack into it
  * Install TWRP `fastboot flash recovery TWRP_path`
  * Enter recovery, Install, find the path of your downgrade pack, install with data wipe

### Unbrick

  * If you still abled to enter bootloader
    Use [Bootloader Flash Tool](https://www.google.com/search?q=https://t.me/gt3neo5hub/521/207068)
      * Connect the Phone in Fastboot Mode
          * Put your phone in Fastboot mode and connect it to your PC
          * Open the ADB Fastboot CMD terminal and type `fastboot devices`
          * Verify that your device is recognized by checking for its serial number
      * Set Up the Flashing Tool
          * Download and set up the flashing tool
        > download from [orginal post](https://www.google.com/search?q=https://t.me/gt3neo5hub/521/207068) or from OneDrive repo
          * Open the tool and navigate to the Firmware Unpacker section
      * Unpack the Stock ROM
          * Select the full stock ROM ZIP file (not an incremental update) that you want to flash
          * In the Mode section, select Full, and then click Press to Unpack to extract the firmware
      * Flash the Firmware
          * After unpacking, go to the Firmware Flasher section
          * Click on Press to Flash and carefully follow the on-screen instructions during the flashing process
      * Complete and Revert to Stock ROM
          * Once the flashing process is complete, your phone will revert to the stock ROM
          * Enjoy the reverted stock experience
  * Black bricked (9008)
      * (Recommend) **GO TO YOUR LOCAL SELLER OF OPLUS**
      * OPlus unofficial unbrick tool
        > someone is publishing the OPlus 9008 auth code, but he's now under pressure, so you might need to purchase auth code from somewhere else, maybe from *Goofish*?

## Useful commands

```shell
adb devices # detect booted devices
adb reboot bootloader
fastboot devices # detect fastbootd & bootloader devices
fastboot flashing unlock # allow you to flash some partition
fastboot flashing unlock_critical # allow you to flash other partiitions
#                       ↓ remember leave a blank space between "init_boot" and file name
fastboot flash init_boot # then drag in init_boot, patched or not, into here
fastboot flash recovery # drag in img file, yaap or other recovery is okay
# to flash some partitions, you have to enter fastbootd
fastboot reboot fastboot # enter fastbootd by reboot to fastboot ... fuck android
# flash GSI ↓
fastboot --disable-verity --disable-verification flash vbmeta (partition_image)

# flash img to both slot, don't do this except you're sure this image is fine-to-use
fastboot flash --slot=all partition img_name.img
```

## Gaming Stuff

  * YAAP build 20250220, Genshin American server, 30 mins Sumeru city running (LazaruX512)

    \<details\>\<summary\>\<b\>(click to expand)\</b\>\</summary\>

      * System & environment
          * YAAP build 202050220
          * [KonaBess tuned](https://www.google.com/search?q=https://t.me/nrk3x/52), Scene 4 at default settings
          * 5G & HotSpot turned on
          * 13℃ room temperature
          * no external controller
      * Graphics Settings
      * Sensor / System logs
          * Battery cost: \~ 30%
          * Terminal Temperature: 42.6℃
          * Terminal Frame rate: \~ 60fps
          * Lowest Frame rate displayed in the chart: \~ 45 fps
          * fps drops at first several minutes are during game loading
      * Typical Route Loop:
          * Sayu & Kirara, route 1, the pink line, Skill dash
          * Mizuki, route 2, Skill dash
          * Mizuki, route 3, run
          * Lan Yan, route 4, Skill dash
          * Lan Yan, route 5, Glide back
      * Issues:
          * touch control glitch in high temperature
          * too hot
          * failed to launch Genshin after test, fixed after deactivate Scene
      * Miscs:
          * Motion Blur & Bloom turned off - not burnnin my eyes
          * Why not use Yelan - I don't have one 😖
            \<s\>I'd be happy if you support me to pull one\</s\> (just kiddin, I don't need support)
            \</details\>

  * HSR ColorOS & OOS 15 port by Kx2sK @ Telegram

    \<details\>\<summary\>\<b\>(click to expand)\</b\>\</summary\>
    I was playing a HoYoverse game.
    The game was mainly running on StockROM. I played a few of them at OOS15 as well.

    In the Honkai-star-rail and later games, it felt tough to play at the highest settings. It is recommended to lower some settings such as shadows.

    I don't think the FPS dropped suddenly. Maybe it's because I was using Scene.

    \</details\>

  * Punishing Gray Raven by lalalalayangre @ Telegram

    \<details\>\<summary\>\<b\>(click to expand)\</b\>\</summary\>
    Punishing Gray Raven only, not a high graphical spec game, no lags
    *LazaruX512: ROM didn't mentioned*
    \</details\>

## YAAP for Ace 3V (audi)

  * basic info
      * Yaap might be unmaintained in future
      * Builds here can have critical
        > by lazarux512: no much critical bugs actually (at least until build 20241027),
        > may have some minor issues though
      * Dedicated to **Ace 3V** only
      * If you want me to not forget about bug you've found, then report it in details on \<s\>[GitHub issues](https://www.google.com/search?q=https://github.com/holoction-audi)\</s\> [Telegram Group](https://www.google.com/search?q=https://t.me/sfiercht)
      * Gapps included
  * \<details\>\<summary\>builds update log \<b\>(click to expand)\</b\>\</summary\>
      * build 20240901
          * metadata
              * [post-sdk-level] `34`
              * [post-security-patch-level] `2024-08-05`
          * Changes
              * playback freeze seems was fixed somehow
      * build 20240920
          * metadata
              * [post-sdk-level] `34`
              * [post-security-patch-level] `2024-08-05`
          * Changes
              * improved perfomance
              * also switched to erofs
              * nothingburger fixed
      * build 20241017 (first Android 15?)
          * metadata
              * [post-sdk-level] `35`
              * [post-security-patch-level] `2024-10-05`
      * build 20241027
          * metadata
              * [post-sdk-level] `35`
              * [post-security-patch-level] `2024-10-05`
          * Changes
              * nfc fix
              * performance fixes
          * Known issues
              * No fingerprint auth
              * SEpolicy permissive
      * build 20241212
          * **REMEMBER TO DOWNGRADE TO COS 14 FIRMWARE BEFORE THE FLASH**
          * Changes
              * fixed charge rate
              * updated sources
      * build 20241231
          * Changes
              * qpr merge
          * Known issues:
              * No fingerprint auth
              * Sepolicy permissive
      * build 20250218
          * Changes
              * update merge
              * fingerprint fix
              * richtap vibro
              * cos 15 Firmware update
          * Known issues
              * You probably won't like new haptics
              * double tap to wake
              * Sepolicy permissive
              * night light
      * build 20250219 & 20250220 (2 hotfixes)
          * synced all display props to stock
          * Fugg seems problem still persist
      * build 20250318
          * updated sources
          * fixed low brightness reboots
            \</details\>

## Official ROM packs

> Since 2025, Official ROM links will display error if you download it using browser, but it's still downloadable
> [Kks](https://www.google.com/search?q=https://t.me/Kx2sK) mentioned, download ROM via [1DM](https://play.google.com/store/apps/details?id=idm.internet.download.manager) is still okay
> [꽉스레](https://www.google.com/search?q=https://t.me/quxngisoverparty) mentioned that you can use wget / curl to download

  * Ace 3V
    > TG user Kx2sK extracted a rollback pack from ColorOS Assistant, it's based on ColorOS **A.40**, it should be okay to flash via **TWRP**
    > If you find the local update button in gray, you shall disconnect all the network
    > \<details\>\<summary\>version details \<b\>(tap to expand)\</b\>\</summary\>
      * PJF110\_14.0.1.630(CN01) official ROM
          * [ColorOS Version] ColorOS 14.1.0
          * [Security patch level] `2024-06-05`
          * [OTA version] `PJF110_11.A.40_0400_202406070217`
          * [File size] `6.93 GB (7,444,426,919)`
          * [MD5] `785ae032aed41c707aea8d5076cb3604`
          * [[invalid URL removed]]
      * PJF110\_14.0.1.700(CN01) official ROM
          * [ColorOS Version] ColorOS 14.1.0
          * [Security patch level] `2024-08-05`
          * [OTA version] `PJF110_11.A.45_0450_202408151756`
          * [File size] `6.93 GB (7,442,441,981)`
          * [MD5] `d49a914f3bfa67cba17df50336ae5058`
          * [[invalid URL removed]]
      * PJF110\_14.0.1.710(CN01) official ROM
          * [ColorOS Version] ColorOS 14.1.0
          * [Security patch level] `2024-09-05`
          * [OTA version] `PJF110_11.A.46_0460_202409121808`
          * [File size] `6.90 GB 