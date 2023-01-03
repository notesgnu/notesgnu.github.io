---
title: "Bad Character '�'"
date: "2016-01-13"
categories: 
  - "comandes"
  - "terminal"
---

Un arxiu que he llegit des de terminal m'ha donat un error de lectura:

\> bad character '�'

Mirant la codificació de l'arxiu amb la comanda ****file****, he vist que no té la codificació per a **UNIX**, així que a canviar-ho. Primer cal instal·lar ****dos2unix****:

sudo apt-get install dos2unix

i després a convertir-ho:

dos2unix -n arxiu.txt arxiu2.txt

i problema resolt!

;-)
