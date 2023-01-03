---
title: "Biombos a la terminal"
date: "2013-04-03"
categories: 
  - "terminal"
---

Ja fa dies que no escrivia res, he estat fent moltes coses, i llegint la revista [Linux Magazine](http://www.linux-magazine.es/issue/91) número 91 he trobat l'eina anomenada [Byobu](http://byobu.co/). Una eina molt interessant per treballar amb la terminal. Ja havia comentat [Screen](http://croniqueslinux.wordpress.com/2011/12/05/screen-una-eina-mes-per-la-terminal/) i també [Tmux](http://croniqueslinux.wordpress.com/2012/03/18/tmux-per-veure-la-terminal-duna-altra-manera/), i ara podriem dir que anem a trobar una evolució d'aquestes dues. Byōbu és una paraula japonesa que significa Biombo (Byō- parar + bu - vent), i serveix per fer separacions, crear i desfer espais ràpidament. Doncs així mateix treballa Byobu en la terminal, deixant tenir varies finestres, i la pantalla dividida. A més a més, permet deixar funcionant la Shell en tancar la terminal, i continuar treballant més tard. També permet executar una terminal remotament via ssh i continuar la feina des del client. I també és capaç de treballar dues persones alhora, en la mateixa finestra de byobu, des de dos ordinadors separats i conectats via ssh. A més a més, a la barra inferior ens informa de la distribució, l'ús del cpu, de ram, hora, data, i d'altres informacions interessants, com per exemple quan surt un número amb ! vol dir que tenim un nombre concret d'actualitzacions.

![http://byobu.co/img/byobu-top-right.png](images/byobu-top-right.png)

### instal·lació

Per instal·lar res més senzill que: Arch

pacman -Sy byobu

Debian, Mint, Ubuntu

apt-get install byobu

Fedora

yum install byobu

Gentoo

emerge byobu

En el cas de **Linkat** m'he baixat de la pàgina [https://launchpad.net/byobu/+download](https://launchpad.net/byobu/+download) el [tar.gz](https://launchpad.net/byobu/trunk/5.35/+download/byobu_5.35.orig.tar.gz) i després l'he descomprimit i compilat

tar -xzvf byobu\_5.35.orig.tar.gz
cd byobu-5.35/
./configure
make
make install

I ja el tenim funcionant!

### ús

Les tecles bàsiques són: F2 - crear una nova pestanya en la terminal. F3 - moure's a la pestanya anterior. F4 - moure's a la pestanya posterior. F5 - refresca l'estat. F6 - sortir, deixant funcionant Byobu en el fons, i quan tornem a executar Byobu a la terminal, el tenim com l'haviem deixat. F7 - mostra l'historial. F8 - reanomena la pestanya de la terminal. F9 - configurar el Byobu.

Shift + F2 - divideix la terminal horitzontalment Ctrl + F2 - divideix la terminal en vertical Shift + F3 - moure's a la pestanya anterior entre divisions. Shift + F4 - moure's a la pestanya posterior entre divisions. Shift + F5 - canvia entre les línies d'estat. Ctrl + F5 - Reconnecta ssh/gpg/dbus Ctrl + Shift + F5 - canvia el color de la barra inferior. Ctrl + F6 - surt de la partició. Shift + F1 - mostra l'ajuda de Byobu.

Nota: escrivint **exit** sortim de la pestanya A veure que us sembla ;-)
