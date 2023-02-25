# Core
```shell
sudo apt install net-tools
sudo apt install curl
sudo apt install libfuse2
sudo apt install gnome-tweaks
sudo apt install mariadb-client
sudo apt install vim
sudo apt install git
```

# Apps

## From apt

```shell
echo "deb [trusted=yes arch=amd64] https://download.konghq.com/insomnia-ubuntu/ default all" \
    | sudo tee -a /etc/apt/sources.list.d/insomnia.list
sudo add-apt-repository ppa:peek-developers/stable
sudo apt-get update
sudo apt install terminator
sudo apt install htop
sudo apt install peek
sudo apt install insomnia
```

## From web

### Chrome
- https://www.google.com/intl/fr_fr/chrome/

### Docker
- https://docs.docker.com/engine/install/debian/

### Jetbrains Toolbox
- https://www.jetbrains.com/fr-fr/toolbox-app/

# disable apache for docker or kubernetes reverse proxy
sudo systemctl disable apache2 && sudo systemctl stop apache2
sudo apt remove apache2

action :
- disable mouse acceleration



terminator config :
~/.config/terminator/config
```
[global_config]
  tab_position = hidden
[keybindings]
  split_horiz = <Primary>f
  split_vert = <Primary>d
  close_term = <Primary>q
  copy = <Primary>c
  paste = <Primary>v
  toggle_zoom = <Primary><Shift>Return
[profiles]
  [[default]]
[layouts]
  [[default]]
    [[[window0]]]
      type = Window
      parent = ""
    [[[child1]]]
      type = Terminal
      parent = window0
[plugins]
```
