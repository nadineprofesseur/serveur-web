# Scripts
## Script de sauvegarde
### Script rotatif 7 jours

Voici un script rotatif
```bash
#!/bin/bash

cd /var/www
tar czvf /home/nadine/sauvegarde/cinema.experimentations.xyz.tgz cinema.experim$
cd /home/nadine/sauvegarde

aujourdhui=$(date +%Y-%m-%d)
ilya7jours=$(date --date '- 7 day' +%Y-%m-%d)
#echo $aujourdhui est maintenant
#echo $ilya7jours est il y a 7 jours

mv cinema.experimentations.xyz.tgz cinema.experimentations.xyz.$aujourdhui.tgz

fichier_a_effacer=cinema.experimentations.xyz.$ilya7jours.tgz
echo $fichier_a_effacer

if [ -e $fichier_a_effacer ]; then
   rm $fichier_a_effacer
fi
```
