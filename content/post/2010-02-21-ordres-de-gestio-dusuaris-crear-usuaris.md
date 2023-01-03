---
title: "Ordres de gestió d'usuaris: Crear Usuaris"
date: "2010-02-21"
categories: 
  - "terminal"
---

[![](images/gnome-terminal.png "Gnome-terminal")](http://croniqueslinux.files.wordpress.com/2010/02/gnome-terminal.png)

_Quan volem crear, modificar, gestionar i eliminar usuaris tenim una série d'ordres que podem fer-ne ús, només cal recordar que ho hem de fer com a root. Així des de qualsevol distro haurem d'entrar com a root (ex: su) o usant $sudo.... en debian i derivats:_

# **crear usuaris:**

**#** **useradd \[opcions\] nom-d'usuari**

Opcions que podem usar:

**\-g nomdelgrup** \[grup principal de l'usuari\]

**\-d /home/nomusuari** \[carpeta que volem asignar a l'usuari\] si no hi ha la carpeta li podem afegir **-m** seguidament perquè la cree.

**\-s /bin/bash** \[o un altre intèrpret si volem que siga diferent\]

exemple:

$**sudo** **useradd norbux**

o amb més opcions

**$****sudo useradd** \-g casa -d /home/norbux -m -s /bin/bash **norbux**

i només ens quedaria afegir-li una contrasenya...

**$sudo** **passwd norbux**

Gràficament podem executar: **ALT+F2** i escriure **users-admin**
