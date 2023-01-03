---
title: "Convertir un vcd a mpg"
date: "2014-01-27"
categories: 
  - "convertir"
  - "media"
  - "terminal"
---

Fa un temps que tenic algunes pel·lícules en format VCD. Amb el temps, ocupen molt d'espai, i els CDs físics solen deteriorar-se. Així que he decidit desar-los en format de video MPG. Per fer això podem usar la comanda **vcdxrip**. Res més senzill que inserir el VCD al lector de l'ordinador, i un cop inserit, usar la comanda:

vcdxrip -p --nofiles -C

un cop ha acabat, ens crea un arxiu **avseq01.mpg** i un altre **videocd.xml**. El primer és el video, i el segon tenim les dades de la conversió. Si volem podem treure el CD des de la mateixa terminal escrivint

eject

I ja tenim la còpia del nostre VCD.

Desitjo que sigui d'utilitat!

;-)
