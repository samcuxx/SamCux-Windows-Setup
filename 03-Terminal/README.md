# ⚡ Terminal Setup Guide

## Overview

Professional terminal setup using **Git Bash** with **Starship** prompt for an enhanced development experience.

## 🎯 What You'll Get

- **Modern terminal prompt** with Git integration
- **Cross-platform compatibility** (works on Windows, macOS, Linux)
- **Customizable themes** and configurations
- **Enhanced productivity** with context-aware prompts
- **Professional appearance** for development work

## 📋 Prerequisites

- Windows 11 (fresh installation preferred)
- Administrator access for installations
- Internet connection for downloading tools

## 🛠️ Installation Guide

### Step 1: Install Git for Windows

Git for Windows includes Git Bash, which will be our primary terminal.

1. **Download Git for Windows** from [git-scm.com](https://git-scm.com/download/win)
2. **Run the installer** with these recommended settings:
   - ✅ **Git Bash Here** (context menu integration)
   - ✅ **Git GUI Here** (optional GUI access)
   - ✅ **Associate .git\* configuration files**
   - ✅ **Associate .sh files to be run with Bash**
   - ✅ **Use Git and optional Unix tools from the Command Prompt**
   - ✅ **Use the OpenSSL library**
   - ✅ **Checkout Windows-style, commit Unix-style line endings**
   - ✅ **Use MinTTY (the default terminal of MSYS2)**

### Step 2: Install a Nerd Font

Starship requires a Nerd Font for proper icon display.

#### Recommended Font: JetBrains Mono Nerd Font

1. **Download** from [Nerd Fonts website](https://www.nerdfonts.com/font-downloads)
2. **Extract the ZIP** file
3. **Select all .ttf files** and right-click → "Install for all users"
4. **Configure Git Bash** to use the font:
   - Right-click Git Bash title bar → Options
   - Text → Font → JetBrains Mono NL (or your chosen Nerd Font)
   - Set size to 11-12pt for optimal readability

### Step 3: Install Starship

Starship is a cross-shell prompt that adds modern functionality to any terminal.

#### Windows Installation

**Option A: Using PowerShell (Recommended)**

```powershell
# Run in PowerShell as Administrator
winget install --id Starship.Starship
```

**Option B: Using Installer**

1. Download the latest `.msi` installer from [Starship releases](https://github.com/starship/starship/releases)
2. Choose the correct architecture (usually `x86_64-pc-windows-msvc.msi`)
3. Run the installer with default settings

### Step 4: Configure Starship for Git Bash

1. **Open Git Bash**
2. **Edit the `.bashrc` file:**
   ```bash
   cd ~
   nano .bashrc
   ```
3. **Add Starship initialization** at the end of the file:
   ```bash
   # Initialize Starship prompt
   eval "$(starship init bash)"
   ```
4. **Save and exit** (Ctrl+X, then Y, then Enter in nano)
5. **Restart Git Bash** or run:
   ```bash
   source ~/.bashrc
   ```

## 🎨 Configuration

### Default Configuration

Starship works great out of the box, but you can customize it extensively.

### Custom Configuration

Create a configuration file for advanced customization:

```bash
# Create config directory
mkdir -p ~/.config
touch ~/.config/starship.toml
```

### Example Configuration

Add this to `~/.config/starship.toml` for a professional setup:

```toml
# Starship Configuration
format = """
[╭─user@host](bold blue) $all[╰─➤](bold blue) """

[username]
style_user = "green bold"
style_root = "red bold"
format = "[$user]($style)"
disabled = false
show_always = true

[hostname]
ssh_only = false
format = "[$hostname](bold red)"
disabled = false

[directory]
style = "blue bold"
read_only = " 🔒"
truncation_length = 4
truncate_to_repo = false

[git_branch]
symbol = "🌱 "
truncation_length = 4
truncation_symbol = ""

[git_status]
ahead = "⇡${count}"
diverged = "⇕⇡${ahead_count}⇣${behind_count}"
behind = "⇣${count}"

[nodejs]
symbol = " "

[python]
symbol = " "

[package]
symbol = " "
```

## 🔗 Integration with External Repository

This terminal setup is part of a larger customization project:

**🔗 Complete Terminal Guide:** [samcuxx/custom-terminal-guide](https://github.com/samcuxx/custom-terminal-guide)

### Features from External Repository

- **Additional themes** and configurations
- **Advanced Starship presets**
- **Cross-platform compatibility**
- **Regular updates** and improvements

### Syncing Configurations

To stay updated with the latest configurations:

```bash
# Clone the terminal guide repository
git clone https://github.com/samcuxx/custom-terminal-guide.git ~/terminal-guide

# Copy latest Starship configuration
cp ~/terminal-guide/Config/Starship/.config/starship.toml ~/.config/starship.toml

# Reload configuration
source ~/.bashrc
```

## 🎯 Advanced Setup

### Windows Terminal Integration

For the best experience, use Windows Terminal with Git Bash:

1. **Install Windows Terminal** from Microsoft Store
2. **Add Git Bash profile:**
   - Settings → Add a new profile
   - Command line: `"C:\Program Files\Git\bin\bash.exe" -i -l`
   - Starting directory: `%USERPROFILE%`
   - Icon: `"C:\Program Files\Git\mingw64\share\git\git-for-windows.ico"`

### PowerShell Configuration (Optional)

If you also use PowerShell, add Starship there too:

```powershell
# Add to PowerShell profile
Add-Content $PROFILE "Invoke-Expression (&starship init powershell)"
```

## 🔧 Troubleshooting

### Common Issues

**Issue:** Icons not displaying properly
**Solution:** Ensure you have a Nerd Font installed and configured

**Issue:** Starship command not found
**Solution:** Restart terminal or check PATH environment variable

**Issue:** Configuration not loading
**Solution:** Verify file path: `~/.config/starship.toml`

### Performance Optimization

For faster terminal startup:

```toml
# Add to starship.toml
[character]
success_symbol = "[➜](bold green)"
error_symbol = "[➜](bold red)"

# Disable slow modules if needed
[package]
disabled = true
```

## 📸 Screenshots

### Before (Default Git Bash)

_Standard Git Bash prompt - functional but basic_

### After (Git Bash + Starship)

_Modern, informative prompt with Git integration and visual enhancements_

## 🎉 What's Next?

After setting up your terminal:

1. Explore [Visual Customizations](../04-Customizations/)
2. Configure your [Development Environment](../05-Development/)
3. Check out additional themes in the [custom-terminal-guide](https://github.com/samcuxx/custom-terminal-guide)

---

**💡 Pro Tip:** Bookmark the [Starship documentation](https://starship.rs/config/) for advanced configuration options!
