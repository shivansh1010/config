# Fresh Dual Boot (Take backup)
### Prepare for larger efi partition
- create a bootable usb with ubuntu and windows both
- boot to ubuntu
- open `disks` in ubuntu and remove all partitions
- create a data partition of `968884224 Bytes` (924 MB)
- leave rest of the disk unallocated

### Install windows
- boot to windows and use custom setup
- click on unallocated and then new button
- give C: drive a size of `256649 MB` (~250GB)
- continue with setup

### enlarge efi
- after windwos installation, download [partition wizard free](https://www.partitionwizard.com/)
- delete the partition initially created that had size of 924MB
- resize efi partition to takeup all the space, around 1024MB
- apply changes

### install linux
- change boot priority to bootable USB
- boot to ubuntu live usb and verify correct setup of partitions
- install ubuntu with 12GB swap and 150GB root
- continue with setup
- verify that no new efi partition should be created
- change grub settings as you like

### enjoy
