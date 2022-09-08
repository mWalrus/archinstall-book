# Mounting

## UEFI systems
1. Create mount point for BOOT partition: `mkdir /mnt/boot`
2. Mount __ROOT__: `mount /dev/disk/by-label/ROOT /mnt`
3. Mount __BOOT__: `mount /dev/disk/by-label/BOOT /mnt/boot`

## BIOS systems
1. Mount __ROOT__: `mount /dev/disk/by-label/ROOT /mnt`
