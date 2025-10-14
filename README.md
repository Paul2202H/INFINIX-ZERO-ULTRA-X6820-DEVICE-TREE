# CUSTOM RECOVERY DEVICE TREE FOR INFINIX ZERO ULTRA ( X6820 )

# Device SPecifications
Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core (2x2.5 GHz Cortex-A78 & 6x2.0 GHz Cortex-A55)
Chipset | MediaTek Dimensity 930 (MT6877)
GPU     | Mali-G68 MC4
Memory  | 8 GB RAM
Shipped Android Version | 12
Storage | 256 GB (UFS)
Battery | 4500 mAh, non-removable
Display | 1080 x 2400 pixels,6.8 inches, 60/120hz

# picture
![infinixzeroultra](https://fdn2.gsmarena.com/vv/pics/infinix/infinix-zero-ultra-1.jpg)

# Checks
Blocking checks
- [✔] Correct screen/recovery size
- [✔] Working Touch, screen
- [✔] Backup to internal/microSD
- [✔] Restore from internal/microSD
- [✔] reboot to system
- [✔] ADB

Medium checks
- [✔] update.zip sideload
- [✔] UI colors (red/blue inversions)
- [✔] Screen goes off and on
- [✔] F2FS/EXT4 Support, exFAT/NTFS where supported
- [✔] all important partitions listed in mount/backup lists
- [✔] backup/restore to/from external (USB-OTG) storage
- [?] backup/restore to/from adb (https://gerrit.omnirom.org/#/c/15943/)
- [✔] decrypt /data
- [✔] Correct date

Minor checks
- [✔] MTP export
- [✔] reboot to bootloader
- [✔] reboot to recovery
- [✔] poweroff
- [✔] battery level
- [✔] temperature
- [?] encrypted backups
- [✔] encrypted backups
- [✔] input devices via USB (USB-OTG) - keyboard and mouse
- [✔] USB mass storage export
- [✔] set brightness
- [?] vibrate
- [✔] screenshot
- [✔] partition SD card
- [✔] Fastbootd

# Clone
    git clone https://github.com/Paul2202H/INFINIX-ZERO-ULTRA-X6820-DEVICE-TREE.git -b Fox-12.1 device/infinix/X6820

# Build
    export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_X6820-eng; mka bootimage
