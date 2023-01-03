---
title: "Solucionar discs amb FSCK"
date: "2013-04-27"
categories: 
  - "terminal"
---

Moltes vegades m'he trobat amb discs externs que no s'obren o que de sobte l'ordinador es queixa que s'ha de fer manualment el xequeig. Sovint passa per extreure-les sense desmuntar, o per altres causes, apagat iniesperat de la màquina,… Així que podem perdre la infromació del disc o no podem accedir-hi. L'eina a usar és **fsck** (file system consistency check) que serveix per solucionar les inconsistències del sistema d'arxius i si en troba pot corregir-les. Per poder executar-lo cal fer-ho de manera com a superusuari (sudo / su).

### Ús:

Per poder dur-ho a terme, el primer és llistar les particions i discs, es pot fer de moltes maneres, la que faig anar és:

$ cat /proc/partitions

Un cop veiem la llista, ara cal desmontar-ho:

$ umount /dev/sdXX

I ara com superusuari iniciem **fsck**:

$ sudo fsck -a /dev/sdXX

### Forçar comprovació en reinici:

Una altra possibilitat és que volem forçar un xequeig automàtic en el proper reinici:

sudo touch /forcefsck
sudo reboot

### Notes:

Aquesta comanda **fsck** se pot fer anar en qualsevol sistema de fitxers, tot i que ha d'estar instal·lades les dependències necessàries.  Per defecte és per a sistemes de fitxers de tipus **ext**, si volem altres tipus **FAT** podem usar la comanda **DOSFSCK**! Altres opcions que permet són:

\-a fa la feina automàticament, no tindrem tot el control de l'eina.

\-r al contrari de el mode automàtic, ens demanarà la confirmació en cada procés.

\-v mostra tota la informació del procés.

\- t executa un sistema de fitxers concret, p.e.:  ...-t ntfs ...

\-c fa una comprovació dels blocs en el disc.

\-f obliga el xequeig.

\-y diu Sí (yes) a totes les preguntes.

### Fonts:

- [Viquipèdia](http://ca.wikipedia.org/wiki/Fsck)
- [Linux Man Page](http://linux.die.net/man/8/fsck)
- [Linux Fsck Command Examples](http://www.thegeekstuff.com/2012/08/fsck-command-examples/)
