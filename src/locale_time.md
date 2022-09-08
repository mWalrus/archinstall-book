# Locale &amp; Time

In this section we setup the system language, clock and time-zone.

1. Set timezone: `timedatectl set-timezone Europe/Stockholm`
    - Replace `Europe/Stockholm` with your time-zone
2. Correct time and sync the system clock: `hwclock --systohc`
3. Set locale: `echo "en_US.UTF-8 UTF-8" && /etc/locale.gen`
4. Generate locale: `locale-gen`