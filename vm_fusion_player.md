# Somethings to remember about VM Fusion Player:

## Port Forwarding:

Using NAT connection you can specific port forwards in the nat.conf file:
For example when running wireguard(on a VM, not the host) you'll want to ensure that all UDP traffic from port 51820 is forwarded to the VM
```
[incomingudp]
<external port number(port on host machine)> = <VM's IP address>:<VM's port number>
51820 = 172.16.254.132:51820
```

Finding the file can be tricky....try:
`/Library/Preferences/VMware FUsion/vmnet8`
(vmnet8 is the interface corresponding to NAT connection)


When modifying the network like this, the easiest way to check your changes quickly is by restarting the vmnet-cli, this way you don't have to quite VM Fusion Player:
`sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --stop` 
`sudo /Applications/VMware\ Fusion.app/Contents/Library/vmnet-cli --start`
