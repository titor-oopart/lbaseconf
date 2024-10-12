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
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim.appimage
```
```sh
chmod u+x nvim.appimage
```
```sh
./nvim.appimage

```
```sh
sudo mv nvim.appimage /usr/local/bin/nvim

```
```sh
export PATH="$PATH:/usr/local/bin"
```
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
sudo apt-get install kitty
```
```sh
bash -c  "$(curl -fsSL https://raw.githubusercontent.com/officialrajdeepsingh/nerd-fonts-installer/main/install.sh)"
```
```sh
23
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
