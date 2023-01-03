---
title: "Trobant duplicats!"
date: "2012-01-11"
categories: 
  - "bash"
  - "terminal"
---

He de confesar que sofreixo una mica el síndrome de diògenes "digital", és a dir, sovint emmagatzemo molts arxius, i moltes vegades trobo que ja els tenia. Això m'ha fet que tingue més vegades de les desitjades el mateix document, en diferents carpetes o amb noms diferents. Hi ha una eina gràfica que va força bé anomenada [fslint](#http-www.pixelbeat.org-fslint). Però per poder a prendre, acostumo a intentar fer-ho des de la terminal. Així quue he trobat la comanda: [fdupes](http://premium.caribe.net/~adrian2/fdupes.html).

Per tenir-la instal·lada, només cal:  
`$ sudo apt-get install fdupes` (Per Debian, Ubuntu i derivats)  
o  
`$ sudo zypper in fdupes` (Per Linkat, Opensuse o derivats)  

Un con instal·lat ja podem fer-ne ús:

`$ fdupes -R -d /carpeta/on/ferlacerca`

Les fonts:  

- [Eliminar archivos duplicados](http://odiolasllaves.com.ar/blog/sebaminguez/eliminar-archivos-duplicados)
- [Fdupes. Buscando ficheros y directorios duplicados](http://linuxsan.wordpress.com/2008/04/25/fdupes-buscando-ficheros-y-directorios-duplicados/)
