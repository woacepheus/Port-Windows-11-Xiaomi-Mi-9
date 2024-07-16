# Enabling Dual Boot

Table of Contents:

* [Enabling Dual Boot](#enabling-dual-boot)
   * [Files/Tools Needed 📃](#filestools-needed-)
   * [Steps 🛠️](#steps-️)
      * [Installing M3K Helper](#installing-m3k-helper)
      * [Installing StA](#installing-sta)
      * [How it Works](#how-it-works)

## Files/Tools Needed 📃

- You will need the following files from the [BSP Release page](https://github.com/qaz6750/XiaoMi9-Drivers/releases/latest):

UEFI Image:

| File Name                              | Target Device         |
|----------------------------------------|-----------------------|
| MuCepheusSecureBoot.img                | Xiaomi Mi 9           |

StA Installer:
| File Name                              | Target Device         |
|----------------------------------------|-----------------------|
| [StA_Installer_vayu.exe](https://github.com/woa-vayu/POCOX3Pro-Guides/raw/main/Files/StA_Installer_vayu.exe)                | POCO X3 Pro/Xiaomi Mi 9               |

M3K Helper:

| File Name                              | Target Device         |
|----------------------------------------|-----------------------|
| [M3K-HelperX.X.apk	](https://github.com/woa-vayu/WoA-Helper-M3K/releases/latest)                | POCO X3 Pro / Xiaomi Mi 9               |

- Stock device boot.img image obtained from an ota package, or from the device itself using **M3K Helper**.
- Rooted POCO X3 Pro with Windows already installed

# Steps 🛠️

## Installing M3K Helper

- Download and install the M3K Helper, then open it and grant it root access.
- Download the UEFI image and place it inside the folder named ```UEFI``` in your internal storage.
- Press the ```Mount Windows``` button, then download and move StA_Installer_vayu.exe to the newly created ```Windows``` folder in your internal storage.
- Return to the M3K Helper and press ```QuickBoot to Windows```.

Your device will now boot into Windows

## Installing StA

- Once in Windows, navigate to ```C:\StA_Installer_vayu.exe``` and run it.

## How it Works

- To boot Android™, run ```Switch to Android``` shortcut on your desktop or start menu
- To boot Windows, press ```QuickBoot to Windows``` inside the M3K Helper

---

_**© 2020-2024 The Duo WOA Authors**_

_Snapdragon is a registered trademark of Qualcomm Incorporated. Microsoft, the Microsoft Corporate Logo, Windows, Surface, Surface Duo, Windows Hello, Continuum, Hyper-V, and DirectX are registered trademarks of Microsoft Corporation in the United States. Android is a registered trademark of Google LLC. Miracast is a registered trademark of the Wi-Fi Alliance. Other binaries may be copyright Qualcomm Incorporated, Microsoft Surface and Xiaomi Inc._

_**Limited emergency calling**_

_Running Windows on your POCO X3 Pro is not a replacement for a proper phone operating system and does not have emergency calling capabilities._

_**Hello from Seattle (US), France, Italy.**_