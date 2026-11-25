# Root-Notes-OnePlus-15R
Personal notes &lt;3


OTA download (boot.img - init_boot.img)- https://roms.danielspringer.at/




Bootloader already unlocked?

- .\adb shell getprop ro.build.version.ota
- .\adb shell getprop ro.boot.slot_suffix

- https://github.com/KernelSU-Next/KernelSU-Next
- grab spoofed apk

- .\adb install <apk-name>.apk
- .\adb push init_boot.img /sdcard/Download/

- Patch it on the phone

- .\adb pull /sdcard/Download/kernelsu_next_patched_<date>.img .
- .\adb reboot bootloader
- .\fastboot getvar current-slot
- .\fastboot flash init_boot_a kernelsu_next_patched_<date>.img
- .\fastboot reboot


modules:
- HMA-OSS + Zygisk next + AlwaysStrong
