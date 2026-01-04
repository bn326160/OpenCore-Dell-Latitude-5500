# OpenCore Dell Latitude 5500

OpenCore EFI configuration for Dell Latitude 5500 running macOS Sequoia 15.7.3. This repository contains config, ACPI patches, and required kexts for a fully functional hackintosh setup.

## Computer Specifications

| Component | Model |
|-----------|-------|
| **Laptop** | Dell Latitude 5500 |
| **CPU** | Intel Core i5-8365U @ 1.6GHz (Whiskey Lake) |
| **GPU** | Intel UHD Graphics 620 |
| **RAM** | 8 GB DDR4 |
| **Storage** | 256 GB NVMe SSD |
| **Audio** | Realtek ALC236 (VEN_10EC&DEV_0236) |
| **Wireless** | Intel Wireless-AC 9560 160MHz |
| **Ethernet** | Intel I219-LM |
| **Touchpad** | I2C |
| **Display** | 15.6" FHD (1920x1080) |

## Status

### ✅ Working
- macOS Sequoia 15.7.3 installation
- Keyboard, trackpad and touchpoint
- Display w/ acceleration
- Audio (mic & built-in speakers)
- USB ports
- Sleep & wake-up
- Webcam
- Ethernet
- Intel Wifi
- Intel Bluetooth
- Power management (presumably)
- Battery indicator (Unsure about accuracy yet)

### ⚠️ Not Working
- HDMI output

### ❓ Untested
- Displayport over USB-C
- Accuracy of battery indicator
- Brightness control

## BIOS Settings

Reset to defaults, then apply these settings:

| Setting | Value |
|---------|-------|
| **Secure Boot** | Disabled |
| **VT-d (VT for Direct I/O)** | Disabled |
| **Virtualization** | Enabled |
| **UEFI Boot** | Enabled |
| **Fast Boot** | Disabled |

*To complete*

Access BIOS by pressing `F2` or `Del` during boot.

## Versions

### OpenCore & Tools
| Component | Version |
|-----------|---------|
| [OpenCore](https://github.com/acidanthera/OpenCorePkg) | 1.0.6 |


### Kexts
| Kext | Version | Purpose |
|------|---------|---------|
| [Lilu](https://github.com/acidanthera/Lilu) | 1.7.1 | Kernel extension patching framework |
| [VirtualSMC](https://github.com/acidanthera/VirtualSMC) | 1.3.7 | System Management Controller |
| SMCProcessor | - | CPU temperature monitoring (part of VirtualSMC) |
| SMCBatteryManager | - | Battery status (part of VirtualSMC) |
| SMCDellSensors | - | Dell sensor support (part of VirtualSMC) |
| [WhateverGreen](https://github.com/acidanthera/WhateverGreen) | 1.7.0 | GPU acceleration (Intel iGPU) |
| [AppleALC](https://github.com/acidanthera/AppleALC) | 1.9.6 | Audio codec support |
| [VoodooPS2](https://github.com/acidanthera/VoodooPS2) | 2.3.7 | Keyboard and trackpad |
| [VoodooI2C](https://github.com/VoodooI2C/VoodooI2C/releases) | 2.9.1 | I2C touchpad controller |
| VoodooI2CHID | - | I2C HID device support (part of VoodooI2C) |
| [AlpsHID](https://github.com/blankmac/AlpsHID/releases) | 1.2 | Alps touchpad HID support |
| [IntelMausi](https://github.com/acidanthera/IntelMausi) | 1.0.8 | Intel Ethernet (I219-LM) |
| [ITLWM](https://openintelwireless.github.io/itlwm/Installation.html#itlwm) | 2.3.0 | Intel WiFi |
| [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | 2.4.0 | Intel Bluetooth firmware |
| [NVMeFix](https://github.com/acidanthera/NVMeFix) | 1.1.3 | NVMe power management |
| [USBToolBox](https://github.com/USBToolBox/kext) | 1.2.0 | USB port mapping tool |


## Resources

- [OpenCore Project](https://github.com/acidanthera/OpenCorePkg)
- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## Disclaimer

This configuration is provided as-is for educational purposes. Proceed at your own risk.
