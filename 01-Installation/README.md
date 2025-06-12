# 💿 Windows 11 Clean Installation Guide

## Overview

This guide will help you perform a clean Windows 11 installation without bloatware using a custom `autounattend.xml` configuration file.

## 🎯 What This Does

- **Skips Microsoft Account requirement** - Install with local account
- **Removes bloatware** - No unwanted pre-installed apps
- **Automates setup** - Minimal user interaction during installation
- **Custom configuration** - Pre-configured regional and privacy settings
- **Clean experience** - Professional, minimal Windows installation

## 📋 Prerequisites

### Required Tools

1. **Windows 11 ISO** - Download from [Microsoft's official website](https://www.microsoft.com/software-download/windows11)
2. **Rufus** - [Download here](https://rufus.ie/en/) for creating bootable USB
3. **USB Drive** - At least 8GB capacity
4. **autounattend.xml** - Our custom configuration file

### Hardware Requirements

- TPM 2.0 chip
- UEFI firmware
- Secure Boot capable
- 4GB RAM minimum (8GB recommended)
- 64GB storage minimum

## 🔧 Setup Instructions

### Step 1: Prepare the autounattend.xml

1. Download the `autounattend.xml` file from this repository
2. **Important:** Edit the computer name to your preference:
   ```xml
   <ComputerName>SamCux-PC</ComputerName>
   ```
   Change `SamCux-PC` to your desired computer name

### Step 2: Create Bootable USB with Rufus

1. **Insert your USB drive** and open Rufus
2. **Select your USB device** from the dropdown
3. **Click "SELECT"** and choose your Windows 11 ISO file
4. **Partition scheme:** GPT
5. **Target system:** UEFI (non CSM)
6. **File system:** FAT32
7. **Click "START"** to create the bootable USB

### Step 3: Add autounattend.xml to USB

1. After Rufus completes, **don't eject the USB yet**
2. **Copy the `autounattend.xml` file** to the root directory of the USB drive
3. The file should be directly in the USB root (not in any folder)

### Step 4: Boot and Install

1. **Insert the USB** into your target computer
2. **Boot from USB** (usually F12, F2, or Delete during startup)
3. **Follow the installation** - most steps will be automated
4. **Wait for completion** - the system will restart several times

## ⚙️ Customization Options

### User Account Configuration

```xml
<LocalAccounts>
    <LocalAccount wcm:action="add">
        <Password>
            <Value></Value> <!-- Leave empty for no password -->
            <PlainText>true</PlainText>
        </Password>
        <Description>Primary User Account</Description>
        <DisplayName>SamCux</DisplayName>
        <Group>Administrators</Group>
        <Name>SamCux</Name>
    </LocalAccount>
</LocalAccounts>
```

### Privacy Settings

The configuration automatically:

- Disables Cortana
- Disables location services
- Disables advertising ID
- Disables WiFi Sense
- Disables telemetry (where possible)

### Regional Settings

- **Time Zone:** UTC (can be changed post-installation)
- **Language:** English (US)
- **Keyboard:** US QWERTY

## 🛡️ Security Features

- **Windows Defender enabled** by default
- **Windows Update enabled** for security patches
- **User Account Control (UAC)** configured appropriately
- **Local account** instead of Microsoft account for privacy

## 🚨 Important Notes

- **Backup your data** before proceeding
- **UEFI/Secure Boot** must be enabled in BIOS
- **TPM 2.0** must be enabled for Windows 11
- This process will **wipe the entire drive**
- **Test in a virtual machine** first if unsure

## 📁 Files in This Directory

- `autounattend.xml` - Main configuration file
- `README.md` - This documentation
- `screenshots/` - Visual guide screenshots

## 🔧 Troubleshooting

### Common Issues

**Issue:** Installation stops at region selection
**Solution:** Ensure autounattend.xml is in USB root directory

**Issue:** Computer name not applied
**Solution:** Verify XML syntax in ComputerName section

**Issue:** Local account not created
**Solution:** Check LocalAccounts configuration in XML

### Getting Help

If you encounter issues:

1. Check the XML file syntax
2. Verify USB creation with Rufus
3. Ensure UEFI/TPM settings in BIOS
4. Create an issue in this repository

## 🎉 What's Next?

After successful installation:

1. Run Windows Update to get latest patches
2. Proceed to [Applications Setup](../02-Applications/)
3. Configure [Terminal Environment](../03-Terminal/)
4. Apply [Visual Customizations](../04-Customizations/)

---

**💡 Pro Tip:** Create a backup of your configured autounattend.xml file for future use!
