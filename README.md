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

- $HOME/<repo>  # this repo
- $HOME/volumes # contaners' data and env files

## container units are linked to $HOME/.config/containers:

ln -s ~/<repo>/containers ~/.config/containers/systemd
