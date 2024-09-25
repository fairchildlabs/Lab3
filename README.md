# Lab3

## 3.1 Enable the Wired Network interface on your PI

```
$ sudo nano /etc/network/interfaces.d/eth0

** paste these lines

allow-hotplug eth0
iface eth0 inet static
address 11.11.11.1/24
netmask 255.255.255.0
gateway 11.11.11.1

<CTRL><X> then "Y" to save

$ sudo nano reboot

```

## 3.2 Use Ethernet (Network) Cable to attach LABPC to PI

Disable Network Connection on PI (DEMO)
Start Putty normally. (Alternate, use 11.11.11.1 IP address)



