---
title: Tech:Proxmox
---

`{{ {{Outdated}} }}`

## Cloud 

1. Install by changing Type Of OS to "Basic".

2. Select 'Debian 12 "Bookworm" - debian12 (Linux)' from the list and proceed to install, make sure to select your ssh key.

3. When you get to the end, enter the server name and select your ssh key from the dropdown.

4. After the server has come back up, login by doing `ssh debian@cloud[num].wikitide.net -i <key>`.

5. Edit `/etc/hosts` and remove `127.0.1.1` section, then add `<main_ip> cloud[num].wikitide.net cloud[num]`.

6. Edit `/etc/cloud/cloud.cfg`, changing `manage_etc_hosts` to false.

7. Run `echo "deb http://download.proxmox.com/debian/pve bookworm pve-no-subscription" > /etc/apt/sources.list.d/pve-install-repo.list`.

8. Run `wget http://download.proxmox.com/debian/proxmox-ve-release-6.x.gpg -O /etc/apt/trusted.gpg.d/proxmox-ve-release-6.x.gpg`.

9. Run the following `apt update && apt full-upgrade`.

10. Run the following `apt install proxmox-ve postfix open-iscsi`.

11. Empty `/etc/network/interfaces.d/50-cloud-init.cfg` and enter the following:

```
# This file is generated from information provided by
# the datasource.  Changes to it will not persist across an instance.
# To disable cloud-init's network configuration capabilities, write a file
# /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg with the following:
# network: {config: disabled}
auto lo
iface lo inet loopback
    dns-nameservers 213.186.33.99

auto eth0
iface eth0 inet dhcp
    mtu 1500
```

12. Run `echo "network: {config: disabled}" > /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg`.

13. Empty `/etc/network/interfaces` and insert the following:

```
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

# The loopback network interface
auto lo
iface lo inet loopback

iface eno1 inet manual

# IPV4 main host addresse, replace address, broadcast, and gateway with the correct IP.
auto vmbr0
iface vmbr0 inet static
    address <main ip>
    netmask  255.255.255.0
    broadcast <main ip (ends in .255)>
    gateway <main ip gateway>
    bridge-ports eno1
    bridge-stp off
    bridge-fd 0

# IPV6 addresses, replace address, gateway with correct IP
iface vmbr0 inet6 static 
    address <ip6 main ip>
    netmask 128
    gateway <ip6 main ip gateway>
    post-up /sbin/ip -f inet6 route add <ip6 main ip gateway> dev vmbr0
    post-up /sbin/ip -f inet6 route add default via <ip6 main ip gateway>
    pre-down /sbin/ip -f inet6 route del <ip6 main ip gateway> dev vmbr0
    pre-down /sbin/ip -f inet6 route del default via <ip6 main ip gateway>

# Set this one last, so that cloud-init or user can
# override defaults.
source /etc/network/interfaces.d/*
```

14. Reboot the server.

15. Run `passwd root` and set the password, make sure it is secure.

16. Run the following "cd /var/lib/vz/template/iso ; wget [https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-12.4.0-amd64-netinst.iso](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-12.4.0-amd64-netinst.iso)" (note that this may be removed, in which case bump version like 12.4.0 -> 12.5.0).

17. On the main cluster host, press join information and copy the information (`ssh -L 8006:127.0.0.1:8006 <user>@<main_cluster_cloud_host_>.wikitide.net`).

18. Go to [https://localhost:8006](https://localhost:8006).

19. Enter login details, click on "Datacenter" then "Cluster".

20. Click on "Join Cluster".

21. Where it says "Join information" copy what’s in the text box.

22. Now go onto the other cloud virt (for instance, cloud16) (`ssh -L 8006:127.0.0.1:8006 <user>@<cloud_host_>.wikitide.net`).

23. Go to [https://localhost:8006](https://localhost:8006).

24. Click "Join Cluster".

25. Paste into the "Join information" text box (the details you copied from cloud15).

26. Run `sudo ufw default allow FORWARD` required for VPS.

## VPS 

* In the OVH UI: assign a failover IPv4 address and IPv6 address for the new VM. Ensure the MAC address of the network adapter of the new VM matches the vMAC address assigned for the failover IPv4 address in OVH.
* Run the following `ssh -L 8006:127.0.0.1:8006 <user>@<cloud_host>.wikitide.net`.
* Go to [https://localhost:8006](https://localhost:8006) (and accept the invalid certificate as the connection will be secure due to SSH) and login using your account and password.
* Create a VM using the UI:
   * ISO image: local, debian-XX-X.X-amd64-DVD-1.iso
   * Type: Linux, 5.x - 2.6 Kernel
   * SCSI Controller: VirtIO SCSI single
   * Hard Disk: raw disk image, write back (unsafe) cache, SSD emulation and IO thread **on** (advanced)
   * Ballooning: on
   * Network: vmbr0, MAC address equal to vMAC for failover IP (or vmbr1 if internal only)
* Once VM is setup, click start and go through the installation, when you get onto the network step enter the following:
   * IP address: the failover IP (or the allocated internal IP)
   * Netmask = 255.255.255.255 (or /32)
   * Default gateway: leave empty!  [Do not enter the gateway here yet, Debian won't understand it.](http://forums.debian.net/viewtopic.php?f=17&t=143186#p705619)
   * Example: on cloud15 (main IP 51.77.117.189), you want to give a VM the failover IP 51.195.236.255. Since this VM is on cloud15, the default gateway will be 51.77.117. **254**
* After install: empty `/etc/network/interfaces`, insert the following in it (don’t forget to change the IPv4/IPv6 addresses) and reload the network configuration (`ifdown ens18` && `ifup ens18`).
* In `/etc/resolv.conf`:
```
search wikitide.net
nameserver 8.8.8.8
```
* In `/etc/apt/sources.list`:
```
deb http://ftp.uk.debian.org/debian/ bookworm main
deb-src http://ftp.uk.debian.org/debian/ bookworm main
deb http://security.debian.org/debian-security bookworm/updates main
deb-src http://security.debian.org/debian-security bookworm/updates main
deb http://ftp.uk.debian.org/debian/ bookworm-updates main
deb-src http://ftp.uk.debian.org/debian/ bookworm-updates main
```
* [Run puppet](/tech-docs/techpuppet#adding-a-new-puppet-agent-28server29-to-the-puppetserver). Do not log out before your user account is set up by puppet; otherwise you'll have a hard time getting back in.
```
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).
source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback

allow-hotplug ens18
auto ens18
iface ens18 inet static
	address <failover IPv4>
	gateway <IPv4 gateway>
        netmask 255.255.255.255

iface ens18 inet6 static
        address <IPv6 address>/64
        gateway <IPv6 gateway>
```
Default gateway IPv4: first three octets of the cloud's main IP address + '.254'. Example: on cloud15 (main IP 51.77.117.189), you want to give a VM the failover IP 51.195.236.255. Since this VM is on cloud15, the default gateway will be 51.77.117. **254**

Instructions for getting the right IPv6 addresses:
* Each cloud server has a /64 assigned by OVH. For example, for cloud15 this is `2001:41d0:0800:1bbd::/64`.
* In the OVH UI, you have assigned an IPv6 address for the new server, for example: `2001:41d0:800:1bbd::2`.
* The last address in the /64 is the IPv6 gateway. In the example IP from 2), this would be `2001:41d0:800:1bFF:FF:FF:FF:FF`.
If you want to add an internal IP in addition to public interfaces, you need to append the following to the above network/interfaces config file:
```
allow-hotplug ens19
auto ens19
iface ens19 inet static
        address <private IP>
        netmask 255.0.0.0
```

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Proxmox](https://meta.miraheze.org/wiki/Tech:Proxmox)