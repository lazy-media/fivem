# 🚀 FiveM Server Setup (QB-Core Version)

**Complete FiveM server setup with 400+ modded vehicles, map mods, and everything you need!**

[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://www.paypal.com/paypalme/lazymediawa) 
[![GitLab Mirror](https://img.shields.io/badge/Mirror-GitLab-orange.svg)](https://link.lazymedia.media/gitlab-fivem)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000.svg)](https://link.lazymedia.media/ytchannel)

---

## ⚠️ IMPORTANT NOTICE
**Repository Size:** ~12GB  
**Credits:** This is a curated collection, not original work. All credits go to original creators.

### Key Features:
- Latest server artifacts included
- 400+ carefully selected vehicles
- Organized, renamed, and de-duplicated resources
- Pre-configured vMenu addons
- Detailed setup instructions

---

## 🔗 Essential Resources

| Resource | Link |
|----------|------|
| FiveM Docs | [Documentation](https://docs.fivem.net/docs/server-manual/setting-up-a-server-vanilla/) |
| Latest Server Build | [Download (Build 12629)](https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master/12629-1035d9b5ef145feff915708e4c02a3300e3a53c9/fx.tar.xz) |
| Vehicle Packs | [CarPack0](https://www.gta5-mods.com/) • [CarPack1](https://github.com/five-m/Vehicles/tree/master) • [PLOKS_CARS](https://github.com/PLOKMJNB/FiveM-Civ-Car-Pack) • [CarPack3](https://github.com/Zerofour04/Fivem-BigCarPack) |
| Admin Tools | [EasyAdmin](https://github.com/Blumlaut/EasyAdmin) • [LambdaMenu](https://github.com/citizenfx/project-lambdamenu) • [vMenu](https://github.com/TomGrobbe/vMenu) |

---

## 🛠️ Setup Instructions

### Prerequisites
- Ubuntu Server 20.04+
- Recommended tools:
  - [Webmin](https://webmin.com/download/)
  - MobaXterm or XPipe for file transfer

### 🚀 Installation Process

#### Part 1: Server Setup

# Download and extract server files

```bash
mv fx FXServer
```

# Configure service

```bash
sudo cp fxserver.service /etc/systemd/system/
sudo systemctl start fxserver
sudo systemctl enable fxserver
```

#### Part 2: TXAdmin Configuration

  1.  Access TXAdmin at http://YOUR.SERVER.IP.HERE:40120

  2.  Select your preferred framework (QB-Core recommended)

#### Part 3: Directory Structure

Navigate to your resources folder:

```bash
cd /home/ubuntu/FXServer/server/txData/QBCoreFramework_*/resources/
```

#### Part 4: Adding Resources

  1.  Copy [vehicles] and [map_mods] folders to your resources directory

  2.  Add to server.cfg:

```cfg
# Vehicle Packs
ensure [vehicles]
ensure [CarPack0]
ensure [CarPack1]
ensure PLOKS_CARS
ensure [CarPack3]

# Map Mods
ensure [map_mods]
```

## 🎁 BONUS FEATURES
vMenu Configuration

  -  Use the provided vMenu_addon_conf.json to enable all vehicles in vMenu

Admin Vehicle

  -  Spawn secret admin vehicle with name: sfbc3

---

## 💖 Support This Project

[![Donate](https://img.shields.io/badge/Donate-Support_My_Work-FF6F00?style=for-the-badge&logo=paypal)](https://www.paypal.com/paypalme/lazymediawa)

## 🔗 Additional Information

[![GitLab Mirror](https://img.shields.io/badge/GitLab_Backup-Repository-orange?style=for-the-badge&logo=gitlab)](https://link.lazymedia.media/gitlab-fivem)
[![YouTube Channel](https://img.shields.io/badge/YouTube-Channel-FF0000?style=for-the-badge&logo=youtube)](https://link.lazymedia.media/ytchannel)
[![Website](https://img.shields.io/badge/Lazy_Media-Website-00AA00?style=for-the-badge&logo=wordpress)](https://link.lazymedia.media/UODds)