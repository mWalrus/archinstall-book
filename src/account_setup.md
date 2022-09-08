# Account Setup

This section takes care of these things:
- Creating a new root password
- Creating a new user with the following things:
  - A home directory
  - Membership in the "wheel" group
  - A new password
- Permit the "wheel" group to use sudo

## Steps

1. Set root password: `passwd`
2. Create user: `useradd -G wheel -m <user-name>`
3. Set new user password: `passwd <user-name>`
4. Grant wheel group sudo access: `echo "%wheel ALL=(ALL) ALL" >> /etc/sudoers`