# Install-workstation
As I do it often, better have a nice list of task to perform

## Configure basic system

### install ssh

    sudo apt install openssh-server
    
Configure multiple ssh identity in case:

For example to use a specific account on github, create/edit ~/.ssh/config with 

```
# hoa account
Host github.com-hoa
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa_hoa
```


[ssh-copy-id|https://www.ssh.com/ssh/copy-id] is handy

## PHP dev environment

### Setup mysql server


    sudo apt install mysql-server

Finish and secure install if needed/prod.

### Setup php 7.0 environment
    sudo apt-get install php7.0 php7.0-fpm php7.0-cli php7.0-common php7.0-mbstring php7.0-gd php7.0-intl php7.0-xml php7.0-mysql php7.0-mcrypt php7.0-zip

### Setup php 7.1 environment
    sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 4F4EA0AAE5267A6C && \
    LC_ALL=en_US.UTF-8 sudo add-apt-repository -y ppa:ondrej/php && \
    sudo apt-get update && sudo apt-get install -y python-software-properties && \
    sudo apt-get update && sudo apt-get install -y \
    nginx \
    software-properties-common \
    git-core \
    php7.1 \
    php7.1-fpm \
    php7.1-mysql \
    php7.1-imagick \
    php7.1-imap \
    php7.1-mcrypt \
    php7.1-curl \
    php7.1-cli \
    php7.1-gd \
    php7.1-pgsql \
    php7.1-sqlite \
    php7.1-common \
    php-pear \
    curl \
    php7.1-json \
    php7.1-intl \
    php7.1-xml \
    php7.1-mbstring \
    php7.1-zip \
    php-apcu \
    python

##Devops Environment
### Setup docker

Follow standard guide:
https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/#install-using-the-repository

Do post install too
https://docs.docker.com/engine/installation/linux/linux-postinstall/#manage-docker-as-a-non-root-user

