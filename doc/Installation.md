# INSTALLATION du SERVICE

sudo apt update

## INSTALLATION du SERVEUR WEB

Pour installer le serveur web et php

```
sudo apt install apache2
cd /var/wwww
sudo chown nadine:www-data -R *
```

## INSTALLATION et CONFIG de PHP

```
sudo apt install php
sudo apt install libapache2-mod-php
```

```
cd /etc/php/8.1/apache2
sudo jed.ini
> display_errors = On
> display_startup_errors = On
> opcache.enable = 0
> mysqlnd.debug = /var/log/php-mysql
sudo service apache2 restart
```

___

# BASE DE DONNÉES

## INSTALLATION de BASE DE DONNEES

```
sudo apt install mysql-server
sudo mysql -u root

> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'unmotdepassecomplique'; 
> flush privileges; 
> exit;

sudo mysql_secure_installation 
(SI erreur au premier N, rebuild de toute la machine)
> N N Y Y Y Y

sudo mysql -u root -o
> CREATE USER 'superadmin'@'localhost' IDENTIFIED WITH mysql_native_password by 'testtest'; 
> GRANT ALL PRIVILEGES ON *.* TO 'superadmin'@'localhost';
> GRANT GRANT OPTION on *.* to 'superadmin'@'localhost';
> flush privileges;
```

## CONFIGURATION de BASE DE DONNEES

```
sudo apt install php-myadmin
sudo /etc/php/8.1/apache2
sudo jed php.ini
  effacer le ; devant 
  extension=mysqli
  extension=pdo_mysql
sudo service apache2 restart
```

## PHPMYADMIN

ECRAN à la full largeur
```
sudo apt install phpmyadmin
> Cocher Apache avec la barre espace (tab pour aller a ok)
> YES
> garder le mot de passe vide
```



