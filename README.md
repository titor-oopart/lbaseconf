# lbaseconf
Base configuration for linux system

### Adding sudo permission to main user

```sh
su -
```

```sh
usermod -aG sudo <user name>
```

### Update Repositories and backports

##### Oficial repositories
```sh
deb http://deb.debian.org/debian/ bullseye main 
deb-src http://deb.debian.org/debian/ bullseye main 

deb http://deb.debian.org/debian-security/ bullseye-security main 
deb-src http://deb.debian.org/debian-security/ bullseye-security main 

deb http://deb.debian.org/debian/ bullseye-updates main 
deb-src http://deb.debian.org/debian/ bullseye-updates main 
```
##### non-free repositories
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
### Install nala-legacy
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
### Install kitty
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

### Install silversearcher-ag
```sh
sudo nala install silversearcher-ag
```

### Install Nvidia drivers

##### Debian 11 "Bullseye" add the file to /etc/apt/sources.list
```sh
deb http://deb.debian.org/debian/ bullseye main contrib non-free
```
```sh
sudo nala update
```
```sh
sudo nala install nvidia-driver firmware-misc-nonfree
```

### Install Brave browser

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
