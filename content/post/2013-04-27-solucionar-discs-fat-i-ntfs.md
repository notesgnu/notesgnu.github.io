---
title: "Solucionar discs FAT i NTFS"
date: "2013-04-27"
categories: 
  - "terminal"
---

Ja he comentat l'ús del [FSCK](http://croniqueslinux.wordpress.com/2013/04/27/solucionar-discs-amb-fsck/) i ara volia comentar com fer-ho amb disc de tipus **FAT**.  
Com a eina imprescindible hi ha [testdisk](http://www.cgsecurity.org/wiki/TestDisk) que permet molts sistemes de fitxers, i realment es pot considerar la navalla suïssa!, gràficament tenim [gparted](http://gparted.sourceforge.net/) i [disks](http://en.wikipedia.org/wiki/GNOME_Disks) (Palimpsest Disk). Però una eina senzilla i molt semblant a **fsck** és **dosfsck**. Primer que res cal tenir instal·lat el paquet **dosfstools**:

sudo apt-get install dosfstools

### FAT:

Per poder dur-ho a terme, el primer és llistar les particions i discs, es pot fer de moltes maneres, la que faig anar és:

$ cat /proc/partitions

Un cop veiem la llista, ara cal desmontar-ho:

$ sudo umount /dev/sdXN

I ara com superusuari iniciem **dosfsck**, cal posar el número, per exemple sdf1:

$ sudo dosfsck -a -t /dev/sdXN 

### NTFS:

No és un sistema de fitxers massa ben suportat per GNU/Linux, però hi ha un bon munt d'eines…  
Si volem comprovar discs NTFS podem usar **ntfs-config**, per això ens cal tenir instal·lat:

sudo apt-get install ntfs-config

O també podem usar [scrounge-ntfs](http://thewalter.net/stef/software/scrounge/)

sudo apt-get install scrounge-ntfs

### Fonts:

- [How to repair a corrupted FAT32 file system](http://askubuntu.com/questions/147228/how-to-repair-a-corrupted-fat32-file-system)
- [Data Recovery with Scrounge NTFS](http://martinstutenglish.wordpress.com/2009/04/18/data-recovery-with-scrounge-ntfs/)
