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
___

# BASE DE DONNÉES

```
sudo apt install mysql-server
sudo mysql -u root

> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'unmotdepassecomplique'; 
> flush privileges; 
> exit;

sudo mysql_secure_installation 
> N N Y Y Y Y

sudo mysql -u root -o
> CREATE USER 'superadmin'@'localhost' IDENTIFIED WITH mysql_native_password by 'testtest'; 
> GRANT ALL PRIVILEGES ON *.* TO 'superadmin'@'localhost';
> GRANT GRANT OPTION on *.* to 'superadmin'@'localhost';
> flush privileges;

```


