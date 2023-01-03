---
title: "Colors a Emacs"
date: "2014-08-11"
categories: 
  - "emacs"
---

![Paletaculori.gif](images/Paletaculori.gif)

Després d'un temps treballant amb **Emacs** van venint ganes de donar-li un aspecte més personal, és a dir, un toc de color!

Hi ha varies maneres de fer-ho. Per una part tenim l'opció de configuració del propi **Emacs**:

`M-x customize-face`

On podrem triar els colors de fons, tipus de lletra, colors varis i un gran etc. I ens queda desat.

A mi m'agrada fer-ho directament al meu `.emacs`.

Així que he escrit només un canvi de color de fons (_background_) i de lletra (_foreground_):

(set-foreground-color "white")
(set-background-color "black")

Per conèixer més colors podem trobar la pàgina [Colors Available to Emacs](http://raebear.net/comp/emacscolors.html) on ens diu els colors i com cercar-los. He fet la prova al **Ubuntu** i ho he trobat a `cat /etc/X11/rgb.txt`.

Si volem alguna cosa més bonica, podem usar un mode ja preparat a [Emacs Themes](http://emacsthemes.caisah.info/) on podrem remenar i veure el codi per _tunejar-nos_ l'****Emacs****.

I ara a fer proves! ;-)
