# rtl8188eus
This is the updated and error free driver for TP-link wn772n v2/3 wifi adapter.

# Steps to install this driver on your linux machine
1. `sudo apt update`
2. `sudo apt install bc`
3. `sudo rmmod r8188eu.ko`
4. `git clone https://github.com/Munazirul/rtl8188eus`
5. `cd rtl8188eus`
6. `sudo -i`
7. `echo "blacklist r8188eu.ko" > "/etc/modprobe.d/realtek.conf"`
8. `exit`
9. `make`
10. `sudo make install`
11. `sudo modprobe 8188eu`
