# Partitioning Xiaomi Mi 9

## Files/Tools Needed 📃

- TWRP image:

Twrp image supports Android™ 11 encryption

| File Name                                       | Target Device         |
|-------------------------------------------------|-----------------------|
| [twrp-cepheus.img](https://github.com/woacepheus/Port-Windows-11-XiaoMI-9/releases/download/recoveries/twrp-cepheus.img) | Xiaomi Mi 9 |

- [Platform Tools from Google (ADB and Fastboot)](https://developer.android.com/studio/releases/platform-tools)
- A Windows PC

## Disclaimers

> [!WARNING]
> - Don't create partitions from Mass Storage Mode on Windows (because ABL will break with blank/spaces in names), your phone may be irrecoverable otherwise
> - If you see a warning and/or error during the process, it is not normal. Contact us on telegram if you see anything odd, but do not continue or proceed on your own, you will break things further.
> - Don't rerun the commands if you interrupt the process. You may break your partition table. Parted is a very *delicate* tool, anything you do may cause permanent damage to your device.
> - Do not run all commands at once. Parted is a very *delicate* tool, anything you do may cause permanent damage to your device.
> - Do not commit *any* typo with *any* commands. Parted is a very *delicate* tool, anything you do may cause permanent damage to your device.
> - Be familiar with command line interfaces. Parted is a very *delicate* tool, anything you do may cause permanent damage to your device.

> [!IMPORTANT]
> **THIS WILL WIPE ALL YOUR ANDROID™ DATA**
>
> We don't take any responsibility for any damage done to your phone. By following this guide, you agree to take full responsibility of your actions. We have done some testing,
>
> but this is **STILL IN PREVIEW** and things can go wrong.

**PLEASE READ AND BE SURE TO UNDERSTAND THE ENTIRE GUIDE BEFORE STARTING**

## What you will get 🛒

You will end up with both Android™ and Windows on your Xiaomi Mi 9. Android™ and Windows will both split the internal storage.

Android™ will boot normally, and you will have to use a PC to boot Windows when needed, unless you flash UEFI in boot partition or use M3K Helper.

# Steps 🛠️

## Acquiring all files

<details>
    <summary>Here's how to acquire the Android SDK Platform Tools: <b>Click to expand</b></summary>
    <p>


First, start by going to the [Android Platform SDK download page](https://developer.android.com/studio/releases/platform-tools) on your computer.

![SDK-1-Top](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/4c1c3762-24d8-4150-ac69-670738eb62c1)

Once on the page, scroll a little bit down til you see the link to download the platform tools for Windows.

![SDK-2-Mid](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/cd14a232-4995-480f-a061-54507e83cf41)

Click on it, an EULA will open like below:

![SDK-3-EULA](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/16d6b7df-ab56-414c-b1a5-561ec6b3ae4e)

Scroll all the way down (after reading it if that's your thing)

![SDK-4-EULA-Bottom](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/1368b2b0-74b8-4a7c-9aff-df2ca25c2f42)

Tick "I have read and agree to above terms conditions"

![SDK-5-EULA-TICK (alt)](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/02905fa2-64b8-426b-b42f-c1bb88eaa88a)

And click download

![SDK-5-EULA-TICK](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/0983f27a-76e7-4fda-ac4d-adaa56702e90)

Save the file on your computer, and extract the zip file by opening it, and selecting extract all.

![SDK-6-DL](https://github.com/WOA-Project/SurfaceDuo-Guides/assets/3755345/adc1bba0-6118-418e-9005-e2db12860893)

  </p>
</details>

## Going to the Bootloader menu

- Start by turning on your Xiaomi Mi 9 into Android™, and unlock it

- Open a command prompt on your PC

- Go to the folder where you extracted the Google Android™ Platform tools using the CD command and the path of the folder

- Run the following command to ensure your phone is detected by your PC

```batch
adb devices
```

> [!TIP]
> If you see no device listed, check for updates in Windows Update, you likely have a Driver Update pending so the phone is recognized, when you're good to go, you should see the following image below this notice.
> It is possible certain computers see no update offered (like Windows ARM64 Computers or other older machines with no functional Windows Update). If this is your case, we also provide Drivers for you to download
> at the following location, you will have to install them using Device Manager on your PC. [Download USB Drivers](https://github.com/WOA-Project/SurfaceDuo-Guides/raw/main/Files/USB-Drivers.zip)

- Run the following command now

```batch
adb reboot bootloader
```

You will be rebooted to Xiaomi Mi 9's bootloader.

## Booting to TWRP

- Plug your phone to your PC, open a command prompt and start by typing the following text, but do not press enter just yet

```batch
fastboot flash recovery
```

- Go find the TWRP image file you downloaded earlier, right click it, click "Copy as path"

- Then go back to the Command Prompt window we started writing text in previously, and simply, right click on it with your mouse (or long press if you're on a touch device) and press enter

- Now you can type the following text and press enter

```batch
fastboot reboot recovery
```

You will now boot to TWRP. Keep the phone plugged to your PC and continue along.

- Now we are issuing commands directly from inside Xiaomi Mi 9 using the PC.

## Making the partitions

### Dangerous section

> [!WARNING]
> This section if followed incorrectly could make your device unusable and require dedicated fixing steps that would be better given through assistance within our telegram channel.
>
> Please carefully follow every step, and try to not commit typos by missing numbers or characters, as those may make the device unusable.
>
> Further more, rerunning these commands after running them once ever can also damage your device, so do not refollow this section ever again.
>
> You can only refollow such instructions when you have followed our uninstall guide first.
>
> A warning or unexpected message is, well, unexpected, contact us if you see one, and do not attempt to fix anything by yourself.

- Let's now run partitioning script:

```bash
adb shell partition [Amount of storage you want Windows to have (only number)]
```

- If it asks you to run it once again, do so

- And let's exit the device shell

```bash
exit
```

### End of the Dangerous section

## Rebooting into Android

Now, reboot into Android again:

```batch
adb reboot
```

- You should now be seeing the Android™ Out of Box Experience (OOBE). Setup your phone to confirm it works correctly.

Congratulations, you successfully partitioned your device.

## The End

And we're done, please continue with the previous guide that made you land here :)

---

_**© 2020-2024 The Duo WOA Authors**_

_Snapdragon is a registered trademark of Qualcomm Incorporated. Microsoft, the Microsoft Corporate Logo, Windows, Surface, Surface Duo, Windows Hello, Continuum, Hyper-V, and DirectX are registered trademarks of Microsoft Corporation in the United States. Android is a registered trademark of Google LLC. Miracast is a registered trademark of the Wi-Fi Alliance. Other binaries may be copyright Qualcomm Incorporated, Microsoft Surface and Xiaomi Inc._

_**Limited emergency calling**_

_Running Windows on your Xiaomi Mi 9 is not a replacement for a proper phone operating system and does not have emergency calling capabilities._

_**Hello from Seattle (US), France, Italy.**_