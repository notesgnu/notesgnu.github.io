---
title: "Unir videos des de terminal"
date: "2012-09-21"
categories: 
  - "mencoder"
  - "org2blog"
  - "terminal"
---

Sovint acabo amb molts videos de la càmera, i no és qüestió de tenir un munt de bocins solts. Així que els podem unir en un de sol. Utilitzant la eina **mencoder**, des de la terminal podem unir dos o més videos en un de sol.

Obrint una terminal:

mencoder -oac copy -ovc copy -idx -o videofinal.avi part1.avi part2.avi :

o també podem:

mencoder -oac copy -ovc copy -idx -o videofinal.avi part\* 

i així de facil tenim un sol video! ;-)
