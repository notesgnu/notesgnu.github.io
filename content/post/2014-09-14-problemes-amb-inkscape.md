---
title: "Problemes amb Inkscape"
date: "2014-09-14"
categories: 
  - "error"
  - "inkscape"
---

![inksbug.png](images/wpid-inksbug.png)

Porto dos dies buscant la solució a un problema que em tenia desesperat. Dibuixant amb Inkscape, i quan copiava i després enganxava, de sobte començaven a saltar errors!

Cannot list directory /home/usuari/.uniconvertor:\[Errno 2\] No such file or directory: '/home/usuari/.uniconvertor'

problemes amb Rellegint la pàgina [Uniconverter fails on copying an svg selection](https://bugs.launchpad.net/inkscape/%2Bbug/1152396) he trobat la **solució**.

Sembla que és un error de programari… és a dir, un **Bitxo** o **Cuca** (Bug) :-D

Resulta que quan hi ha algun programa que capta el portaretalls (xclipboard), com per exemple el _jdownloader_, llavors saltent tota mena d'errors!!!

Així que de moment, haurem d'usar l'Inkscape sense cap programa que li faci destorb. I de moment, ja funciona!
