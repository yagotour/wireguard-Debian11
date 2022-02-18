# wireguard-Debian11


* En proxmox:

`nano /etc/pve/lxc/[container number].conf`
              
lxc.cgroup.devices.allow: c 10:200 rwm  
lxc.mount.entry: /dev/net dev/net none bind,create=dir

                
`chown 100000:100000 /dev/net/tun`

* En container:

`apt-get update && upgrade`

`wget https://git.io/wireguard -O wireguard-install.sh && bash wireguard-install.sh`
