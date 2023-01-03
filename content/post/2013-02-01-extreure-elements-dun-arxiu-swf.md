---
title: "extreure elements d'un arxiu swf"
date: "2013-02-01"
categories: 
  - "audio"
  - "comandes"
  - "eines"
---

No m'agrada massa el flash ja que en no és un programari lliure, i no té massa bona implementació. Bé, la qüestió és que en un [swf](http://ca.wikipedia.org/wiki/SWF "swf") hi havia un audio que volia tenir per separat. També serveix per les imatges que surten, que pot ser volem recuperar-les d'un swf.

Un cop creat es fa difícil tornar a extreure el que s'ha incrustat...

bé, doncs he trobat una eina que ho permet, està dins d'un conjunt d'eines anomenades [SWFTOOLS](http://www.swftools.org/about.html "swftools"). Estan sota llicència GPL, i ens permeten fer un bon munt de coses.

### **El primer que cal fer és instal·lar-ho**

Podem provar de veure si el tenim als repositoris, mirant d'instal·lar-ho com sempre

- zypper in swftools (en linkat i opensuse)
- apt-get install swftools (en debian i derivats)

Com que no els he trobat, he passat a compilar-los des del que ofereix la pàgina oficial:

- _en abaixem el paquet amb:_ wget http://www.swftools.org/swftools-0.9.2.tar.gz
- _el descomprimim_: tar -zvxf swftools-0.9.2.tar.gz
- _entrem dins de la carpeta:_ cd swftools-0.9.2/
- el compilem:
    - ./configure --prefix=/usr/local
    - make
    - make install
    - _nota: si dóna problemes, cal instal·lar alguna dependència ( install libgif-dev xpdf libfreetype6 libfreetype6-dev libjpeg62 libjpeg8 libjpeg8-dev)_

Jo he fet la prova en la Linkat 11.4 i en un Debian (Whezzy i Squeeze) i perfecte!

(font: [http://maurizio-franco.blogspot.com.es/2012/01/installing-swftools-on-debianubuntu.html](http://maurizio-franco.blogspot.com.es/2012/01/installing-swftools-on-debianubuntu.html))

Ara ja el tenim per ser usat.... com veiem a la pàgina oficial, podem fer un bon munt de coses, des de crear swf a partir de pdf, així com extreure-ho després.

El que jo vull explicar és

### **com extreure:**

una de les aplicacions que tenim ara instal·lades és **swfextract**

Per usar, res més senzill que:

**$ swfextract \[el què volem\] arxiuorigen.swf -o arxiusortida.extensió**

exemple:

**$ swfextract nom.swf** i ens diu el que conté per exemple, jo he fet una prova amb un que tenia i m'ha donat aquesta informació: \[-i\] 87 Shapes: ID(s) 3, 7, 15, 17-94, 96, 98, 100, 102-104 \[-i\] 3 MovieClips: ID(s) 6, 8, 13 \[-j\] 5 JPEGs: ID(s) 16, 95, 97, 99, 101 **\[-s\] 1 Sound: ID(s) 14** \[-F\] 3 Fonts: ID(s) 1, 4, 9 \[-M\] 3 Embedded MP3s: ID(s) 6, 8, 13 \[-f\] 1 Frame: ID(s) 0 \[-m\] 1 **MP3** Soundstream

això vol dir que si vull extreure audio, res més senzill que: **$ swfextract \-s 14  arxiuorigen.swf -o arxiusortida.mp3**

on -s vol dir so i el número fa referència al número de la info que m'ha donat!

Com veieu aquesta eina ens dóna molt de joc!

;-)
