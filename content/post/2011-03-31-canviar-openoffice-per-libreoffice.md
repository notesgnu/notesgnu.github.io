---
title: "Canviar Openoffice per Libreoffice"
date: "2011-03-31"
categories: 
  - "ofimatica"
  - "org2blog"
---

[![](images/Screenshot-01.png)](http://www.libreoffice.org/assets/resized_screenshots_avoid/Screenshot-01.png) Avui he decidit defugir de l'Openoffice i la política de la companyia oracle, ha estat una gran eina fins ara, però calia seguir fent el canvi. Així que he desinstal·lat l'openoffice i he instal·lat [Libreoffice](http://www.libreoffice.org/).

Ho he fet al portàtil on hi ha instal·lat un ubuntu.

A la ternimal he seguit aquests passos:

sudo apt-get purge "openoffice\*.\*"

sudo add-apt-repository ppa:libreoffice/ppa

sudo apt-get update

sudo apt-get install libreoffice libreoffice-gnome
libreoffice-l10n-ca libreoffice-l10n-common 
libreoffice-help-ca language-support-writing-ca

;)
