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
| VirtualSMC | 1.3.2 | System Management Controller |
| SMCProcessor | 1.3.2 | CPU temperature monitoring |
| SMCBatteryManager | 1.3.2 | Battery status |
| Lilu | 1.6.8 | Kernel extension patching framework |
| WhateverGreen | 1.6.6 | GPU acceleration (Intel iGPU) |
| AppleALC | 1.8.9 | Audio codec support |
| AtherosE2200Ethernet | 2.2.2 | Ethernet driver (if applicable) |
| VoodooPS2Controller | 2.3.8 | Keyboard and trackpad |
| CPUFriend | 1.2.7 | CPU power management |
| CPUFriendDataProvider | 1.0.0 | CPU power management data |
| IOPCI | 1.0.0 | PCI bridge support |
| USBInjectAll | 0.7.1 | USB port mapping (during setup) |
| NVMeFix | 1.2.1 | NVMe power management |

*To update versions to match my current setup.*

## Resources

- [OpenCore Project](https://github.com/acidanthera/OpenCorePkg)
- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)

## Disclaimer

This configuration is provided as-is for educational purposes. Proceed at your own risk.
