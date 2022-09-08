# Network Configuration

Here we will set a hostname and configure `/etc/hosts`.

__Note__: replace all instances of `arch` with your preferred hostname in the steps below.

1. Set hostname: `echo arch > /etc/hostname`
2. Open and edit `/etc/hosts` using either `nvim` or `nano`:
```
  127.0.0.1  localhost
  ::1        localhost
  127.0.1.1  arch.localdomain arch
```
3. Enable NetworkManager: `systemctl enable NetworkManager.service`