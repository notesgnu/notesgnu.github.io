---
title: "Apunts d'EMACS, part II"
date: "2011-03-07"
categories: 
  - "emacs"
  - "org2blog"
---

Avui vull apuntar quatre notes més sobre dreceres de teclat i comandes bàsiques per a l'Emacs. Ja vaig fer la [primera part](http://croniqueslinux.wordpress.com/2010/10/12/apunts-demacs-part-i/), on vaig apuntar com iniciar.

### obrir un arxiu

Per obrir un arxiu, només cal `C-x C-f` i escriure el nom de l'arxiu que tenim o que volem iniciar. Si el tenim a la carpeta de l'usuari, s'obrirà; i si no el tenim a la carpeta, en crearà un nou a la carpeta de l'usuari. Per defecte, sempre el cerca a la carpeta usuari. Si volem que el cerqui a una altra carpeta o el volem crear; llavors hem de posar davant de l'arxiu a _editar/crear_ tota la drecera:  

/Documents/arxiu.text 

### desar un arxiu

Podem desar automàticament fent `C-x C-s` i així desarem sobreescrivint el que acabem de canviar. Si volem desar-ne una còpia, llavors hem d'escriure `C-x C-w`.

### inserir un arxiu

Si el que volem es crear un arxiu a partir de varis que ja he escrit, només cal `C-x i` i ens afegirà a continuació el contingut de l'arxiu següent.

### canviar de buffer

Si estem treballant amb diferents arxius, i/o en diferents buffers, podem anar canviant `C-x b` (b=buffer), i amb les fletxes del teclat podem anar canviant entre els buffers.

### matar el buffer

Si volem matar el buffer, és a dir, tancar el buffer i seguir treballant amb **Emacs**, només cal `C-x k` (k=kill) i dir el buffer que volem tancar.

Recordo que si ens equivoquem en teclejar, només cal fer `C-g` i tema solucionat.

;)
