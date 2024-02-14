# From Command-line
```shell
# Remove useless folders
rm -r ~/Music
rm -r ~/Templates
# Disable apache 2
sudo systemctl disable apache2 && sudo systemctl stop apache2
sudo apt remove apache2
# Install default apps
echo "deb [trusted=yes arch=amd64] https://download.konghq.com/insomnia-ubuntu/ default all" \
    | sudo tee -a /etc/apt/sources.list.d/insomnia.list
sudo add-apt-repository ppa:peek-developers/stable
sudo apt update
sudo apt upgrade -y
sudo apt install -y net-tools
sudo apt install -y python3-launchpadlib
sudo apt install -y snapd
sudo snap install core
sudo snap install snapcraft --classic
sudo apt install -y curl
sudo apt install -y libfuse2
sudo apt install -y gnome-tweaks
sudo apt install -y mariadb-client
sudo apt install -y vim
sudo apt install -y git
sudo apt install -y htop
sudo apt install -y peek
sudo apt install -y insomnia
# Chrome
sudo wget -q -O /tmp/chrome.deb https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i /tmp/chrome.deb
# Node
sudo snap install node --classic
# Golang
sudo wget -q -O /tmp/go.tar.gz https://golang.org/dl/$(curl -s https://go.dev/VERSION?m=text | awk 'NR==1').linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf /tmp/go.tar.gz
export PATH=$PATH:/usr/local/go/bin
# PHP
sudo apt install -y software-properties-common ca-certificates lsb-release apt-transport-https
sudo wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/php.list
sudo apt update
sudo apt install -y php8.3
curl -sS https://getcomposer.org/installer | php && sudo mv composer.phar /usr/local/bin/composer
# Terminator
sudo apt install -y terminator
mkdir -p .config/terminator
wget -q -O .config/terminator/config https://gist.githubusercontent.com/ermos/c3fb706718e47c09781fbb51a62261ce/raw/ba24c0f94b76dd1d19215a535ab5b3e898d42528/config
# Remove useless apps
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

action :
- disable mouse acceleration
