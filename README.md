# tiny11-arch-dualboot
A comprehensive guide to dual-booting Tiny11 and Arch Linux (Hyprland + Wayland) on a system with AMD CPU and GPU. Includes step-by-step instructions, troubleshooting tips, and performance optimization strategies. Perfect for users seeking a lightweight and efficient dual-boot setup.

1. Download Windows 11 ISO from Microsoft's website: `https://www.microsoft.com/en-us/software-download/windows11`.
2. Download latest Tiny 11 release from ntdevlabs reposetory: `https://github.com/ntdevlabs/tiny11builder/releases`.
3. Download latest Rufus release from: `https://rufus.ie/en/`.
4. Mount Windows 11 ISO using File Explorer (note the drive letter).
5. Launch WindowsPowerShell as administrator.

### In PowerShell 
1. Set execution policy in PowerShell as unrestricted: `Set-ExecutionPolicy unrestricted`.
2. Press `A` (Yes to All).
3. Launch tiny11maker.ps1: `& C:\path\to\tiny11maker.ps1`.
4. Enter drive letter for mounted ISO, eg `D`.
5. Select ImageIndex, recommended: `6`, for Windows 11 Pro (N versions have proven to not be suitable, for me).
6. Wait for script to finish.

### In Rufus
#### Drive Properties
1. Choose your boot device, (8 GB minimum).
2. Select `tiny11.iso` boot image.
3. Select `GPT` partition scheme.

#### Format Options

4. name the volume `TINY11_BOOT`.
5. Select NTFS file system.
6. Select `4096 bytes (Default)` cluster size.
7. START.
