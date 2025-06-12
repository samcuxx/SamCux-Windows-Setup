# 🎨 Windows 11 Customizations

## Overview

Transform your Windows 11 experience with professional visual enhancements and productivity modifications.

## 📋 Customization Categories

### 🖱️ Mouse Cursors

- **macOS-style cursors** for a premium look
- **Professional appearance** for development work
- **Easy installation** with step-by-step guide

### 🪟 Windhawk Modifications

- **System-level enhancements** for productivity
- **Taskbar customizations** for better workflow
- **Explorer improvements** for file management

### 🖼️ Wallpapers

- **DesktopPro** - Personal wallpaper management
- **Dynamic wallpaper rotation**
- **Professional backgrounds** collection

## 🖱️ Mouse Cursor Setup

### Overview

Replace Windows default cursors with sleek macOS-style cursors for a more premium appearance.

**📁 Location:** [`Mouse-Cursors/`](./Mouse-Cursors/)

### Installation Steps

1. **Download cursor files** from this repository
2. **Copy cursor files** to Windows Cursors directory:
   ```
   Source: C:\Users\SamCux\Desktop\macOS cursors for Windows
   Destination: C:\Windows\Cursors
   ```
3. **Apply cursors** through Windows Settings:
   - Open **Settings** → **Personalization** → **Themes**
   - Click **Mouse cursor**
   - Select **Browse** and choose the new cursor files
   - Apply changes and restart if necessary

### Cursor Files Included

- `Normal Select.cur` - Standard pointer
- `Working in Background.ani` - Busy indicator
- `Text Select.cur` - Text selection
- `Hand.cur` - Link selection
- `Move.cur` - Move/drag operations
- `Resize Vertical.cur` - Vertical resize
- `Resize Horizontal.cur` - Horizontal resize
- `Resize Diagonal 1.cur` - Diagonal resize
- `Resize Diagonal 2.cur` - Diagonal resize

### Backup Original Cursors

**Important:** Always backup original Windows cursors before replacing:

```powershell
# Create backup directory
mkdir "C:\Windows\Cursors\Backup"

# Copy original cursors
copy "C:\Windows\Cursors\*.cur" "C:\Windows\Cursors\Backup\"
copy "C:\Windows\Cursors\*.ani" "C:\Windows\Cursors\Backup\"
```

## 🪟 Windhawk Modifications

### What is Windhawk?

Windhawk is a platform for Windows customization that allows system-level modifications through community-created mods.

**📁 Location:** [`Windhawk-Mods/`](./Windhawk-Mods/)

### Installation

1. **Download Windhawk** from [official website](https://windhawk.net/)
2. **Install with default settings**
3. **Restart Windows** for full functionality

### Available Modifications

#### 📁 File Management

- **Better file sizes in Explorer details** - More readable file sizes
- **Modernize Folder Picker Dialog** - Updated folder selection interface

#### 🖥️ Taskbar Enhancements

- **Middle click to close on the taskbar** - Close apps with middle mouse click
- **Taskbar auto-hide when maximized** - Auto-hide taskbar for maximized windows
- **Taskbar height and icon size** - Customize taskbar dimensions
- **Taskbar Volume Control** - Quick volume adjustment from taskbar
- **Taskbar Clock Customization** - Enhanced clock display and formatting

#### 🎨 Visual Styling

- **Windows 11 Notification Center Styler** - Custom notification appearance
- **Windows 11 Start Menu Styler** - Personalized Start menu design
- **Windows 11 Taskbar Styler** - Advanced taskbar visual customization

### Mod Configuration Files

Each modification comes with a configuration file:

#### File Structure

```
04-Customizations/Windhawk-Mods/
├── better-file-sizes-explorer.txt
├── middle-click-close-taskbar.txt
├── modernize-folder-picker.txt
├── taskbar-auto-hide-maximized.txt
├── taskbar-clock-customization.txt
├── taskbar-volume-control.txt
├── taskbar-height-icon-size.txt
├── notification-center-styler.txt
├── start-menu-styler.txt
└── taskbar-styler.txt
```

### Installing Mods

1. **Open Windhawk**
2. **Navigate to Mods** section
3. **Click "Install a new mod"**
4. **Copy the mod code** from the respective `.txt` file
5. **Paste and install**
6. **Configure settings** as needed
7. **Apply changes**

### Recommended Mod Settings

#### Taskbar Height and Icon Size

- **Taskbar Height:** 40px (default) or 48px (larger)
- **Icon Size:** 24px (default) or 28px (larger)
- **Spacing:** 8px between icons

#### Auto-hide When Maximized

- **Trigger:** When window is maximized
- **Delay:** 500ms before hiding
- **Animation:** Smooth transition

#### Better File Sizes

- **Format:** Human-readable (KB, MB, GB)
- **Precision:** 2 decimal places
- **Show full path:** In tooltip

## 🖼️ Wallpaper Management

### DesktopPro (Coming Soon)

Personal wallpaper management application for dynamic desktop backgrounds.

**📁 Location:** [`Wallpapers/`](./Wallpapers/)

### Features

- **Dynamic rotation** of wallpapers
- **Time-based themes** (day/night cycles)
- **Category organization** (Nature, Abstract, Minimal, etc.)
- **Custom intervals** for wallpaper changes
- **Multi-monitor support**

### Current Wallpaper Collection

#### Categories Available

1. **Minimal/Abstract**

   - Clean, professional backgrounds
   - Solid colors and gradients
   - Geometric patterns

2. **Nature/Landscape**

   - High-resolution nature photography
   - Landscape and scenery
   - Seasonal themes

3. **Technology/Development**

   - Code-themed backgrounds
   - Dark mode friendly
   - Programming language themes

4. **Professional/Business**
   - Corporate-friendly designs
   - Neutral color schemes
   - Professional photography

### Manual Wallpaper Setup

Until DesktopPro is released, use these methods:

#### Windows 11 Slideshow

1. **Right-click desktop** → Personalize
2. **Select "Slideshow"** from Background dropdown
3. **Browse** to wallpaper folder
4. **Set change frequency** (1 hour recommended)
5. **Enable "Shuffle"** for random selection

#### Third-party Alternatives

- **DisplayFusion** - Advanced multi-monitor wallpaper management
- **Wallpaper Engine** - Animated and interactive wallpapers
- **John's Background Switcher** - Simple automatic wallpaper rotation

## 🔧 Advanced Customizations

### Registry Tweaks (Optional)

**⚠️ Warning:** Always backup registry before making changes.

#### Disable Windows Web Search

```reg
[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Search]
"BingSearchEnabled"=dword:00000000
```

#### Disable Cortana

```reg
[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search]
"AllowCortana"=dword:00000000
```

### PowerShell Customization Script

A comprehensive script to apply multiple customizations automatically:

**📁 Location:** [`apply-customizations.ps1`](./apply-customizations.ps1)

## 📸 Screenshots & Previews

### Before vs After

**📁 Location:** [`../06-Screenshots/customizations/`](../06-Screenshots/customizations/)

- `desktop-before.png` - Default Windows 11 desktop
- `desktop-after.png` - Fully customized desktop
- `taskbar-comparison.png` - Taskbar before/after modifications
- `cursor-showcase.png` - New cursor designs
- `wallpaper-gallery.png` - Wallpaper collection preview

## 🔄 Maintenance & Updates

### Keeping Modifications Updated

1. **Windhawk updates** - Check monthly for mod updates
2. **Cursor maintenance** - Re-apply after major Windows updates
3. **Wallpaper refresh** - Add new wallpapers quarterly
4. **Backup configurations** - Export settings before major changes

### Troubleshooting

#### Cursor Issues

- **Problem:** Cursors revert to default
- **Solution:** Re-apply through Personalization settings

#### Windhawk Mod Conflicts

- **Problem:** Some mods don't work together
- **Solution:** Disable conflicting mods and test individually

#### Performance Impact

- **Monitor:** System performance after applying mods
- **Optimize:** Disable unnecessary visual effects if needed

## 🎯 Next Steps

After applying customizations:

1. Configure your [Development Environment](../05-Development/)
2. Take [Screenshots](../06-Screenshots/) of your setup
3. Fine-tune settings based on personal preferences

---

**💡 Pro Tip:** Apply customizations gradually and test each change to ensure system stability!
