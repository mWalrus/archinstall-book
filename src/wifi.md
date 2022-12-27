# WiFi

__Note__: You can skip this part of the guide if you have a wired connection.

1. Run `iwctl`
2. Find your device: `device list`
3. Scan for networks: `station <DEVICE> scan`
4. List all scanned networks: `station <DEVICE> get-networks`
5. Connect to your network: `station <DEVICE> connect <NETWORK_SSID>`
6. Enter the network passphrase
7. Quit iwctl: `quit`
8. `ping archlinux.org`
    - If everything went well, you should see ping responses indicating you have an internet connection

## Troubleshooting
General troubleshooting information can be found on the [archwiki](https://wiki.archlinux.org/title/Iwd#iwctl)

### Operation failed when trying to connect
Running `journalctl -u iwd` gives you information about what has gone wrong.

#### Recieved Deauthentication event, reason: 2, from_ap: true
If you are encountering this issue you can follow these steps:
1. Create or open the iwd config file: `vim /etc/iwd/main.conf`
2. Add:
    ```
    [General]
    ControlPortOverNL80211=False
    ```
3. Save and quit: `:wq`
4. Restart iwd: `systemctl restart iwd.service`
5. Try connecting again
