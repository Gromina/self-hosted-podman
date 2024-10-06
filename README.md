# Work in progress

Containers work. However this repo is still needs 
- documentation
  - firewall setup
  - privileged ports instructions
- .env files sample
- and more testing

## My folder structure is as following

- $HOME/<repo>  # this repo
- $HOME/volumes # contaners' data and env files

## container units are linked to $HOME/.config/containers:

ln -s ~/<repo>/containers ~/.config/containers/systemd
