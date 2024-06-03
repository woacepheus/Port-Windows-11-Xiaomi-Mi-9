<img align="right" src="https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/blob/main/cepheus.png" width="425">


# Running Windows on the Xiaomi Mi 9

## Updating Drivers

### Prerequisites
- Windows on your Xiaomi Mi 9
- [Drivers](https://github.com/qaz6750/XiaoMi9-Drivers/releases)
- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Boot the modded recovery
> If Xiaomi has replaced your recovery back to stock, flash it again in fastboot with:
```cmd
fastboot flash recovery path\to\recovery-cepheus.img reboot recovery
```

#### Enter mass storage mode
> Run it twice if it tells you to
```cmd
adb shell msc
```

#### Start the Windows disk manager
> Once the Mi 9 is detected as a disk
```cmd
diskpart
```

### Assign `X` to Windows volume

#### Select the Windows volume of the phone
> Use `list volume` to find it, it's the one named "WINCEPHEUS"
```diskpart
select volume <number>
```

#### Assign the letter X
```diskpart
assign letter x
```

#### Exit diskpart
```diskpart
exit
```

### Installing drivers
> Extract the drivers archive and open the 'OfflineUpdater.cmd' file. Type the drive letter of WINCEPHEUS (should be X) and hit enter.

### Reboot to Windows
> Restore your "Windows" boot.img backup in TWRP and reboot your phone.

## Finished!
