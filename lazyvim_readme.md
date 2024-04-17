# lazyvim config
Base configuration for linux system

### Install neovim last version
```sh
sudo apt-get install curl
```
```sh
sudo apt-get remove nvim
```
```sh
sudo apt-get remove vim
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
```sh
echo "alias vim=\"nvim\"" | tee -a ~/.zshrc
```
```sh
echo "alias fd=\"nvim\"" | tee -a ~/.zshrc
```
```sh
git clone https://github.com/titor-oopart/takuya-nvim.git
```

```sh
sudo apt-get install alacritty
```

