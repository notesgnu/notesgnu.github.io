---
title: "Canviar el noms de fitxers amb <b>rename</b>"
date: "2012-10-06"
categories: 
  - "emacs"
  - "org2blog"
---

Algunes vegades necessito canviar el nom d'un fitxer o d'una carpeta, res més senzill que usant l'entorn gràfic i fent clic amb el botó dret sobre el fitxer (ho faig així amb el nautilus, o el pcmanfm, o el dolphin) o directament amb el fitxer eleccionat i prement \[F2\].

Però quan vull canviar molt fitxers de nom o d'extensió, llavors es fa molt lent. Hi ha eines gràfiques per fer-ho com [gprename](http://gprename.sourceforge.net/), [krename](http://www.krename.net/) o [pyrenamer](http://www.infinicode.org/code/pyrenamer/), però jo voldria compartir la que uso jo, des de terminal, la comanda **rename**.

Tenim la comanda de linux **mv** que ens pot fer servei, però aquest cop parlaré de la comanda **rename**. Està escrita en **perl** i això vol dir que usa les mateixes [expressions regulars de perl.](http://perlenespanol.com/tutoriales/expresiones_regulares/)

L'altre dia vaig fer unes carpetes comprimides en **zip** d'unes imatges, i després vaig pensar que si els convertia a **cbz** els podria visualitzar amb un visor de comics (comix o el propi okular o evince). Resulta que els fitxers **cbz** són **zip** amb extensió canviada, així que només calia canviar el nom de l'extensió.

### Canviar l'extensió dels fitxers

Així, res més senzill que usar **rename** per canviar l'extensió dels fitxers de \*.zip a \*.cbz he usat:

rename -v .zip .cbz \*.zip :

Si ens fixem veiem que he posat -v per anar veient tot el procés (-v verbose) després li dic que vull canviar .zip per .cbz i al final li dic que ho faci en els fitxers \*.zip (tots els que tenen l'extensió zip).

Si volguessim canviar un \*.JPG en majúscules en \*.jpg en minúscules, senzill:

rename -v .JPG .jpg \*.JPG :

### Canviar el nom dels fitxers

Ara us vull comentar la idea de canviar una part del nom o tot el nom del fitxer. Per exemple volem canviar el nom de varies fotos que hem fet amb la càmera, i que la càmera ha nombrat com arar IMG\_5121.JPG IMG\_5122.JPG IMG\_5123.JPG ….. i volem que es digui _fotografia\_5121.JPG_, etc…

Doncs res més senzill:

rename -v IMG fotografia IMG\* :

Així, buscarà tots els arxius començats per IMG (IMG\*) i canviarà _IMG_ per _fotografia_.

### Més informació

Podeu trobar més informació a:

man rename:

i en algunes pàgines de la web:  
[Algo de linux: Comando rename](http://enavas.blogspot.com.es/2009/11/el-shell-de-linux-comando-rename.html)  
[jmarior ens explica l'ús de rename](http://www.jmarior.net/como-renombrar-archivos-en-linux-comando-rename.htmla?storyid=296)  
[Soluciones productivas Libres: Renombrar archivos…](http://linux-productivo.blogspot.com.es/2010/08/renombrar-archivos-masiva-y-rapidamente.html)
