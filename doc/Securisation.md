# Sécurisation du serveur web

## Activation de HTTPS pour les 3 sites


## Installation des CMS

### Installation de Flatpress sur blog.mon-site.com


### Installation de Dokuwiki sur wiki.mon-site.com


## Préparation du site badge

### Préparation du fichier html avec favicon

```
cd /var/www/nadine.scintillant.world/
touch index.html
mv /home/nadine/machin.png ./favicon.png
jed index.html
```
- inclure le link <link> vers le favicon
- inclure un lien <a> vers le fichier gpg.txt
Voir le fichier index.html dans le backup des sites

### Génération de ma clé GPG

```
$ gpg --full-generate-key
$ gpg --list-secret-keys --keyid-format=long
/Users/hubot/.gnupg/secring.gpg
------------------------------------
sec   4096R/3AA5C34371567BD2 2016-03-10 [expires: 2017-03-10]
uid   Hubot <hubot@example.com>
ssb   4096R/4BB6D45482678BE3 2016-03-10
$ gpg --armor --export 3AA5C34371567BD2
-----BEGIN PGP PUBLIC KEY BLOCK-----
mQGNBGPurcwBDADy5JpCywRga4FrDIxk5ICillkKYtEoxL3uyoaBlh9zLiu1YWnG
TUil/EEKD1K8SoWa+ggBp/OWvWnWr/EPj82+g2FmMud/DmRUksUEUszAwfE6mfIp
$ gpg --armor --export 3AA5C34371567BD2 > gpg.txt
cp gpg.txt /var/www/nadine.scintillant.world/gpg.txt
```

## Préparation des webmestres
