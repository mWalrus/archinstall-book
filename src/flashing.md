# Flashing

This section is intended for Linux, if you're on Windows
you download Etcher from their website listed in the previous section.

This section also assumes you have `paru`, the [AUR](https://aur.archlinux.org/) helper installed, but any other helper should work the same way.

## Steps

1. Insert the USB into the PC.
2. Install etcher: `paru -S etcher-bin`
3. Run as root: `sudo etcher`
    - If you're on Windows, run it as administrator.
4. Flash the ISO file onto the USB stick following the instructions in Etcher.

__Reboot__ after the image has been flashed onto the USB and head into your UEFI setup.
This can usually be done by pressing the <kbd>Del</kbd> key on boot although this might vary.
