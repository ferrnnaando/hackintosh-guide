# Hackintosh Setup Guide

## 1. Check Hardware Compatibility
- Verify if your PC hardware is compatible with macOS. Ensure compatibility for:
  - **CPU (Central Processing Unit):** Check CPU compatibility for macOS. Refer to the Dortania guide for CPU-specific instructions.
  - **GPU (Graphics Processing Unit):** Identify your GPU model and ensure it's compatible with macOS. AMD GPUs are generally more compatible.
  - **Wi-Fi Chipset:** Check Wi-Fi chipset model. Replace with a macOS-compatible chipset if necessary.
  - **Ethernet:** Verify compatibility. Most built-in Ethernet adapters work.
  - **Audio:** Check your motherboard's audio chipset. Some may require additional kexts.
  - **Motherboard:** Verify motherboard compatibility. Refer to Dortania or Hackintosh forums for recommendations.
  - **RAM and Storage:** Ensure sufficient RAM and storage space.
  - **Bluetooth:** Confirm Bluetooth chipset compatibility.
  - **Other Components:** Check compatibility for webcams, card readers, and peripherals.

## 2. Gather Necessary Files
- Download OpenCore bootloader from the [Dortania website](https://dortania.github.io/OpenCore-Install-Guide/).
- Choose x32 or x64 based on your PC's architecture:
  - **x32 (32-bit):** For 32-bit UEFI firmware (less common).
  - **x64 (64-bit):** For 64-bit UEFI firmware (modern PCs).
- Follow Dortania's installation instructions.

## 3. Configure OpenCore
- Follow Dortania's guide for configuring OpenCore based on your hardware.

## 4. BIOS/UEFI Settings
- Access BIOS/UEFI settings and configure as specified in Dortania's guide.
- Disable secure boot, enable AHCI mode, and adjust other relevant options.

## 5. Create EFI Partition
- Create an EFI partition on your USB drive and place OpenCore files in it.

## 6. Addressing "Error 1004" (if encountered)
- If you face "Error 1004" during macOS installation:
  - Unplug non-essential devices (monitors, audio adapters, peripherals).
  - Boot PC, enter BIOS/UEFI with the keyboard plugged in.
  - Boot macOS installer USB.
  - Unplug the keyboard once macOS installer boots.
  - Plug in only the mouse during installation.

## 7. Boot from USB
- Insert your USB installer and select it as the boot device from the boot menu (F12, F8, etc.).

## 8. Install macOS
- Boot into the macOS installer from USB.
- Format the target drive using Disk Utility as GUID Partition Map with Mac OS Extended (Journaled) or APFS.
- Install macOS on the formatted drive.

## 9. Post-installation Setup
- Boot macOS from USB, then install OpenCore on the internal drive.
- Configure necessary kexts and settings for hardware compatibility.

## 10. Troubleshooting
- Be aware that installing macOS through Hackintosh can be a challenging process and may initially result in an experience that doesn't resemble macOS. You may encounter:
  - Aesthetic issues with graphics and user interface elements.
  - Problems with hardware functionality like Wi-Fi, audio, or Bluetooth.
  - System stability issues.
  - Frequent updates and maintenance to keep your Hackintosh functioning.

  It's essential to be patient and persistent when troubleshooting and be prepared for potential limitations in your Hackintosh setup.
