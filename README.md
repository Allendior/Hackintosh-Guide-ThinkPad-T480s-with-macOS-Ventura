# Hackintosh-Guide-ThinkPad-T480s-with-macOS-Ventura
Welcome to my guide for installing macOS Ventura on the ThinkPad T480s. This project is designed to help any ThinkPad T480s owner who wants to experience macOS on their hardware. Whether you're a hackintosh enthusiast or new to macOS installations, this guide is tailored for you!
---

## 🎯 Project Goal

To help **ThinkPad T480s owners** install macOS Ventura with ease, leveraging a prebuilt OpenCore EFI configuration. This guide is for anyone who loves tinkering with hardware and software, just like I do!

---

## 🔧 Hardware Configuration

Here’s the hardware setup tested and confirmed to work:

| Component     | Specification                |
|---------------|------------------------------|
| **CPU**       | Intel Core i5-8350u          |
| **GPU**       | Intel UHD Graphics 620       |
| **RAM**       | 24GB (8GB soldered + 16GB Samsung stick) |
| **Touchpad**  | Elan SMBus                   |
| **Audio**     | Realtek ALC257               |
| **Wi-Fi**     | Intel Wireless-AC 8265      |
| **Ethernet**  | Intel I219-LM                |
| **SSD**       | Intel 7600p 256GB            |

---

## ⚠️ Important Notes

- **Ventura Users:** You can use Wi-Fi without issues during the setup.  
- This EFI is specifically configured for **macOS Ventura**.  
- Always follow the **"Downloading macOS"** section in the Dortania guide to obtain macOS safely and correctly:  
  [Guide to Downloading macOS](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html#downloading-macos)  
  **Note:** Support will not be provided if macOS is obtained from other sources.

---

## 🌐 What’s Included

- A **prebuilt OpenCore EFI folder** for easy installation.  
- Full support for Intel Wi-Fi cards and all essential hardware components.

---

## 🛠 BIOS Configuration

Before starting, configure your BIOS as follows:

1. **Disable:**
   - Wake On LAN: `Config -> Network -> Wake On LAN -> Disabled`
   - Wake On LAN from Dock: `Config -> Network -> Wake On LAN from Dock -> Disabled`
   - Security Chip: `Security -> Security Chip -> Disabled`
   - VT-d: `Security -> Virtualization -> Intel (R) VT-d Features -> Disabled`
   - Secure Boot: `Security -> Secure Boot -> Disabled`
   - Intel SGX: `Security -> Intel(R) SGX Control -> Disabled`

2. **Enable:**
   - Hyper-Threading: `Config -> CPU -> Intel (R) Hyper-Threading Technology -> Enabled`
   - Virtualization: `Security -> Virtualization -> Intel (R) Virtualization Technology -> Enabled`

3. **Startup Settings:**
   - Boot Mode: `Startup -> UEFI/Legacy Boot -> UEFI Only`
   - CSM Support: `Startup -> CSM Support -> No`

---

## 🖥 Installation Process

### Step 1: Prepare the USB Installer
1. Download the latest **macOS Ventura** using the Dortania guide.
2. Use **OpenCore Configurator** or **OpenCore Auxiliary Tools** to prepare a bootable USB with the provided EFI folder.
3. Mount the EFI partition on the USB and copy the provided EFI folder into it.

### Step 2: BIOS Configuration
- Ensure your BIOS settings match those listed above.

### Step 3: Installation
1. Boot into the USB installer.
2. Follow the macOS installation guide to install Ventura on your SSD.
3. After installation, copy the EFI folder to your SSD's EFI partition.

---

## ✅ Working Features

The following features work flawlessly after installation:
- **Trackpad & Keyboard** (Gestures supported)
- **Wi-Fi & Bluetooth**
- **Thunderbolt 3** ports
- **Audio**: Headphones, internal speakers
- **Battery Management** (Although "Service Recommended" message appears)

---

## 🖱️ Post-Installation Step

After macOS is installed, you’ll need to adjust the trackpad settings. By default, macOS registers all clicks as force clicks. Here’s how to fix it:  
1. Go to **System Settings → Trackpad**.  
2. Uncheck the box for **"Force Click and haptic feedback"**.

---

## 📋 Future Plans

I’m currently working on refining this setup and improving compatibility with newer macOS versions. Contributions and feedback are welcome!

---

