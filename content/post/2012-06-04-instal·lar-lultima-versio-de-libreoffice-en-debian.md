---
title: "Instal·lar l'última versió de Libreoffice en Debian"
date: "2012-06-04"
---

Últimament estic tenint algun problema amb el **Debian Testing** (amb gnome-shell) i el **LibreOffice** 3.4.x així que cercant per internet he llegit que més gent ha tingut problemes, i amb la nova versió s'ha corregit molts dels problemes.

Així, que no m'he pogut esperar, en especial per l'angoixa que produeix la constant congelació del gnome-shell, on només puc moure el ratolí. Molts diuen que es pot solucionar amb **Alt+F2** i escriure **r** (per fer un restart del gnome-shell), però moltes vegades tampoc funciona.

La manera de fer la instal·lació directament des dels paquets de [http://www.libreoffice.org/](http://www.libreoffice.org/ "http://www.libreoffice.org/") 1- baixar els paquets: _LibO\_x.x.x\_Linux\_x86\_install-deb\_en-US.tar.gz (el paquet base)_ _LibO\_x.x.x\_Linux\_x86\_langpack-deb\_ca.tar.gz (per la llengua en català!)_ _LibO\_x.x.x\_Linux\_x86\_helppack-deb\_ca.tar.gz (el paquet d'ajuda en català!)_

2 -desempaquetar-los i entrar en la carpeta "del paquet bases" que posa DEBS des de terminal amb un $ **cd ~/..../DEBS/**

3 - i ara cal instal·lar-ho amb: # **dpkg -i \*.deb** (cal fer-ho com a root, així es pot fer un su i després la comanda o directament un _$sudo dpkg -i \*.deb_)

4 - ara només cal seguir el pas anterior entrant a cada carpeta descomprimida i anant instal·lant el paquet de llengua i després el d'ajuda.

Si tot va bé, ja l'has de tenir instal·lat!

font: [http://es.libreoffice.org/asistencia/instalacion/linux/](http://es.libreoffice.org/asistencia/instalacion/linux/)
