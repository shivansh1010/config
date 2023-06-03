# Checklist
### Basics
- install popOS with boot(1GB), swap(8GB) and root partitions (Test keyboard layout during install)
- update packages and os
- change dock and touchpad settings (turn on natural scrolling for touchpad)
- resolve time issue in dual boot `timedatectl set-local-rtc 1`
- install `python` and/or `python-is-python3` and pip `apt install python3-pip`
### Bootloader
- copy the entire `Microsoft` folder from `{windows-efi-partition-name}/EFI/` to `/boot/efi/EFI/`
- add a newline `timeout 4` to the end of `/boot/efi/loader/loader.conf`
- reboot to bios menu and give higest priority to PopOS
- reboot (bootselector should work fine)
### Terminal (optional)
- install zsh and make it the default shell
- logout and login
- install ohmyzsh and apply agnoster theme (by changing `~/.zshrc`)
- install jetbrains mono and change font for the terminal

### Customizations (optional) 
- install gnome tweak tool
- install papirus icon pack
- install "hide top bar" extension
- enable hot corner for workspaces and `hide top bar` extension

### Firefox
- login firefox
- login gmail, github, ldap

### Software
- Install Sublime Text
- Install VS Code
