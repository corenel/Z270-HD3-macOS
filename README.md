# Z270X-UD3-macOS
My configurations and files for macOS 10.13.6 with Z270-HD3 and i7-6700K.

## Hardware
* Intel Core i7-6700K
* Gigabyte Z270-HD3
* DDR4-2400 16G (16G x 1)
* 256 NVMe SSD (Samsung SM961) + 128GB AHCI SSD (Samsung 750 EVO) + 1TB HDD (WD-Blue)
* Gigabyte GTX1080Ti

## Installation w/ GPU
For configuration w/o GPU, please look at [this release](https://github.com/corenel/Z270-HD3-macOS/releases/tag/10.13.2).

* Install with UniBeast (8.1.0) and `CLOVER_INSTALL` ([Tutorial](http://hackintosher.com/guides/high-sierra-install-full-guide/)).
* Modify `/System/Library/Extensions/AppleGraphicsControl.kext/Contents/PlugIns/AppleGraphicsDevicePolicy.kext/Contents/Info.plist` to enable HDMI output.
* Copy `CLOVER` into `/EFI/CLOVER`.
* Install NVIDIA Web Driver ([Tutorial](http://hackintosher.com/guides/properly-install-nvidia-drivers-high-sierra-10-13/))
* Restart and Enjpy!

## Tips

- Remind to reinstall audio driver after you update system.
- Remind to rebuild kext cache after installing or uninstalling kext files.
- Once updating or restoring system, remember to enable SIP and reinstall NVIDIA Web Driver.
