---
title:  "Escanejar PDF i OCR"
date:   2020-05-21 
categories: ["ocr"] 
tags: ["pdf", "terminal", "ocr"]
---

El primer post des de fa temps és per escriure sobre entrepans i PDFs. ;-)

Sovint em passa que tinc molts PDFs escanejats de documents, i els voldria tenir a text. Remenant una mica, ja fa uns dies, vaig trobar una eina molt interessant: **pdfsanwich** tenim tota la informació a http://www.tobias-elze.de/pdfsandwich/

La part interessant, és que pot agafar un PDF i llegir-lo a través del tesseract i definint la llengua, podem escanejar la imatge del PDF i incrustrar-hi a dins el text usant OCR.

### instal·lem
Per fer la instal·lació en **Ubuntu** (i derivades), jo ho he fet amb 18.04 i 20.04, només cal:

```
sudo apt install pdfsanwich
```

també ens farà falta les llengues que necessitem:

```
sudo apt install tesseract-ocr-XXX
```

En el meu cas, he instal·lat cat (català), spa (espanyol), fra (francès) i epo (esperanto).

### ús
El que cal escriure és:

```
pdfsandwich -lang XXX document.pdf
```

El codi XXX cal dir la llengua que volem usar.

Després d'una estona, tindrem un segon PDF amb text seleccionable i copiable del PDF.

Si tenim un document escanejat a doble pàgina, és a dir, hi ha dues pàgines per pàgina, llavors podem indicar-ho:

```
pdfsandwich -lang cat -layout double document.pdf
```

Si voleu més opcions, podeu mirar la pàgina oficial de [pdfsanwich](http://www.tobias-elze.de/pdfsandwich/).

