# Fresh Dual Boot (Take backup)
- create a bootable usb with ubuntu and windows both (ventoy recommended)

### Prepare for larger efi partition (optional)
- boot to ubuntu
- open `disks` in ubuntu and remove all partitions
- create a data partition of `968884224 Bytes` (924 MB)
- leave rest of the disk unallocated

### Install windows
- boot to windows and use custom setup
- click on unallocated and then new button
- give C: drive a size of `256649 MB` (~250GB)
- continue with setup

### enlarge efi (optional)
- after windwos installation, download [partition wizard free](https://www.partitionwizard.com/)
- delete the partition initially created that had size of 924MB
- resize efi partition to takeup all the space, around 1024MB
- apply changes

### install linux
- change boot priority to bootable USB
- boot to ubuntu live usb and modify partitions as needed
- install ubuntu with 12GB swap, 70GB root, and 100GB home
- continue with setup
- change grub settings as you like

___

### Basics
- update packages and os
- **change dock and touchpad settings (turn on natural scrolling for touchpad)**
- resolve timezone issue in dual boot, run this in linux`timedatectl set-local-rtc 1`
- install `python3` and/or `python-is-python3` and pip `apt install python3-pip`

### Terminal (optional)
- install zsh and make it the default shell
- logout and login
- install ohmyzsh and apply agnoster theme (by changing `~/.zshrc`)
- **install `zsh-autosuggestions` and `zsh-syntax-highlighting`**
- install powerline fonts for shell
- install jetbrains mono and change font for the terminal

### Customizations (optional)
- install gnome tweak tool
- **install papirus icon pack**
- install "hide top bar" extension
- **enable hot corner for workspaces** and `hide top bar` extension

  
```bash
sudo apt update
sudo apt install zsh curl git python3 python-is-python3 python3-pip terminator gnome-tweaks dconf-editor
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
timedatectl set-local-rtc 1
sudo apt upgrade

# ============ INTERACTIVE COMMANDS ============
chsh -s $(which zsh)
sudo update-alternatives --config x-terminal-emulator

```
