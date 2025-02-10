# VIRTUALISATION

## Redirection des DNS

Aller sur mon registraire Porkbun, dans le panneau DNS

1) effacer tous les champs existant
2) Créer un champs A qui pointe vers mon ip
3) Créer 3 champs CNAME pour www, wiki et blog qui pointent vers experimentations.buzz.

## VHOST du VPS

Exemple pour le blog

```
cd /etc/apache2/sites-available/
sudo jed blog.experimentations.buzz.conf
(ne pas ecrire la config ici mais upload du fichier)
```
