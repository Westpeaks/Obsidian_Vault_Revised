## WiFi Fix Steps:

1. **Install required packages:**
```bash
sudo pacman -S linux-firmware iw iwd
```

2. **Download the BCM43602 configuration file:**
```bash
cd /tmp
wget https://gist.githubusercontent.com/MikeRatcliffe/9614c16a8ea09731a9d5e91685bd8c80/raw/38180b6a0ce552e1a3a2826ffea2bf1f52d05e9f/brcmfmac43602-pcie.txt
```

3. **Edit the file to add your MAC address:**
```bash
nano brcmfmac43602-pcie.txt
```

Find the line `macaddr=xx:xx:xx:xx:xx:xx` and replace with your actual MAC address (get it with `ip link show wlan0`)

4. **Copy the configuration file to firmware directory:**
```bash
sudo cp brcmfmac43602-pcie.txt /lib/firmware/brcm/
```

5. **Reload the brcmfmac driver:**
```bash
sudo modprobe -r brcmfmac
sudo modprobe brcmfmac
```

6. **Configure iwd:**
````bash
sudo nano /etc/iwd/main.conf
```
Add:
```
[General]
EnableNetworkConfiguration=true

[Network]
NameResolvingService=systemd
````

7. **Enable required services:**
```bash
sudo systemctl enable iwd
sudo systemctl enable systemd-networkd
sudo systemctl enable systemd-resolved
sudo systemctl start iwd
sudo systemctl start systemd-networkd
sudo systemctl start systemd-resolved
```

8. **Create DNS resolver symlink:**
```bash
sudo ln -sf /run/systemd/resolve/stub-resolv.conf /etc/resolv.conf
```

9. **Connect to WiFi:**
```bash
iwctl 

station wlan0 connect ThePeaks
```

**Key points:**

- Driver: `brcmfmac` (built into kernel)
- WiFi manager: `iwd` (not NetworkManager, not wpa_supplicant)
- Critical file: `/lib/firmware/brcm/brcmfmac43602-pcie.txt` with your actual MAC address
- The .txt file contains calibration data specific to BCM43602

## Links:

20260204