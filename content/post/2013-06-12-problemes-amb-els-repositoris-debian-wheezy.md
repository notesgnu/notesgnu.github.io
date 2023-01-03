---
title: "Problemes amb els repositoris Debian Wheezy"
date: "2013-06-12"
categories: 
  - "debian"
---

Porto uns dies que Debian Wheezy em donava problemes per actualitzar.

Resulta que en fer les actualitzacions em donava:

Release http://ftp.es.debian.org/debian/dists/testing/InRelease caducat (invàlid des de XdataX)

Així que he hagut de corregir les llistes del repositori, resulta que com havia actualitzat Whezzy, i havia passat de testing a definitiva, llavors, al no haver canviat els meus repositoris em donava l'error.

emacs /etc/apt/sources.list

La solució ha estat canviar on posa "testing" per "Whezzy". Després de fer el **update** i **upgrade** tot solucionat!

:-)
