---
layout: post
title:  "Eliminar el compte de Copy"
date:   2016-02-08 16:13:38
categories: neteja
tags: núvol neteja
---
![Copy](http://www.screencastsonline.com/public_images/01-new/SCOM0403-summary-icon-100x100.png  "Copy")

Ja fa uns dies que el **Copy** m'avisa que deixarà de tenir suport. 

A la [seva pàgina](https://www.copy.com) podem llegir:
> Copy and CudaDrive services will be discontinued.
> We are announcing today that the Copy and CudaDrive services will be discontinued on May 1, 2016.

És una llàstima, ja que fins ara m'ha anat molt bé. Però el món digital ens obliga a estar preparats per a canvis, així que ara toca deixar-lo.

En la meva distro habitual (***Lubuntu***) cal treure la seva execució automàtica.
Els passos que he seguit són: 

> - desintal·lar
> - eliminar la carpeta on resideix el programa
> - una còpia de la carpeta de *Copy*

Així que ho he fet de la següent manera... Primer cal entrar a la seva carpeta:

    cd .copy/x86/
    
A dins cal executar la comanda:
    
    sudo ./CopyCmd overlay remove 

I elimino la carpeta on ho tenia instal·lat:

    rm -rf .copy/

Finalment deso la carpeta dels fitxers en un disc extern. 
I ara cal buscar un altre servei al núvol!

:+1:

