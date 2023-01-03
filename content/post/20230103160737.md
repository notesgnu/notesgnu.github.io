---
title: "Exportar Wordpress a Markdown"
date: 2023-01-03
author: "notesgnu"
categories:  ["markdown"]
tags: ["hugo", "markdown"]
id: 20230103162652
---

Hi ha diverses eines que es poden usar, entre elles hi ha [wordpress-export-to-markdown](https://github.com/lonekorean/wordpress-export-to-markdown
). 

El primer que cal fer és instaŀlar-la.

## instaŀlar wordpress-export-to-markdown

Si seguim les instruccions, podem fer:

```
npx wordpress-export-to-markdown
```
Ens instaŀlar-rà els paquest necessari i ja la tindrem.

## Baixar còpia de seguretat del Wordpress
A continuació, baixem l'aplicació tot el contingut del Wordpress a Markdown. La trobem 

Allí, exportem:
- Els meus llocs → eines → exporta

triem:
- Export content → Exporta-ho tot

Un cop baixat, tenim un arxiu comprimit en zip  i a dins un document en xml.

## Conversió de Wordpress a Markdown
Ara ho posem tot dins de la carpeta de l'aplicatiu on l'exeutarem:

```
 npx wordpress-export-to-markdown --post-folders=false --prefix-date=true
```

ens van sortint les preguntes, ens demana el fitxer `xml`, he renombrat a `export.xml` per facilitar l'exportació.

Diem a tot *yes*, i comença l'exportació.

Ara ja tenim tots els articles en carpetes i amb la majoria de les fotos en carpetes d'imatges. Per desgràcia, no ha baixat totes les imatges.

I he aprofitat per repujar-les a aquest blog.

:+1: