# Hackintosh Setup Guide for Intel-based Systems

**Disclaimer:** This guide is based on settings tested for Intel-based motherboards. Individual motherboard models may have slight variations in their BIOS options. Consult your motherboard's manual for specific instructions.

## 🖥️ 1. Check Hardware Compatibility
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

## 📦 2. Prepare Installation Media
- Download OpenCore bootloader from the [Dortania website](https://dortania.github.io/OpenCore-Install-Guide/).
- For USB drives with large partitions (+16GB), use Rufus or your system's partition eraser tool to create a macOS installer USB.

## 📂 3. Create EFI Partition
- Create an EFI partition on your USB drive.
- Place the necessary OpenCore files in the EFI partition.

## ⚙️ 4. BIOS/UEFI Settings
- Access your motherboard's BIOS/UEFI settings during system startup. This is typically done by pressing a specific key (e.g., F2, Del, or F12) when your computer boots. Refer to your motherboard's manual for the exact key and method.
- In the BIOS/UEFI settings, make the following adjustments:

  - **❌ Disable Secure Boot:** Secure Boot restricts the loading of unsigned operating systems and drivers. Disable it to allow macOS to boot properly.

  - **❌ Disable Fast Boot:** This feature speeds up the boot process by skipping certain checks, but it can interfere with macOS installation. Disable it to ensure macOS compatibility.

  - **❌ Disable Compatibility Support Module (CSM):** CSM provides backward compatibility for older operating systems like Windows 7. However, macOS is designed to work in UEFI mode, so it's essential to disable CSM to prevent compatibility issues. GPU errors and stalls like `gIO` are common when this option is enabled.

  - **❌ Disable Serial/COM Port:** This is often not needed for Hackintosh and can cause conflicts. Disable it.

  - **❌ Disable Parallel Port:** Parallel ports are rarely used in modern computing and can cause issues with macOS. Disable this feature.

  - **❌ Disable VT-d (Virtualization Technology for Directed I/O):** VT-d can conflict with macOS. It should be disabled unless you set `DisableIoMapper` to `YES` in your OpenCore configuration.

  - **❌ Disable Thunderbolt:** Disable Thunderbolt during the initial macOS installation, as Thunderbolt can cause issues if not set up correctly. You can enable it later if needed.

  - **❌ Disable Intel SGX:** This feature is not typically needed for Hackintosh and can be disabled.

  - **❌ Disable Intel Platform Trust:** Platform Trust technology can interfere with macOS. Disable it.

  - **❌ Disable CFG Lock (MSR 0xE2 write protection):** This must be off for your Hackintosh to boot. If you can't find the option, enable `AppleCpuPmCfgLock` under `Kernel -> Quirks` in your OpenCore configuration.

- Save your BIOS/UEFI settings and exit. Your computer will restart.

## 🛠️ 5. Configure OpenCore
- Customize the OpenCore configuration for your PC. Follow the Dortania guide to:
  - Add necessary kexts (drivers) to the Kexts folder.
  - Place ACPI files, if needed, in the ACPI folder.
  - Add specific files or patches to the Resources and Tools folders.
  - Edit the config.plist file according to your PC's requirements. Dortania provides explanations for each section.

## 💿 6. Boot from USB
- Insert your USB installer into your Hackintosh system.
- Access the boot menu (usually by pressing a key like F12 or F8 during startup).
- Select the USB drive as the boot device.

## ⚙️ 7. Install macOS
- Boot into the macOS installer from USB.
- Use Disk Utility to erase a partition where macOS will be installed. Format it as Mac OS Extended (HFS+).
- Proceed with the macOS installation on the formatted partition.

## 🚧 8. Addressing "Error 1004" (if encountered)
- If you encounter "Error 1004" during macOS installation, follow these steps:
  - Unplug non-essential devices (monitors, audio adapters, peripherals).
  - Boot your PC, enter BIOS/UEFI with the keyboard plugged in.
  - Boot the macOS installer USB.
  - Once the macOS installer boots successfully, unplug the keyboard again.
  - Plug in only the mouse during installation.

## 🌐 9. Post-installation Setup
- After macOS is installed, boot into it using your USB drive, and install OpenCore on the internal drive.
- Configure necessary kexts (drivers) and other settings to make your hardware work correctly.

## 🚀 10. Troubleshooting
- Be aware that installing macOS through Hackintosh can be a challenging process and may initially result in an experience that doesn't resemble macOS. You

