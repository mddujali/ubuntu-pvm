# Setup PHP Version Manager (PVM) in Ubuntu Desktop 16.04 or Higher

### Get PHP information
```console
$ sudo apt show php
```
Or
```console
$ sudo apt show php -a
```

### Ensure you are using the latest Ubuntu updates by entering the following command into a terminal window:
```console
$ sudo apt update && sudo apt upgrade
```

### Install software-properties-common to help you manage distributions and independent software sources:
```console
$ sudo apt install software-properties-common
```

### Next, add the ondrej/php PPA which provides all the latest releases of PHP
```console
$ sudo add-apt-repository ppa:ondrej/php
```

### Update the repository to include the new packages:
```console
$ sudo apt update
```

### To install default PHP version
```console
$ sudo apt install php
```

### To install different PHP version

#### For Apache 2
```console
$ sudo apt install php7.4  [PHP 7.4]
$ sudo apt install php8.0  [PHP 8.0]
```

#### For Nginx
```console
$ sudo apt install php7.4-fpm   [PHP 7.4]
$ sudo apt install php8.0-fpm   [PHP 8.0]
```

### To install extensions/modules
```console
$ sudo apt install php7.4-cli ...
$ sudo apt install php8.0-cli ...
```

### Set default PHP version i.e. from 7.4 to 8.0)

#### For Apache 2
```console
$ sudo update-alternatives --set php /usr/bin/php8.0
$ sudo a2dismod php7.4
$ sudo a2enmod php8.0
$ sudo service apache2 restart
```

#### For Nginx
```console
$ sudo update-alternatives --set php /usr/bin/php8.0
$ sudo service php*-fpm restart
```