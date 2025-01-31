# FiveM Server Setup
FiveM Server Setup. QB-Core Version. Comes with modded vehicles, map mods, everything you need.

# NOTICE

- I take no credit in creating any of these. I simply just gathered all the resources necessary to run a FiveM server and put it all in one place.
- I tried to make this as easy as possible for me or anyone else who needs this.
- This repository has the latest server artifacts

# Resources

- [FiveM Docs](https://docs.fivem.net/docs/server-manual/setting-up-a-server-vanilla/)
- [FiveM Server Download (Latest Build Number 12629)](https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master/12629-1035d9b5ef145feff915708e4c02a3300e3a53c9/fx.tar.xz)
- [GTA5 Mods](https://www.gta5-mods.com/)
- [CarPack1](https://github.com/five-m/Vehicles/tree/master)
- [CarPack2](https://github.com/PLOKMJNB/FiveM-Civ-Car-Pack)
- [CarPack3](https://github.com/Zerofour04/Fivem-BigCarPack?tab=readme-ov-file)

# Assumptions

- This repository assumes your Ubuntu Server is setup as standard
- This repository assumes your Ubuntu Server username is `ubuntu`
- Please Double check any files to make sure your paths are correct
- This repository assumes your main home directory is `/home/ubuntu/`

# Setup

- Install Ubuntu Server 20.04 or higher
- Log into Ubuntu Server via SSH
- Make yourself root with `sudo su`

# Instructions

- This repository is meant to be downloaded as a whole.
- Please follow these instructions carefully.

## Part 1

- Extract `fx.tar.xz` with `tar xf fx.tar.xz`
- Rename this FX Server folder to `FXServer`
- Place the `fxserver.service` file in `/etc/systemd/system`
- Start the service with `systemctl start fxserver`
- Enable this service to start at system boot with `systemctl enable fxserver`

# Part 2

- Navigate to the `http://YOUR.SERVER.IP.HERE:40120` from another PC
  - This should open up TXAdmin
  - Setup TXAdmin as you would

- At the TXADMIN page for Picking your Recipe, Choose which every one you want, I prefer QB-Core Framework, but these have been tested on both ESX and QB-Core.

# Part 3

- When TXAdmin is complete, ssh back into the ubuntu server.
- Navigate back to your home directory or wherever you installed FiveM to.
  - For me it `cd \home\ubuntu\FXServer\`
  - If you show what is listed in the folder with `ls -a`, you should have a folder called `server`
  - Navigate into this folder
  - You should have a folder called `txData`
  - Navigate into this folder
  - List the contents again
    - You should have a folder named something like `CFXDefault...`, `ESXLEGACY...`, or `QBCoreFramework...` depending on which version you installed
    - Navigate into your appropriate server folder.
    - List the Contents of this folder
    - You should have a `resources` folder in here

The full command to change into this directory should be something like `cd \home\ubuntu\FXServer\server\txData\QBCoreFramework_jfieo38.base\resources\`

# Part 4 (Adding Resources)

- From this repository, there are 2 Folders named `[vehicles]` and `[map_mods]`.
  - Copy both of these folders into your `resources` folder.

- Edit your server config, preferrebly from TXAdmin Web Interface, or you can edit it through ssh
  - Your server config file is located in `\home\ubuntu\FXServer\server\txData\QBCoreFramework_jfieo38.base\` named `server.cfg`

- Add the following to your `server.cfg` file to enable the mods

  ```
  ensure [vehicles]
  ```
  ```
  ensure [map_mods]
  ```

# BONUS

## vMenu

If you have vMenu installed, copy the contents of the `vMenu_addon_conf.json` to your vMenu addon configuration to enable the vehicles to be selected using vMenu
