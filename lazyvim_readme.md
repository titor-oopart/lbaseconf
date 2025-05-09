# lazyvim config
Base configuration for linux system

### Install neovim last version
```sh
sudo apt-get install curl
```
```sh
sudo apt remove nvim
```
```sh
sudo apt remove vim
```
```sh
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.appimage
```
```sh
chmod 755 nvim-linux-x86_64.appimage
```
```sh
./nvim-linux-x86_64.appimage
```
```sh
sudo mv nvim-linux-x86_64.appimage /usr/local/bin/nvim
```
```sh
export PATH="$PATH:/usr/local/bin"
```
Le damos los permisos a /user/local/bin/nvim con chmod 755 para poder ser ejecutado pero no pueda ser escrito por el grupo o el usuario
### Uninstall neovim last version
```sh
sudo rm -R /usr/local/bin/nvim
```
```sh
sudo apt install build-essential
```

```sh
cd ~/.config
```

```sh
mv nvim nvim.back
```

```sh
rm -rf ~/.local/share/nvim
```

```sh
rm -rf ~/.local/state/nvim
```

```sh
rm -rf ~/.cache/nvim
```
```sh
sudo apt install fd-find
```

```sh
sudo apt install ripgrep
```
borrar
```sh
echo "alias vim=\"nvim\"" | tee -a ~/.zshrc
```
```sh
echo "alias fd=\"nvim\"" | tee -a ~/.zshrc
```
borrar

```sh
sudo apt install git
```
```sh
git clone https://github.com/LazyVim/starter ~/.config/nvim
```

```sh
cd ~/.config/nvim
```
```sh
rm -rf .git
```

```sh
nvim
```
```sh
sudo apt install tmux
```
```sh
bash -c  "$(curl -fsSL https://raw.githubusercontent.com/officialrajdeepsingh/nerd-fonts-installer/main/install.sh)"
```
```sh
23
```
### Fish shell
```sh
echo 'deb http://download.opensuse.org/repositories/shells:/fish:/release:/3/Debian_12/ /' | sudo tee /etc/apt/sources.list.d/shells:fish:release:3.list

curl -fsSL https://download.opensuse.org/repositories/shells:fish:release:3/Debian_12/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/shells_fish_release_3.gpg > /dev/null

sudo apt update

sudo apt install fish

chsh -s $(which fish)
```
Bat es cat mejorado
```sh
sudo apt install bat

mkdir -p ~/.local/bin

ln -s /usr/bin/batcat ~/.local/bin/bat
```
Restart your terminal
```sh
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
```
```sh
fisher install simnalamburt/shellder
```
```sh
fisher install IlanCosman/tide@v6

tide configure
```
```sh
fisher install jethrokuan/z
```
```sh
sudo apt install fzf
```
```sh
fisher install PatrickF1/fzf.fish
```
Peco es grep pero dinamico, ejemplo: peco /var/logs/archivo.log   luego filtramos
```sh
sudo apt install peco
```
```sh
sudo apt install exa

alias --save ls='exa --long'
```
```sh
functions --erase ls
```
```sh
ghq Para manejar git pendiente de aprender
```
### Fish instalation finished
```sh
sudo apt-get install kitty
```

```sh
sudo apt install nodejs
```
```sh
sudo apt install npm
```

```sh
sudo npm install --global yarn
```

```sh
git clone https://github.com/titor-oopart/takuya-nvim.git
```
Para solucionar el error lsp ruff failed installed se tiene que crear una venv de python luego entrar a esa venv y entrar a nvim
Configuracion de copilot
Primero :LazyExtras luego :Copilot auth finalmente :Copilot setup, Fuente https://github.com/orgs/community/discussions/46866
