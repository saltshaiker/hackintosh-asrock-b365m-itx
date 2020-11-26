# OpenCore 0.6.3 Hackintosh on Asrock B365M-ITX

Repo for my Hackintosh build.

## System Specifications

CPU: Intel i7-9700 3GHz

GPU: ZOTAC GeForce® GTX 1070 Ti Mini

Motherboard: Asrock B365M-ITX/ac

RAM: CORSAIR Vengeance LPX 32GB (2 x 16GB) 288-Pin DDR4 2666

CPU Cooler: Alpenföhn® Black Ridge

PSU: Corsair SF600 Gold SFX

Case: JONSBO T8 Handle Mini-ITX Computer Case - Silver

SSD: SK hynix Gold S31 1TB 3D NAND 2.5 inch SATA III Internal SSD

## EFI File Tree

```
EFI/
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
    │   └── OpenRuntime.efi
    ├── Kexts
    │   ├── AirportBrcmFixup.kext
    │   ├── AppleALC.kext
    │   ├── BrcmBluetoothInjector.kext
    │   ├── BrcmFirmwareData.kext
    │   ├── BrcmPatchRAM2.kext
    │   ├── IntelMausi.kext
    │   ├── Lilu.kext
    │   ├── SMCProcessor.kext
    │   ├── SMCSuperIO.kext
    │   ├── USBInjectAll.kext
    │   ├── VirtualSMC.kext
    │   ├── WhateverGreen.kext
    │   └── XHCI-unsupported.kext
    ├── OpenCore.efi
    └── Tools
        ├── libaistat.dylib
        ├── OpenShell.efi
        ├── rtcread
        ├── smc
        └── smcread
```
