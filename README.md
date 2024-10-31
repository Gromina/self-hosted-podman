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
| :heavy_check_mark:  | [Home assistant](https://www.home-assistant.io/) | Smart home system  | 0.0.0.0:8123 |   |
| :heavy_check_mark:  | [Syncthing](https://syncthing.net/)  | File sync over devices p2p | 0.0.0.0:8384 |   |
| :heavy_check_mark: | [Transmission](https://transmissionbt.com/)  | Torrents  | 0.0.0.0:9091 |   |
| :heavy_check_mark:  | [Jellyfin](https://jellyfin.org/) | Media library and player  | 0.0.0.0:8096 | lldap |
| :heavy_check_mark:  | [Gitea](https://about.gitea.com/)  | Git source control  | 0.0.0.0:3000  |   |
| :heavy_check_mark: | [Calibre Web](https://github.com/janeczku/calibre-web)  | Books management  | 0.0.0.0:8083  | lldap  |
| :heavy_check_mark:  | [Z2M](https://www.zigbee2mqtt.io/) | Zigbee to MQTT bridge  | 0.0.0.0:8002  |   |
| :heavy_check_mark:  | [Grocy](https://grocy.info/)  | groceries & household management solution  | 0.0.0.0:9283 ; grocy.h.MYSERVER.com  | lldap  |
| :heavy_check_mark:  | [Lldap](https://github.com/lldap/lldap)  | User management  | 0.0.0.0:17170  | lldap ; 0.0.0.0:3890  |
| :heavy_check_mark:  | [Caddy](https://caddyserver.com/)  | HTTP/HTTPS server proxy  | 0.0.0.0:80,443 |   |
| :heavy_check_mark:  | [Homarr](https://homarr.dev/)  | homepage  | 0.0.0.0:7575 |   |
| :heavy_check_mark:  | [Ollama](https://ollama.com/)  | Ollama + Open-WebUI  | 0.0.0.0:7080 |   |
| :hammer:  | [PenPot](https://penpot.app/)  |   | |  |
| :hammer:  | [VaultWarden](https://github.com/dani-garcia/vaultwarden)  | Self hosted Bitwarden server  | |  |
| :hammer:  | [Forgejo](https://codeberg.org/forgejo/forgejo)  | Gitea fork  | |  |
| :hammer::  | [Mopidy](https://github.com/badaix/snapcast/blob/develop/doc/player_setup.md#mopidy)  | Media streaming  | |  |
| :hammer:  | [SnapCast](https://github.com/badaix/snapcast)  |`TCP/UDP tunelling  | |  |
| :hammer:  | [JupyterLab](https://jupyter.org/)  | Python experiments in browser  | |  |
| :hammer:   | [LeanTime](https://leantime.io/)  | Project management  |   |   |
| :hammer:   | [Wyoming whisper](https://github.com/rhasspy/wyoming-faster-whisper)  | STT for Home assistant  |   |   |
| :hammer:   | [Wyoming piper](https://hub.docker.com/r/rhasspy/wyoming-piper)  | TTS for Home assistant  |   |   |
| :hammer:   | [wyoming openwakeword](https://github.com/rhasspy/wyoming-openwakeword)  | Word activation for Home assistant  |   |   |
|   |   |   |   |   |
