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
- Check Online Resources: Research your hardware on Hackintosh forums, websites, or community databases to see if others have successfully set up Hackintosh systems with similar components. Dortania's guide may also provide information on specific hardware considerations.

## 2. Prepare Installation Media
- Download OpenCore bootloader from the [Dortania website](https://dortania.github.io/OpenCore-Install-Guide/).
- For USB drives with large partitions (+16GB), use Rufus or your system's partition eraser tool to create a macOS installer USB.

## 3. Create EFI Partition
- Create an EFI partition on your USB drive.
- Place the necessary OpenCore files in the EFI partition.

## 4. Configure OpenCore
- Customize the OpenCore configuration for your PC. Follow the Dortania guide to:
  - Add necessary kexts (drivers) to the Kexts folder.
  - Place ACPI files, if needed, in the ACPI folder.
  - Add specific files or patches to the Resources and Tools folders.
  - Edit the config.plist file according to your PC's requirements. Dortania provides explanations for each section.

## 5. BIOS/UEFI Settings
- Access your motherboard's BIOS/UEFI settings.
- Configure settings as specified in Dortania's guide, including:
  - Disabling secure boot.
  - Enabling AHCI mode for SATA devices.
  - Adjusting other relevant options.

## 6. Boot from USB
- Insert your USB installer into your Hackintosh system.
- Access the boot menu (usually by pressing a key like F12 or F8 during startup).
- Select the USB drive as the boot device.

## 7. Install macOS
- Boot into the macOS installer from USB.
- Use Disk Utility to erase a partition where macOS will be installed. Format it as Mac OS Extended (HFS+).
- Install macOS on the formatted partition.

## 8. Addressing "Error 1004" (if encountered)
- If you encounter "Error 1004" during macOS installation, follow these steps:
  - Unplug non-essential devices (monitors, audio adapters, peripherals).
  - Boot your PC, enter BIOS/UEFI with the keyboard plugged in.
  - Boot the macOS installer USB.
  - Once the macOS installer boots successfully, unplug the keyboard again.
  - Plug in only the mouse during installation.

## 9. Post-installation Setup
- After macOS is installed, boot into it using your USB drive, and install OpenCore on the internal drive.
- Configure necessary kexts (drivers) and other settings to make your hardware work correctly.

## 10. Troubleshooting
- Be aware that installing macOS through Hackintosh can be a challenging process and may initially result in an experience that doesn't resemble macOS. You may encounter:
  - Aesthetic issues with graphics and user interface elements.
  - Problems with hardware functionality like Wi-Fi, audio, or Bluetooth.
  - System stability issues.
  - Frequent updates and maintenance to keep your Hackintosh functioning.

  It's essential to be patient and persistent when troubleshooting and be prepared for potential limitations in your Hackintosh setup.

**Note:** Hackintoshing may not work perfectly, and it may require ongoing maintenance. Ensure you respect Apple's terms and the legality of creating a Hackintosh in your jurisdiction.
