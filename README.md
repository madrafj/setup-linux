# setup-linux
ENvironment setup for Linux

source: https://www.digitalocean.com/community/tutorials/how-to-install-php-7-4-and-set-up-a-local-development-environment-on-ubuntu-20-04

## 1. install PHP
```
sudo apt-get update
```
```
sudo apt -y install software-properties-common
```
```
sudo add-apt-repository ppa:ondrej/php
```
```
sudo apt-get update
```
```
sudo apt -y install php7.4
```
```
php -v
```
```
sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath
```

## 2. install Composer
```
sudo apt install curl
```
```
cd ~
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php```
```
```
HASH=`curl -sS https://composer.github.io/installer.sig`
```
```
php -r "if (hash_file('SHA384', '/tmp/composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
```
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer
```
```
composer
```
