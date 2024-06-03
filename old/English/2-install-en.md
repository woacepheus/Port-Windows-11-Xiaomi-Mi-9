<img align="right" src="https://raw.githubusercontent.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/main/cepheus.png" width="425" alt="Windows 11 Running On A Xiaomi Mi 9">

# Running Windows on the Xiaomi Mi 9

## Installing Windows

### Prerequisites
- [Windows on ARM image](https://worproject.com/esd)

- [Drivers](https://github.com/qaz6750/XiaoMi9-Drivers/releases)

- [Modded TWRP](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.4/recovery-cepheus.img) (Should already be installed)

### Boot the modded recovery
> If rebooting on the last page has replaced your recovery back to stock, flash it again in fastboot with:
```cmd
fastboot flash recovery path\to\recovery-cepheus.img reboot recovery
```

#### Execute the msc script
> If it asks you to run it once again, do so
```cmd
adb shell msc
```
  
#### Start the Windows disk manager
> [!WARNING]
> DO NOT ERASE, CREATE OR OTHERWISE MODIFY ANY PARTITION WHILE IN DISKPART!!!! THIS WILL ERASE ALL OF YOUR UFS OR PREVENT YOU FROM BOOTING TO FASTBOOT!!!! THIS MEANS THAT YOUR DEVICE WILL BE PERMANENTLY BRICKED WITH NO SOLUTION! (except for taking the device to Xiaomi or flashing it with EDL, both of which will likely cost money)
```cmd
diskpart
```

#### Select the Windows volume of the phone
> Use `list volume` to find it, it's the one named **WINCEPHEUS**
```diskpart
select volume <number>
```

#### Assign the letter X
```diskpart
assign letter x
```

#### Select the esp volume of the phone
> Use `list volume` to find it, it's the one named **ESPCEPHEUS**
```diskpart
select volume <number>
```

#### Assign the letter Y
```diskpart
assign letter y
```

#### Exit diskpart
```diskpart
exit
```

### Installing Windows
> Replace `path\to\install.esd` with the actual path to install.esd.

> If you are using an ISO file, the image file is located in the sources folder inside the ISO. Mount the ISO with Windows Explorer and then copy the path to it.

> Replace `index:6` with `index:1` if your image is not from the link in this guide.

```cmd
dism /apply-image /ImageFile:path\to\install.esd /index:6 /ApplyDir:X:\
```

### Installing drivers
> Extract the drivers archive and open the 'OfflineUpdater.cmd' file. Type the drive letter of **WINCEPHEUS** (should be X) and hit enter.

#### Create Windows bootloader files for the EFI
```cmd
bcdboot X:\Windows /s Y: /f UEFI
```

#### Remove disk letter
> Use diskpart to remove the letter from **ESPCEPHEUS**, or it will remain until you reboot your PC

> Use `list volume` to find ESPCEPHEUS, select it with `select volume <number>`, then remove letter Y with `remove letter y`

### Reboot to Android
> To set up dualboot

### [Last step: Setup Dualboot](dualboot-en.md)



















