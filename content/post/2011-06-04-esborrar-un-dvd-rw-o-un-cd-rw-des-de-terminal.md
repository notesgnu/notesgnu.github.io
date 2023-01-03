---
title: "Esborrar un DVD-RW o un CD-RW des de Terminal"
date: "2011-06-04"
categories: 
  - "eines"
  - "terminal"
---

![http://upload.wikimedia.org/wikipedia/commons/4/44/Edge-gnome-terminal.png](images/Edge-gnome-terminal.png)

Sempre he usat el K3B, brasero o d'altres entorns GUI per esborrar els meus regrabables. Però avui m'ha sorgit el problema que no hi havia manera d'esborrar-lo. Per sort els usuaris Gnu/Linux tenim la **terminal** que mai ens falla!

![](images/K3b_logo.png "K3B")

Així que he esborrat el DVD-RW amb dues senzilles comandes:

- la primera comanda és per demuntar el CD o DVD, en el meu cas quan es munta ho fa a /dev/sr0, a vegades pot tenir un altre nom /dev/cdrom /dev/XX…

umount /dev/sr0

- la segona comanda que cal escriure a la terminal és la que demana que esborri:

cdrecord dev=/dev/sr0 blank=fast

Cal fixar-se que fa referència al /dev/sr0 que he desmuntat, si cal ho hem de canviar per el que hem usat nosaltres amb la comanda anterior.

Un cop fet això, el DVD-RW que pensava que ja no aniria, perfecte! Ja va i he pogut tornar a enregistrar-hi de nou.

;)
