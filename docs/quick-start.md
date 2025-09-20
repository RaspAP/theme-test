---
title: Quick Start
hide:
  - navigation
---

RaspAP gives you two different ways to get up and running quickly. The simplest approach is to use our <a href="https://github.com/RaspAP/raspap-webgui/releases/latest">custom OS image</a> with RaspAP preinstalled. This option eliminates guesswork and gives you a base upon which to build. An alternative method is to execute the Quick installer on an existing <a href="#distros">compatible OS</a>.

## Custom OS
Custom Raspberry Pi OS Lite images with the latest RaspAP are available for <a href="https://github.com/RaspAP/raspap-webgui/releases/latest">direct download</a>. This includes both 32- and 64-bit builds for ARM architectures.

> Note
> As a courtesy, starting with v3.4.1, we've made available Torrent files for the images. The downloads will still come from Github, but will be able to completely finish without falling victim to Github's token timeout issues. Please connect with us if you still have issues downloading.

| Distribution | Debian version | Kernel version | RaspAP version | Size |
| ------------ | -------------- | -------------- | -------------- | ---- |
| Raspberry Pi OS (64-bit) Lite | 12 (bookworm) | 6.6 | Latest | 869 MB |
| Raspberry Pi OS (32-bit) Lite | 12 (bookworm) | 6.6 | Latest | 897 MB |

These images are automatically generated with each release of RaspAP and are made <a href="https://github.com/RaspAP/raspap-webgui/releases/latest">available here</a>. You may choose between an `arm64` or `armhf` (32-bit) based build.

After downloading your desired image, use a utility such as the Raspberry Pi Imager or <a href="https://www.balena.io/etcher">balenaEtcher</a> to flash the OS image onto a microSD card. Insert the card into your device and boot it up. The latest RaspAP release with the most popular components will be active and ready for you to configure.

## Quick Installer
Alternatively, begin with a clean install of the latest release of a <a href="#distros">supported Linux distribution</a>. In the example below, <a href="https://www.raspberrypi.com/software/operating-systems/#raspberry-pi-os-64-bit">Raspberry Pi OS (64-bit) Lite</a> is used.

Update your OS to its latest version, including the kernel and firmware, followed by a reboot:
```
sudo apt-get update
sudo apt-get full-upgrade
sudo reboot
```
Set the WiFi country in `raspi-config`'s Localisation Options:
```
sudo raspi-config
```
Invoke RaspAP's Quick Installer:
```
curl -sL https://install.raspap.com | bash
```

The <a href="https://docs.raspap.com/get-started/quick-installer/">Quick installer</a> will complete the steps in the <a href="https://docs.raspap.com/get-started/manual/">manual installation</a> for you. At the end of the install process, accept the prompt to reboot your system.

## Initial settings
After completing either of these setup options, the wireless AP network will be configured as follows:  

- IP address: 10.3.141.1  
- Username: admin  
- Password: secret  
- DHCP range: 10.3.141.50 — 10.3.141.254  
- SSID: RaspAP  
- Password: ChangeMe  

It is strongly recommended that you change these default credentials in RaspAP's Authentication and Hotspot > Security panels.

Your AP's <a href="https://docs.raspap.com/features-core/ap-basics/">basic settings</a> and many <a href="https://docs.raspap.com/features-core/ap-basics/#advanced-options">advanced options</a> may now be modified by RaspAP.

## Supported Distributions
<a name="distros"></a>
RaspAP was originally made for Raspberry Pi OS, but now also installs on the following Debian-based distros:

| Distribution | Release | Architecture | Support | 
| ------------ | ------- | ------------ | ------- |
| Raspberry Pi OS | (64-bit) Lite Bookworm | ARM | Official | 
| Raspberry Pi OS | (32-bit) Lite Bookworm | ARM | Official | 
| Raspberry Pi OS | (64-bit) Desktop Bookworm | ARM | Official | 
| Raspberry Pi OS | (64-bit) Lite Bullseye | ARM | Official | 
| Raspberry Pi OS | (32-bit) Lite Bullseye | ARM | Official | 
| Armbian  | 23.11 (Jammy)  | ARM  | Beta  |
| Debian | Bookworm | ARM / x86_64 | Beta |

<img src="/assets/images/supported-distros.png" style="max-width: 50%;" alt="Supported distributions">

You are also encouraged to try RaspAP's community-led <a href="https://github.com/RaspAP/raspap-docker">Docker container</a>.

## Documentation and more
Our <a href="https://docs.raspap.com/faq/">frequently asked questions (FAQ)</a> are continuously updated and are a great place to start. Need help not covered in the FAQ, have an idea, or want to share your project with the RaspAP community? Head over to our <a href="https://github.com/RaspAP/raspap-webgui/discussions">GitHub Discussions</a>. For everything else and more detailed information, dive into our official <a href="https://docs.raspap.com">documentation</a>.