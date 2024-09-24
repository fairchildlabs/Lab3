# Lab3

$ sudo nano /etc/network/interfaces.d/eth0

** paste these lines

allow-hotplug eth0
iface eth0 inet static
address 11.11.11.1/24
netmask 255.255.255.0
gateway 11.11.11.1

<CTRL><X> then "Y" to save

