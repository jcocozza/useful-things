# WireGuard

## Useful commands:
- `sudo wg-quick down <wireguard-interface(e.g.wg0)>` stop server
- `sudo wg-quick up <wireguard-interface(e.g.wg0)>` start server
- `sudo wg showconf <wireguard-interface>` show config info about the server
- `sudo wg show <wireguard-interface>` show info about the server, things like peer endpoints, listening ports, ltest handshake etc.
- `journalctl -u wg-quick@<wireguard-interface>` get log like info about the server
## Interfaces
Create an interface as `/etc/wireguard/<interface-name>.conf` e.g. `/etc/wireguard/wg0.conf`

## Adding Clients:

- `qrencode --read-from=<path/to/client.conf> --type=UTF8` Generate a qr code for a client config file
- `sudo wg show wg0 public-key` show public key of server
- 
