# Paquetage Linux des dispositions

Ce paquetage contient les dispositions de clavier 

- Dvorak français [BÉPO, version 0.6.5.1](http://www.clavier-dvorak.org/)
- Variante Cœur IO

*Nota Bene:* Le paquetage original de la disposition Dvorak français
BÉPO peut être trouvée
[ici](https://bepo.fr/wiki/XKB_:_installation_manuelle).

## Description

Les fichiers de ce paquetage sont destinés à une utilisation en mode
utilisateur (sans les droit d'administrateur) sur un système possédant
xkbcomp.

Requiert une version de xorg postérieure à la 7.0.

## Utilisation

La commande
  
  xkbcomp -w0 fr-dvorak-bepo.xkb $DISPLAY
  
bascule le clavier en clavier Dvorak français BÉPO. Sur les systèmes
utilisant une version de xorg antérieure à la 7.0, le fichier à utiliser
est « fr-dvorak-bepo-xorglegacy.xkb ».

La commande
  
  xkbcomp -w0 fr-coeur-io.xkb $DISPLAY
  
bascule le clavier en clavier Coeur IO. Le fichier n'est pas disponible
sur ,

Pour disposer des nouvelles touches mortes introduites par ces claviers,
le contenu du fichier XCompose doit être ajouté au fichier ~/.XCompose
de l'utilisateur, par exemple avec la commande :

  cat XCompose >> ~/.XCompose
  
Il est possible de revenir au clavier français par défaut (AZERTY) avec
la commande

  setxkbmap fr

## Licences

Les configurations de clavier de ce paquetage sont distribuées sous la
double licence CC-SA-BY/GFDL. Le texte exact de ces licences peut être
consulté dans les fichiers ../licences/CC-SA-BY.txt et
../licences/GFDL.txt.
