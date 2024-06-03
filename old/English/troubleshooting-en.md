<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Running Windows on the Xiaomi Mi 9

## Troubleshooting Issues

## Charging in Windows does not work
> [!WARNING]
> Do not use a powered USB hub with host mode enabled, this can potentially break your device. If you use a powered USB hub, please use the [disable USB host mode guide](post-install-en.md#disabling-usb-host-mode).

> Charging in Windows only works on specific cables, regardless of whether USB host mode is on or off.

Cables that have been known to work are the original Poco X3 Pro cable (identified by the additional orange/red pin in the USB-A port), and the Nimaso 100W USB-C to USB-C fast charging cable.

## TWRP does not start and the phone does not exit from fastboot

Take the bootloaders from the [firmware](https://xiaomifirmwareupdater.com/archive/firmware/cepheus/) and flash them via fastboot, then try to launch again
