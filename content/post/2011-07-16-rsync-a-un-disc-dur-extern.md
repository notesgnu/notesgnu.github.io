---
title: "Rsync a un disc dur extern"
date: "2011-07-16"
categories: 
  - "comandes"
  - "rsync"
  - "terminal"
---

![http://mindprod.com/image/iconcorp/rsync.png](images/rsync.png)

[rsync](http://es.wikipedia.org/wiki/Rsync) és una eina que ens permet fer còpies de seguretat entre difrents màquines, discs, i té molta versalitat. Si ens costa la línia de comandes, llavors la podem usar en entorn gràfic a través de [Grsync](http://www.opbyte.it/grsync/).

rsync \[OPCIONS\]... origen ... destí

Un exemple de la comanda:

rsync -r -t -v --progress -s /home/usuari/lacarpeta/ /media/discdur/

Amb això farà una còpia de seguretat.

Per fer-ho via _SAMBA_ amb ssh:

1. primer cal muntar el disc amb samba

mount -t cifs //ip/carpetadeldiscdur /mnt/carpetadestímuntada

1. sincronitzem

rsync -rtv --progress -e -ssh /origen/ /mnt/carpetadestímuntada

1. desmontem el disc

umount /mnt/carpetadestímuntada

**Un truc senzill** és aprofitar quan muntem un disc, podem usar la carpeta on es munta per defecte **.gvfs**:

rsync -r -t -v --progress -s /origen/ /home/usuari/.gvfs/carpetadeldiscextern/

;-)

Per saber-ne més de l'ús de [grsync](http://www.neoteo.com/grsync-backups-faciles-en-linux). Per saber-ne més de [rsync](http://rsync.samba.org/) y [manual rsync](http://www.samba.org/ftp/rsync/rsync.html).
