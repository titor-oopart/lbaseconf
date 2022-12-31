# lbaseconf
Base configuration for linux system

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

### Install nala-legacy
```sh
$ echo "deb http://deb.volian.org/volian/ scar main" | sudo tee /etc/apt/sources.list.d/volian-archive-scar-unstable.list
$ wget -qO - https://deb.volian.org/volian/scar.key | sudo tee /etc/apt/trusted.gpg.d/volian-archive-scar-unstable.gpg > /dev/null
$ sudo apt update
$ sudo apt install nala-legacy
```
### Install Nvidia drivers

##### Debian 11 "Bullseye" add the file to /etc/apt/sources.list
```sh
deb http://deb.debian.org/debian/ bullseye main contrib non-free
$ apt update
$ apt install nvidia-legacy-390xx-driver firmware-misc-nonfree
```
