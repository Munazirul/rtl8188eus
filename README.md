# rtl8188eus
This is the updated and error free driver for TP-link wn772n v2/3 wifi adapter.
If you still face any trouble installing this driver on your Kali machine, my suggestion is to download Parrot Home from - https://deb.parrot.sh/parrot/iso/5.0.1/Parrot-home-5.0.1_amd64.iso.torrent  or  https://deb.parrot.sh/parrot/iso/5.0.1/ 
There is no need to install any driver on your parrot OS Home edition.
"Do not" update or upgrade your Parrot OS after downloading and installing it on virtualBox (apt update and upgrade)
# Steps to install this driver on your linux machine. Plug in the adapter first.
1. `sudo apt update`
2. `sudo apt install dkms bc`
3. `git clone https://github.com/Munazirul/rtl8188eus`
4. `cd rtl8188eus`
5. `echo "blacklist r8188eu.ko" >> "/etc/modprobe.d/realtek.conf"`
6. `echo "blacklist 8188eu.ko" >> "/etc/modprobe.d/realtek.conf"`
7. `sudo make`
8. `sudo make install`
9. `sudo reboot` (must)
10. `sudo modprobe 8188eu` (Only if the wifi networks are not shown on your machine)

# Original Driver can be found at https://github.com/aircrack-ng/rtl8188eus
