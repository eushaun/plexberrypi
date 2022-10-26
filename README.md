# plexberrypi

My personal docker setup for a nas/seedbox running on a Raspberry Pi 4B 4gb.

The Pi runs raspbian lite os with omv installed + Portainer to monitor docker stack.

Docker compose file contains containers for jackett, flaresolverr, sonarr, radarr, transmission-openvpn and plex. 

Sonarr, radarr and jackett are routed through to a vpn using transmission-openvpn, which is why the port numbers are all setup in the transmission container.

.env file is stored locally. Format for .env file:

```
MOUNT_POINT=/path/to/nas  
VPN_PROVIDER=nordvpn  
VPN_USERNAME=username  
VPN_PASSWORD=password  
VPN_COUNTRY=AU  
```

Credits to https://gitlab.com/mediaguides/media-install-script for the initial docker setup and post install scripts.
