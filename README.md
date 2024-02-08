# lbaseconf
Base configuration for linux system

### Adding sudo permission to main user

```sh
su -
```

```sh
usermod -aG sudo <user name>
```

## Update Repositories and backports (ONLY DEBIAN 11 bullseye)
##### Oficial repositories
```sh
deb http://deb.debian.org/debian/ bullseye main 
deb-src http://deb.debian.org/debian/ bullseye main 

deb http://deb.debian.org/debian-security/ bullseye-security main 
deb-src http://deb.debian.org/debian-security/ bullseye-security main 

deb http://deb.debian.org/debian/ bullseye-updates main 
deb-src http://deb.debian.org/debian/ bullseye-updates main 
```
##### non-free repositories (ONLY DEBIAN 11 bullseye)
```sh
deb http://deb.debian.org/debian/ bullseye-backports main contrib non-free 
deb-src http://deb.debian.org/debian/ bullseye-backports main contrib non-free 

deb http://deb.debian.org/debian/ bullseye main contrib non-free 
deb-src http://deb.debian.org/debian/ bullseye main contrib non-free 

deb http://deb.debian.org/debian-security/ bullseye-security main contrib non-free 
deb-src http://deb.debian.org/debian-security/ bullseye-security main contrib non-free 

deb http://deb.debian.org/debian/ bullseye-updates main contrib non-free 
deb-src http://deb.debian.org/debian/ bullseye-updates main contrib non-free
```
```sh
sudo apt update
```
## Update Repositories and backports (ONLY DEBIAN 12 bookworm)
##### Oficial repositories
```sh
deb http://deb.debian.org/debian bookworm main
deb-src http://deb.debian.org/debian bookworm main

deb http://deb.debian.org/debian-security/ bookworm-security main
deb-src http://deb.debian.org/debian-security/ bookworm-security main

deb http://deb.debian.org/debian bookworm-updates main
deb-src http://deb.debian.org/debian bookworm-updates main
```
##### non-free repositories (ONLY DEBIAN 12 bookworm)
```sh
deb http://deb.debian.org/debian bookworm main non-free-firmware
deb-src http://deb.debian.org/debian bookworm main non-free-firmware

deb http://deb.debian.org/debian-security/ bookworm-security main non-free-firmware
deb-src http://deb.debian.org/debian-security/ bookworm-security main non-free-firmware

deb http://deb.debian.org/debian bookworm-updates main non-free-firmware
deb-src http://deb.debian.org/debian bookworm-updates main non-free-firmware
```
```sh
sudo apt update
```
## Install nala-legacy (ONLY DEBIAN 12 bookworm)
```sh
sudo apt install nala
```

## Install nala-legacy (ONLY DEBIAN 11 bullseye)
```sh
echo "deb http://deb.volian.org/volian/ scar main" | sudo tee /etc/apt/sources.list.d/volian-archive-scar-unstable.list
```
```sh
wget -qO - https://deb.volian.org/volian/scar.key | sudo tee /etc/apt/trusted.gpg.d/volian-archive-scar-unstable.gpg > /dev/null
```
```sh
sudo apt update
```
```sh
sudo apt install nala-legacy
```

## Install kitty
```sh
sudo nala install kitty
```
###### Press crtl+shift+F2
###### Close the windows
###### Go to the path to modify kitty font size 
```sh
.config/kitty/kitty.conf
```
###### Add the line with the font number, e.g. 20.0
```sh
font_size 20.0
```

## Install silversearcher-ag
```sh
sudo nala install silversearcher-ag
```

## Install Brave browser

```sh
sudo nala install curl
```
```sh
sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
```
```sh
echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list
```
```sh
sudo nala update
```
```sh
sudo nala install brave-browser
```

## Install tmux
```sh
sudo nala install tmux -y
```

## Install curl
```sh
sudo nala install curl
```

## Install Nodejs and npm
```sh
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```
```sh
sudo nala update
```
```sh
sudo nala upgrade
```

##### If nodejs and npm is not installed run the following
```sh
sudo nala install nodejs npm -y
```

## Install vim
```sh
sudo nala install vim
```
```sh
ln -s configs/.vimrc ./.vimrc
```
```sh
ln -s configs/.vim ./.vim
```

##### Install vim-plug [vim-plug doc](https://github.com/junegunn/vim-plug)
```sh
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

## Install nvim
```sh
sudo nala install neovim
```
##### Create a folder on ~/.config/ named nvim and inside a file init.vim
##### Problema resuelto en mi laptop al crear el path ./.config/nvim
```sh
mkdir ./.config/nvim
```
```sh
touch init.vim
```
##### In the file init.vim write the following
```sh
set runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath=&runtimepath
source ~/.vimrc
```

## Install zsh
```sh
sudo nala install zsh -y
```
```sh
ln -s configs/.zshrc ./.zshrc
```
## Install git
```sh
sudo nala install git
```
##### Install oh my zsh
```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
##### In .config/nvim/init.vim run the following comand :PlugInstall

##### Copiar tal cual no reemplazar which zsh
```sh
chsh -s $(which zsh)
```
```sh
ln -s configs/.zshrc .zshrc
```
```sh
cd ~/.oh-my-zsh/custom/plugins
```
```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```
```sh
source ~/.zshrc
```
