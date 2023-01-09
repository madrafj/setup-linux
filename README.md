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
```
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer
```
```
composer
```

## 3. install NodeJS
source: https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04-id

```
cd ~
curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
```
```
sudo bash nodesource_setup.sh
```
```
sudo apt install nodejs
```
```
node -v
```

## 4. install Code





===================================================================
## BackEnd GRPC
https://grpc.io/docs/languages/go/quickstart/
### GoLang
```
wget -c https://golang.org/dl/go1.16.3.linux-amd64.tar.gz -O - | sudo tar -xz -C /usr/local
```
https://www.letscloud.io/community/how-to-install-golang-on-ubuntu-2004
https://www.digitalocean.com/community/tutorials/how-to-install-go-on-ubuntu-20-04
### Protoc
```
sudo apt install -y protobuf-compiler
```
proto plugins
```
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
```
```
sudo nano ~/.profile
```
```
export PATH="$PATH:$(go env GOPATH)/bin"
```



## Redis
```
curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

sudo apt-get update
sudo apt-get install redis
```
https://redis.io/docs/getting-started/installation/install-redis-on-linux/

## Post-man
https://gist.github.com/prrao87/114933c4638a4f77aa3d4b2c5a3b2477


================================================================================================
## NVM

https://tecadmin.net/how-to-install-nvm-on-ubuntu-20-04/
```
sudo apt install curl
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
```


