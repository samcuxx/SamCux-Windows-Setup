# 📱 Applications Setup Guide

## Overview

Complete software installation guide for a professional Windows 11 development environment. Applications are organized by category for easy navigation and installation.

## 🗂️ Application Categories

### 🛠️ Development Tools

**Essential tools for software engineering and development work.**

#### Code Editors & IDEs

- **[Visual Studio Code](https://code.visualstudio.com/)** - Primary code editor
- **[Cursor](https://cursor.sh/)** - AI-powered code editor
- **[Trae](https://www.trae.ai/)** - AI productivity tool
- **[Android Studio](https://developer.android.com/studio)** - Android development
- **[GitHub Desktop](https://desktop.github.com/)** - Git GUI client

#### Development Utilities

- **[Git Bash](https://git-scm.com/download/win)** - Version control
- **[Node.js](https://nodejs.org/)** - JavaScript runtime
- **[Python](https://www.python.org/downloads/)** - Programming language


### Design & Creative

**Applications for UI/UX design, graphics, and creative work.**

#### Design Software

- **[Adobe Photoshop 2025](https://www.adobe.com/products/photoshop.html)** - Professional image editing
- **[Figma](https://www.figma.com/)** - UI/UX design


#### Content Creation

- **[OBS Studio](https://obsproject.com/)** - Screen recording/streaming
- **[Wondershare Filmora 14](https://filmora.wondershare.com/)** - Video editing

### 🔧 System Utilities

**Tools for system optimization, monitoring, and maintenance.**

#### System Management

- **[Windhawk](https://windhawk.net/)** - Windows system modifications
- **[TranslucentTB](https://github.com/TranslucentTB/TranslucentTB)** - Transparent taskbar
- **[Flow Launcher](https://www.flowlauncher.com/)** - Quick file/app launcher
- **[PowerToys](https://github.com/microsoft/PowerToys)** - Windows utilities
- **[7-Zip](https://www.7-zip.org/)** - File compression
- **[Winrar](https://www.winrar.com)** - File compression

#### Networking & Transfer

- **[LocalSend](https://localsend.org/)** - Cross-platform file sharing
- **[Internet Download Manager](https://www.internetdownloadmanager.com/)** - Download accelerator

### 📊 Productivity

**Office applications, note-taking, and productivity tools.**

#### Office Suite

- **[Microsoft Office 365](https://www.microsoft.com/microsoft-365)** - Word, Excel, PowerPoint

#### Note-Taking & Organization

- **[Notion](https://www.notion.so/)** - All-in-one workspace

#### Communication

- **[Microsoft Teams](https://www.microsoft.com/en-us/microsoft-teams/group-chat-software)** - Team collaboration
- **[WhatsApp Desktop](https://www.whatsapp.com/download)** - Messaging
- **[Discord](https://discord.com/)** - Community communication
- **[Zoom](https://zoom.us/download)** - Video conferencing
- **[Telegram](https://telegram.com/download)** - Video conferencing
- 

#### AI & Productivity

- **[ChatGPT Desktop](https://openai.com/chatgpt/desktop/)** - AI assistant

### 🎵 Media & Entertainment

**Media players, streaming apps, and entertainment software.**

#### Music & Audio

- **[WinMed Media Player](https://github.com/samcuxx/WinMed-Media-Player/releases)** - Music streaming
- **[Spotify](https://www.spotify.com/download/)** - Music streaming
- **[Spicetify](https://spicetify.app/)** - Spotify customization
- **[AIMP](https://www.aimp.ru/)** - Audio player
- **[VLC Media Player](https://www.videolan.org/vlc/)** - Universal media player

#### Video & Streaming

- **[Netflix](https://www.microsoft.com/store/apps/9wzdncrfj3tj)** - Video streaming
- **[YouTube Desktop](https://www.youtube.com/)** - YouTube client

#### System & Browser

- **[Google Chrome](https://www.google.com/chrome/)** - Web browser
- **[Zen Browser](https://zen-browser.app/)** - Privacy-focused browser
- **[Microsoft Edge](https://www.microsoft.com/edge)** - Built-in browser

#### Windows Built-in Apps

- **[Terminal](ms-settings:taskmanager)** - Windows Terminal
- **[File Explorer](ms-settings:)** - Built-in file manager
- **[Photos](ms-photos:)** - Built-in photo viewer
- **[Phone Link](https://www.microsoft.com/en-us/p/your-phone/9nmpj99vjbwv)** - Connect Android/iPhone
- **[Settings](ms-settings:)** - Windows Settings

### 🎯 Personal & Custom Apps

**Personal projects and custom applications.**

#### Custom Applications

- **Desktop Pro** - Personal wallpaper management app (Coming Soon)

## 🎶 Special Setup: Spotify + Spicetify

### What is Spicetify?

Spicetify is a command-line tool to customize the Spotify client with themes, custom apps, and additional features.

### Installation Steps

1. **Install Spotify** from the [official website](https://www.spotify.com/download/) or Microsoft Store
2. **Install Spicetify** using PowerShell:
   ```powershell
   iwr -useb https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.ps1 | iex
   ```
3. **Apply a theme:**
   ```powershell
   spicetify config current_theme Dribbblish
   spicetify apply
   ```

## 📦 Bulk Installation Options

### Package Managers

Consider using package managers for easier installation:

#### Winget (Windows Package Manager)

```powershell
# Install multiple apps at once
winget install Microsoft.VisualStudioCode
winget install Cursor.Cursor
winget install Git.Git
winget install Google.Chrome
winget install Spotify.Spotify
winget install Discord.Discord
winget install Notion.Notion
winget install OBSProject.OBSStudio
winget install VideoLAN.VLC
winget install WhatsApp.WhatsApp
winget install GitHub.GitHubDesktop
winget install Microsoft.PowerToys
winget install 7zip.7zip
```

#### Chocolatey

```powershell
# Install Chocolatey first
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# Install apps
choco install vscode cursor git googlechrome spotify discord notion obs-studio vlc whatsapp github-desktop powertoys 7zip -y
```

## 🔄 Installation Scripts

### PowerShell Installation Script

A comprehensive PowerShell script is available to install all essential applications automatically.

**📁 Location:** [`install-apps.ps1`](./install-apps.ps1)

### Usage

```powershell
# Run as Administrator
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
.\install-apps.ps1
```

## 📋 Application Checklist

Use this checklist to track your installation progress:

### Essential (Priority 1)

- [ ] [Git for Windows](https://git-scm.com/download/win)
- [ ] [Visual Studio Code](https://code.visualstudio.com/)
- [ ] [Cursor](https://cursor.sh/)
- [ ] [Google Chrome](https://www.google.com/chrome/)
- [ ] [7-Zip](https://www.7-zip.org/)
- [ ] [PowerToys](https://github.com/microsoft/PowerToys)

### Development (Priority 2)

- [ ] [Node.js](https://nodejs.org/)
- [ ] [Python](https://www.python.org/downloads/)
- [ ] [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [ ] [Postman](https://www.postman.com/downloads/)
- [ ] [GitHub Desktop](https://desktop.github.com/)
- [ ] [Android Studio](https://developer.android.com/studio)

### Daily Use (Priority 3)

- [ ] [Spotify](https://www.spotify.com/download/) + [Spicetify](https://spicetify.app/)
- [ ] [Discord](https://discord.com/)
- [ ] [Notion](https://www.notion.so/)
- [ ] [WhatsApp Desktop](https://www.whatsapp.com/download)
- [ ] [ChatGPT Desktop](https://openai.com/chatgpt/desktop/)

### Professional (Priority 4)

- [ ] [Adobe Photoshop 2025](https://www.adobe.com/products/photoshop.html)
- [ ] [Microsoft Office 365](https://www.microsoft.com/microsoft-365)
- [ ] [OBS Studio](https://obsproject.com/)
- [ ] [Wondershare Filmora 14](https://filmora.wondershare.com/)

### System Enhancement (Priority 5)

- [ ] [Windhawk](https://windhawk.net/)
- [ ] [TranslucentTB](https://github.com/TranslucentTB/TranslucentTB)
- [ ] [Flow Launcher](https://www.flowlauncher.com/)
- [ ] [LocalSend](https://localsend.org/)
- [ ] [AIMP](https://www.aimp.ru/)
- [ ] [VLC Media Player](https://www.videolan.org/vlc/)

## 🎯 Next Steps

After installing your applications:

1. Configure [Terminal Environment](../03-Terminal/)
2. Apply [Visual Customizations](../04-Customizations/)
3. Set up [Development Environment](../05-Development/)

---

**💡 Pro Tip:** Use winget or chocolatey for bulk installation to save time!
