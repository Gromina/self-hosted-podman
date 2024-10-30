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
| :heavy_check_mark:  | [Caddy](https://caddyserver.com/)  |   | 0.0.0.0:80,443 |   |
| :heavy_check_mark:  | [Homarr](https://homarr.dev/)  |   | 0.0.0.0:7575 |   |
| :heavy_check_mark:  | [Ollama](https://ollama.com/)  | Ollama + Open-WebUI  | 0.0.0.0:7080 |   |
| :hammer:  | [PenPot](https://penpot.app/)  |   | |  |
| :hammer:  | [VaultWarden](https://github.com/dani-garcia/vaultwarden)  |   | |  |
| :hammer:  | [Forgejo](https://codeberg.org/forgejo/forgejo)  |   | |  |
| :hammer::  | [Mopidy](https://github.com/badaix/snapcast/blob/develop/doc/player_setup.md#mopidy)  |   | |  |
| :hammer:  | [SnapCast](https://github.com/badaix/snapcast)  |   | |  |
| :hammer:  | [RatHole](https://github.com/rapiz1/rathole)  |   | |  |
| :hammer:  | [JupyterLab](https://jupyter.org/)  |   | |  |
|   |   |   |   |   |
|   |   |   |   |   |
