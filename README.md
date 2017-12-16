# Z270X-UD3-macOS
My configurations and files for macOS 10.13.2 with Z270-HD3 and i7-6700K.

## Handware
* Intel Core i7-6700K
* Gigabyte Z270-HD3
* DDR4-2400 16G (16G x 1)
* 256 NVMe SSD (Samsung SM961) + 128GB AHCI SSD (Samsung 750 EVO) + 1TB HDD (WD-Blue)

## Installation
* Install with UniBeast (8.1.0) and MultiBeast (10.1.1).
  * Quick Start - UEFI Boot Mode
  * Drivers - Audio - Realtek - ALC887/888b && 100/200 Series Audio
  * Drivers - Misc - FakeSMC && Plugins && HWMonitor && NullCPUPowerManagement
  * Drivers - Network - Intel - IntelMausithernet v2.3.0
  * Drivers - USB - Increase Mac Port Limit 200 Series
  * Bootloaders - Clover UEFI Boot Mode
  * Customize - Graphics - Intel HD 5xx && Intel Graphics Fixup
  * Customize - System Definitions - iMac17,1
* Open `Clover Configurater` to customize SMBIOS for `iMac17,1`
* Modify `/System/Library/Extensions/AppleGraphicsControl.kext/Contents/PlugIns/AppleGraphicsDevicePolicy.kext/Contents/Info.plist` to enable HDMI output.
* Copy `config.plist` and other things in `CLOVER` into `/EFI/CLOVER`.
* **<u>!IMPORTANT</u>**: MultiBeast (10.1.1) use 1.2.0 version of `Lilu.kext` but it'll cause boot loop in macOS High Sierra 10.13.2. You need replace it with a newer version (1.2.1 or higher) before restarting system.

## Tips

- Remind to reinstall audio driver after you update system.
- Remind to rebuild kext cache after installing or uninstalling kext files.
