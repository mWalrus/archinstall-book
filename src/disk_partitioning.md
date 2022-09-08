# Disk Partitioning

This part of the guide is divided into two steps:
- UEFI system
- BIOS system

__Note__: For this guide we assume that the disk you're installing on is named `/dev/sda`. 

## Delete partitions
1. List disks: `fdisk -l`
2. Find the disk you want to install Arch Linux onto
3. Use fdisk on disk: `fdisk /dev/sda`
4. Wipe all partitions on disk: `d`
    - Repeat this step for all partitions

## Creating partitions
### UEFI Systems
If you have an UEFI system you need a __ROOT__ and a __BOOT__ partition.

#### BOOT partition
1. Create the EFI/BOOT partition: `n`
2. Partition number: <kbd>Enter</kbd>
3. First sector: <kbd>Enter</kbd>
4. Last sector: `+512M`
5. Change partition type to EFI: `t`
6. Press the number corresponding to EFI
    - list all types with `L`

#### ROOT partition
1. Partition number: <kbd>Enter</kbd>
2. First sector: <kbd>Enter</kbd>
3. Last sector: <kbd>Enter</kbd>
4. Write changes to disk: `w`

#### Make file systems
1. Make __BOOT__ file system: `mkfs.fat -F32 /dev/sda1 && fatlabel /dev/sda1 BOOT`
2. Make __ROOT__ file system: `mkfs.ext4 -L ROOT /dev/sda2`

### BIOS Systems
If you have a BIOS system you only need a __ROOT__ partition.

#### ROOT partition
1. Create the ROOT partition: `n`
2. Partition number: <kbd>Enter</kbd>
3. First sector: <kbd>Enter</kbd>
4. Last sector: <kbd>Enter</kbd>
5. Write changes to disk: `w`


#### Make file system
1. Make __ROOT__ file system: `mkfs.ext4 -L ROOT /dev/sda1`
