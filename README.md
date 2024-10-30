# Work in progress

Containers work. However this repo is still needs 
- documentation
  - firewall setup
  - privileged ports instructions
- .env files sample
- and more testing

## What is this repo about?
Here are my config of self hosted services using (mostly) rootless podman/Quadlet

Host system is Fedora just becuase it is not Ubuntu and it has recent enough podman version

## My folder structure is as following

- $HOME/\<repo\>  # this repo
- $HOME/volumes # contaners' data and env files

## container units are linked to $HOME/.config/containers:

ln -s ~/\<repo\>/containers ~/.config/containers/systemd

## Current scheme
![scheme](/docs/self_hosted.png?raw=true "Scheme")


## Services TODO
- [Calibre Web](https://github.com/janeczku/calibre-web)
- [RatHole](https://github.com/rapiz1/rathole)
- [SnapCast](https://github.com/badaix/snapcast)
- [Mopidy](https://github.com/badaix/snapcast/blob/develop/doc/player_setup.md#mopidy)
- [JupyterLab](https://jupyter.org/)
- [VaultWarden](https://github.com/dani-garcia/vaultwarden)
- [PenPot](https://penpot.app/)
- [Forgejo](https://codeberg.org/forgejo/forgejo)

| | Service | Comment | Ports | Networks |
|---|---|---|---|---|
| :heavy_check_mark:  | [Home assistant](https://www.home-assistant.io/) |   | 0.0.0.0:8123 |   |
| :heavy_check_mark:  | [Syncthing](https://syncthing.net/)  |  | 0.0.0.0:8384 |   |
| :heavy_check_mark: | [Transmission](https://transmissionbt.com/)  |   | 0.0.0.0:9091 |   |
| :heavy_check_mark:  | [Jellyfin](https://jellyfin.org/) |   | 0.0.0.0:8096 | lldap |
| :heavy_check_mark:  | [Gitea](https://about.gitea.com/)  |   | 0.0.0.0:3000  |   |
| :heavy_check_mark: | [Calibre Web](https://github.com/janeczku/calibre-web)  |   | 0.0.0.0:8083  | lldap  |
| :heavy_check_mark:  | [Z2M](https://www.zigbee2mqtt.io/) |   | 0.0.0.0:8002  |   |
| :heavy_check_mark:  | [Grocy](https://grocy.info/)  |   | 0.0.0.0:9283 ; grocy.h.MYSERVER.com  | lldap  |
| :heavy_check_mark:  | [Lldap](https://github.com/lldap/lldap)  |   | 0.0.0.0:17170  | lldap ; 0.0.0.0:3890  |
| :heavy_check_mark:  | [Caddy](https://caddyserver.com/)  |   | 0.0.0.0:80,443 | lldap ; 0.0.0.0:3890  |
|   |   |   |   |   |
|   |   |   |   |   |
