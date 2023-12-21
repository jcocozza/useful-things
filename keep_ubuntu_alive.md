# Edits to keep a headless ubuntu server up when you close the laptop:

1) edit the `logind.conf`: `sudo vim /etc/systemd/logind.conf`
  - change `#HandleLidSwitch=suspend` to `HandleLidSwitch=ignore`
2) restart `logind`: `sudo systemctl restart systemd-logind`
