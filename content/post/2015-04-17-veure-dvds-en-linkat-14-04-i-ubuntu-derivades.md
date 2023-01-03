---
title: "Veure DVDs en Linkat (14.04) i Ubuntu (derivades)"
date: "2015-04-17"
categories: 
  - "linkat"
  - "multimedia"
---

Ja porten uns dies que dues persones m'han preguntat el motiu pel qual no es veuen els DVDs en la **Linkat** 14.04, que és una derivada d'Ubuntu.

![](images/229px-DVD-Video_bottom-side.jpg)

Així que només cal anar a la pàgina oficial d'Ubuntu on parla dels [Formats Restringits](https://help.ubuntu.com/community/RestrictedFormats/PlayingDVDs), allí ens aconsella instal·lar els paquets **libdvdcss2** que en la LinkatEdu 14.04 és **libdvdread4**. En la [pàgina de la Linkat](http://linkat.xtec.cat/portal_linkat/wikilinkat/index.php/Reproduccio_DVD_Linkat_edu_12.04) també ho tenim ben documentat!

Per això anem a la terminal i escrivim:

sudo apt-get install libdvdread4

Un cop fet això, ara ens cal executar l'**Script**:

sudo /usr/share/doc/libdvdread4/install-css.sh

En un principi ja ha de funcionar!

Si veiem que no va, només cal reiniciar. I un cop fet això ja podem veure DVDs des de el VLC, per exemple.

;-)
