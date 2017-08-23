# Z270X-UD3-macOS
My configurations and files for macOS 10.12.5 with Z270-HD3 and i7-6700K.

## Handwara
* Intel Core i7-6700K
* Gigabyte Z270-HD3
* DDR4-2400 16G (8G x 2)
* 128GB AHCI SSD (Samsung 750 EVO) + 1TB HDD (WD-Blue)

## Installation
* Install with UniBeast and MultiBeast.
  * Quick Start - UEFI
  * Drivers - Audio - Realtek - ALC887 && 100/200 Series Audio
  * Drivers - Misc - FakeSMC && Plugins && HWMonitor && NullCPUPowerManagement
  * Drivers - Network - Intel - IntelMausithernet v2.2.1d1
  * Drivers - USB - Increase Mac Port Limit 200 Series
  * Bootloaders - Clover UEFI Boot Mode
  * Customize - Graphics - Intel HD 5xx
  * Customize - System Definitions - iMac17,1
* Open `Clover Configurater` to customize SMBIOS for `iMac17,1`
* Install `Lilu.kext` and `IntelGraphicsFixup.kext` in `/L/E` to fix Intel Grapgics Driver since macOS 10.12.5
* Modify `/System/Library/Extensions/AppleGraphicsControl.kext/Contents/PlugIns/AppleGraphicsDevicePolicy.kext/Contents/Info.plist` to enable HDMI output.
* Copy `config.plist` and other things in `CLOVER` into `/EFI/CLOVER`.
