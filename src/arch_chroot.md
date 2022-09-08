# Arch Chroot

1. Packstrap base packages into mount point: `pacstrap /mnt base base-devel linux linux-firmware linux-headers neovim nano networkmanager dhcpcd`
2. Generate FS Tab: `genfstab -U /mnt >> /mnt/etc/fstab`
3. Enter mount point: `arch-chroot /mnt`