# lazyvim config
Base configuration for linux system

### Install neovim last version
```sh
sudo apt-get install curl
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

