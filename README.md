# twrp device tree for Tecno Pova 5 pro ( LH8n )

Tecno Pova 5 Pro ( _LH8n_ ) is a mid-range smartphone from Tecno

Released on 2023, August 01

# Device SPecifications
Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core (2x2.4 GHz Cortex-A76 & 6x2.0 GHz Cortex-A55)
Chipset | MediaTek Dimensity 6080 (MT6833)
GPU     | Mali-G57 MC2
Memory  | 4/8 GB RAM
Shipped Android Version | 13 (HIOS 13.5) ~ upgradable to hios 14 ~
Storage | 128/256 GB (UFS)
Battery | 5000 mAh, non-removable
Display | 1080 x 2460 pixels,6.78 inches, 60/90/120hz

# picture
![infinixzeroultra](https://www.google.com/search?client=ms-android-transsion&sca_esv=5539dfb16aea6726&sxsrf=AE3TifMH_iJi4w54Zh6T6PeZN4FrhwtNNQ:1759839030273&udm=2&fbs=AIIjpHz30rPMyW-0vSP0k1VTNmO_kCOARpjPjQRkBWH2HwUIz5XUSIJvSK0oms7XOxizDlmaluFRoyHhfze9DJaNLZEHuS0Lu5MiuUYTh4n371n02sv90SHbfC_miBtM9h92L_3_Yp2Rv8lqaGVyK1gr5OVnbzUln9SNp-uYHneU0p_Ps8wtXRmcDyJs0xSJNKsl1Z5cA8612ElpDaT3ffZCkr8HgNdQoB-TwYCS3Yhw0zUT_yW-7ac&q=infinix+zero+ultra&sa=X&sqi=2&ved=2ahUKEwjjsIuih5KQAxWVb_UHHdHmGdUQtKgLegQIEhAB&biw=360&bih=692&dpr=3#sv=CAMSuQQajAQK5gEKuQEStgEKd0FMa3RfdkVJc2FfUWZIUkJiWjVsWXBHckM0a1BSNVY4akpWM0l3Q0l1TUp1Y2NDZ00xamFoMW1lMTRMRzRpN0lxRDZwcGZXWTA1cW1rSjBQdmc4SVhiXzB4SWJ3anBzamdycm4tMmY0enpYWk9VZnE0UjFDQnNvEhdVUVBsYUpmc0FzM3QxZThQX08tWWlBURoiQUZNQUdHb1NfUE9zWnNpZTg0WnkxRzljLVQ5cURBUDQyZxIDODQ5GgEzIhcKAXESEmluZmluaXggemVybyB1bHRyYSIHCgN0YnMSABKOAgrPARLMAQqMAUFMa3RfdkV4d1cyQlFKSG95YXhJd2NhaUdnMVhtbHpiVHNSXzJvUFB1ekFPMGhmTklPMDRZWXJRdnAxaHNEUlF1dU1NUzk4YmNvLXpMdm5ySlVzTnpXZ0tSQkRULTh0eFNYNzVvWmRtazZSMmplWkpCNTRNaUc1bDBhalhJWGEtYnZaUXBSbGZnWmZwEhdVUVBsYUpmc0FzM3QxZThQX08tWWlBURoiQUZNQUdHb3p4X0VqMVF2bVRaOEdBM1hfeXVYdG1wQV9jQRIENDY5OBoBMyIYCgZpbWdkaWkSDkZudzB2SEVva3NIQUtNIhcKBWRvY2lkEg5oRUdhSDlnRGVTcS1kTSoQZS1GbncwdkhFb2tzSEFLTSAEKiQKDlBhQWVscUJyUmwzRUFNEhBlLUZudzB2SEVva3NIQUtNGAAwARgHIKi65acGMAFKCggCEAIYAiACKAI)

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
- [✔] vibrate
- [✔] screenshot
- [✔] partition SD card
- [✔] Fastbootd

# Clone
    git clone https://github.com/naden01/tecno_LH8n.git -b android-12.1 device/tecno/LH8n

# Build
    export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch twrp_LH8n-eng; mka vendorbootimage
