---
title: "Girar un video"
date: "2015-07-09"
categories: 
  - "mencoder"
  - "terminal"
  - "video"
---

Avui tenia una mica de temps, i remenant videos de fa uns mesos, m'he trobat amb un video gravat amb mòbil, i es veu girat a l'ordinador.

Així que remenant una mica, el **mencoder** novament em dóna un cop de mà. Escrivim a la terminal:

mencoder -vf rotate=1 -oac pcm -ovc lavc videosensegirar.mp4 -o videogirat.mp4

El que el fa girar és l'opció **rotate=1** que el gira 90º a la dreta. Si volem en l'altra direcció ho canviem per **rotate=2**

En poc temps ja tinc el video girat!

;-)
