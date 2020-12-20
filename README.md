# OpenCore 0.6.3 Hackintosh on Asrock B365M-ITX

Repo for my Hackintosh build using MacOS 11.0.0 (Big Sur). Will also attempt to make it a multi-boot build with Linux/Windows.

## System Specifications

| Component   | Model                                                                                                                                                         | Notes                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| CPU         | [Intel i7-9700 3GHz](https://ark.intel.com/content/www/us/en/ark/products/191792/intel-core-i7-9700-processor-12m-cache-up-to-4-70-ghz.html)                  |                                                   |
| GPU         | [ZOTAC GeForce® GTX 1070 Ti Mini](https://www.zotac.com/us/product/graphics_card/zotac-geforce-gtx-1070-ti-mini)                                              | Only compatible up to MacOS 10.13 (High Sierra)   |
| Motherboard | [Asrock B365M-ITX/ac](https://www.asrock.com/MB/Intel/B365M-ITXac/index.asp)                                                                                  |                                                   |
| RAM         | [CORSAIR Vengeance LPX 32GB (2 x 16GB) 288-Pin DDR4 2666](https://www.corsair.com/us/en/Categories/Products/Memory/VENGEANCE-LPX/p/CMK32GX4M2A2666C16)        |                                                   |
| CPU Cooler  | [Alpenföhn® Black Ridge](https://www.alpenfoehn.de/produkte/cpu-kuehler/black-ridge)                                                                          |                                                   |
| PSU         | [Corsair SF600 Gold SFX](https://www.corsair.com/us/en/Categories/Products/Power-Supply-Units/SF-Series%E2%84%A2-80-PLUS-Gold-Power-Supplies/p/CP-9020105-NA) |                                                   |
| Case        | [JONSBO T8 Handle Mini-ITX Computer Case - Silver](https://www.jonsbo.com/en/products/t8silver.html)                                                          | Needs to be partially disassembled to install GPU |
| SSD         | [SK hynix Gold S31 1TB 3D NAND 2.5 inch SATA III Internal SSD](https://ssd.skhynix.com/GoldS31.html)                                                          |                                                   |

## EFI File Tree

```
EFI
├── BOOT
│   └── BOOTx64.efi
└── OC
    ├── ACPI
    │   ├── SSDT-AWAC.aml
    │   ├── SSDT-EC-USBX.aml
    │   ├── SSDT-PLUG.aml
    │   └── SSDT-PMC.aml
    ├── Bootstrap
    │   └── Bootstrap.efi
    ├── config.plist
    ├── Drivers
    │   ├── HfsPlus.efi
    │   ├── OpenCanopy.efi
    │   └── OpenRuntime.efi
    ├── Kexts
    │   ├── AirportItlwm.kext
    │   ├── AppleALC.kext
    │   ├── IntelBluetoothFirmware.kext
    │   ├── IntelBluetoothInjector.kext
    │   ├── IntelMausi.kext
    │   ├── Lilu.kext
    │   ├── SMCProcessor.kext
    │   ├── SMCSuperIO.kext
    │   ├── USBInjectAll.kext
    │   ├── VirtualSMC.kext
    │   ├── WhateverGreen.kext
    │   └── XHCI-unsupported.kext
    ├── OpenCore.efi
    ├── Resources
    │   ├── Audio
    │   ├── Font
    │   ├── Image
    │   └── Label
    └── Tools
        ├── libaistat.dylib
        ├── OpenShell.efi
        ├── rtcread
        ├── smc
        └── smcread
```

## What's Working
* Intel WLAN support
* 
## What's Not Working
* OpenCore UEFI GUI with corresponding Big Sur assets

## Potentially Useful Tools
| Tool                                     | Use Case                                                                                                          |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Connectify](https://www.connectify.me/) | Wi-Fi to Ethernet passthrough. For when you don't have Ethernet ports in the walls but have one on your computer. |

## Getting Started
1. Follow the [OpenCore Installer Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) to create the installation media.
2. Clone this repository, and copy the `EFI` directory and its contents to your installation media.
3. Create a folder at the root of the installation media called `com.apple.recovery.boot`. Use the `macrecovery` tool specified in the [OpenCore Installer Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) to download the Big Sur base system image.
4. Copy both the `.dmg` and `.chunklist` files to the `com.apple.recovery.boot` folder created in step 3.
5. Eject the installation media from your computer and plug it into your Hackintosh build.
6. When the OpenCore UEFI shows up, select `<Your Installation Media Name> (External)`. This will launch the base system installation.
WIP
7. format disk
8. reinstall os
