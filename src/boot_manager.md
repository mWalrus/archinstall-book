# Boot Manager

1. Install packages: `pacman -S grub os-prober efibootmgr`
    - Omit `efibootmgr` if you have a BIOS system
2. Install boot loader: `grub-install --target=x86_64-efi --efi-directory=/boot --bootloader-id=grub`
3. Make boot loader config: `grub-mkconfig -o /boot/grub/grub.cfg`