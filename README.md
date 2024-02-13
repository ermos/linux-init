# Core
```shell
rm -r ~/Music
rm -r ~/Templates
echo "deb [trusted=yes arch=amd64] https://download.konghq.com/insomnia-ubuntu/ default all" \
    | sudo tee -a /etc/apt/sources.list.d/insomnia.list
sudo add-apt-repository ppa:peek-developers/stable
sudo apt update
sudo apt upgrade -y
sudo apt install -y net-tools
sudo apt install -y snapd
sudo snap install core
sudo snap install snapcraft --classic
sudo apt install -y curl
sudo apt install -y libfuse2
sudo apt install -y gnome-tweaks
sudo apt install -y mariadb-client
sudo apt install -y vim
sudo apt install -y git
sudo apt install -y terminator
sudo apt install -y htop
sudo apt install -y peek
sudo apt install -y insomnia
wget -q -O /tmp/chrome.deb https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i /tmp/chrome.deb
sudo apt purge -y libreoffice-*
sudo apt purge -y firefox-esr*
sudo apt purge -y transmission-*
sudo apt purge -y cheese
sudo apt purge -y rhythmbox
sudo apt purge -y gnome-terminal
sudo apt purge -y gnome-contacts
sudo apt purge -y gnome-games
sudo apt purge -y gnome-maps
sudo apt purge -y gnome-software
sudo apt purge -y gnome-music
sudo apt purge -y gnome-weather
sudo apt purge -y gnome-sound-recorder
sudo apt purge -y evolution
sudo apt purge -y shotwell
sudo apt -y autoremove
sudo apt autoclean
```

## From web

### Docker
- https://docs.docker.com/engine/install/debian/

### Jetbrains Toolbox
- https://www.jetbrains.com/fr-fr/toolbox-app/
- ``sudo tar -xzf jetbrains-toolbox-1.17.7391.tar.gz -C /opt``


# disable apache for docker or kubernetes reverse proxy
```shell
sudo systemctl disable apache2 && sudo systemctl stop apache2
sudo apt remove apache2
```

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
