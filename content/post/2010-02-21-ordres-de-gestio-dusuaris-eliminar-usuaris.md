---
title: "Ordres de gestió d'usuaris: Eliminar Usuaris"
date: "2010-02-21"
categories: 
  - "terminal"
---

[![](images/gnome-terminal.png "Gnome-terminal")](http://croniqueslinux.files.wordpress.com/2010/02/gnome-terminal.png)

_Quan volem crear, modificar, gestionar i eliminar usuaris tenim una série d'ordres que podem fer-ne ús, només cal recordar que ho hem de fer com a root. Així des de qualsevol distro haurem d'entrar com a root (ex: su) o usant $sudo.... en debian i derivats:_

# **eliminar usuaris:**

**#** **userdel \[opcions\] nom-d'usuari**

així per exemple podem elimnar l'usuari creat abans... (l'opció **\-r** elimina l'enllaç a la carpeta del _home_)

#**userdel -r norbux**

o també

$**sudo** **userdel -r norbux**
