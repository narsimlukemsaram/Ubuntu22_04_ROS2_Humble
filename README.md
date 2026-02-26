# Ubuntu22_04_ROS2_Humble
Installing ROS 2 Humble on Ubuntu 22.04 alongside Windows 11

## Install Ubuntu22.04 alongside Windows 11

**Pre-requisites**:
- A Windows 11 or higher computer
- At least 100 GB of free disk space for Ubuntu 22.04
- A USB drive with at least 8 GB
- Internet connection
- Make sure you back up your computer (especially personal files, but also your OS) in case something bad happens, which can happen since we are going to do a lot of formatting, partitioning, and changing BIOS/UEFI settings.

**Disable Secure Boot**:

On some computers, `Secure Boot` prevents you from installing or booting new operating systems. 
To disable this:
    Turn your computer off. Then turn it back on and press the BIOS entry key during boot. This key varies by hardware type but is generally F1, F2, F12, etc.
    Find the **Secure Boot** option. If possible, set it to **Disable/Off**. It is usually found in the Security, Boot Configuration, or Authentication tab.
    **Save and Exit**. Your system will reboot.

Reference:
    [How to Disable UEFI Secure Boot to Dual Boot Any System](https://www.makeuseof.com/tag/disable-secure-uefi-dual-boot/)

**Create a new partition on your Windows 11 computer for Ubuntu 22.04**: 
Do not shrink the partition from within Linux if it is your primary Windows C: drive; use Windows Disk Management instead. 
Backup your data: Always back up before partitioning.

Open Disk Management: Press Win + R, type diskmgmt.msc, and hit Enter.

Shrink Volume: Right-click your main partition (usually C:) and select Shrink Volume.
Allocate Space: Enter the amount of space to shrink in MB (e.g., for 100GB, enter 102400 and for 200GB, enter 204800).
    
**Download the Ubuntu 22.04 iso image file from https://releases.ubuntu.com/jammy/** 
Download ***Ubuntu 22.04*** from the official website, select ***64-bit PC (AMD64) desktop image***

**Install Rufus using https://rufus.ie/en/**
***Rufus*** is software that makes your USB drive bootable. Select the ***Standard*** type with your computer platform.
Most of you choose the standard one with the Windows x64 platform.

**Create a bootable Ubuntu 22.04 USB drive using Rufus.** Note: Ensure your bootable Ubuntu 22.04 USB drive is ready.
- Insert your USB into the USB port.
- In the File Explorer, right-click your USB, select the ***Format*** option, and follow the instructions.
- Right click the ***Rufus*** and run as an administrator.
- Leave everything default, click the ***SELECT*** option, and select the ISO image file just downloaded (ubuntu-22.04.5-desktop-amd64.iso).
- Click ***START*** and follow the steps.

**Boot from the USB flash drive**
Insert the bootable Ubuntu 22.04 USB drive into the laptop or PC where you want to install Ubuntu.

Restart the computer.

Your device should recognize the installation media and launch the Ubuntu installer.

If Ubuntu doesn’t launch, restart your computer. This time, hold a key during startup:
On a PC or Windows computer, F12 is the most common key for bringing up the system boot menu, but Escape, F2, and F10 are common alternatives. If unsure, look for a brief message when your system starts. It often tells you which key to press to access the boot menu. You can also find the right key in the documentation for your laptop or PC.

In the boot menu that appears, select your USB device.

**Step 6: Follow the installer**

The Ubuntu Desktop installer opens.

## Install ROS 2 Humble on Ubuntu 22.04
