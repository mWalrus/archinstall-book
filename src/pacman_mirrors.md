# Pacman Mirrors

When installing the base packages needed for an installation you want the fastest download mirrors.
To obtain these you can use `reflector`, a simple tool to update your mirrorlist.

1. Update current mirrors: `pacman -Syy`
2. Install reflector: `pacman -S reflector`
3. Generate new mirrorlist (replace "XX" with your country code): `reflector --protocol https -c "XX" -f 12 -l 10 -n 12 --save /etc/pacman.d/mirrorlist`