# wireguard-Debian11

* Da igual unprivileged container, marcado funciona.

* En proxmox:

`nano /etc/pve/lxc/[container number].conf`
              
lxc.cgroup.devices.allow: c 10:200 rwm  
lxc.mount.entry: /dev/net dev/net none bind,create=dir

                
`chown 100000:100000 /dev/net/tun`

* En container:
 
`apt-get update && upgrade` 
  
(Con Root):  
  
`wget https://git.io/wireguard -O wireguard-install.sh && bash wireguard-install.sh`  
(Con Sudo):  
  
`sudo wget https://git.io/wireguard -O wireguard-install.sh && sudo bash wireguard-install.sh`
