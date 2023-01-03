---
title: "Conectar-se a Identi-ca amb Emacs"
date: "2011-01-08"
categories: 
  - "emacs"
---

Després de portar dies buscant com usar un client d'Identica, al final m'he decidit per usar EMACS.

El primer que he fet ha estat descarregar [identica.el](http://blog.nethazard.net/u/1) des de la seva pàgina.

Un cop l'he descomprimit, ho he copiat dins de la carpeta /home/user/.emacs.d/

```
$ tar xvzf identica-mode.tar.gz
```

$ cd identica-mode/

$ cp identica-mode.el /home/~user/.emacs.d/

Després he hagut de crear / modificar el fitxer .emacs de configuració d'EMACS.

$ emacs .emacs

I he escrit el següent:

(add-to-list 'load-path "/home/user/.emacs.d/")
;;; Identi.ca mode
(require 'identica-mode)

La primera línia no la tenia en cap lloc comentada, però sense aquest em retornava l'error, ja que li hem d'especificar a l'EMACS on ha de carregar els modes. Si volem podem afegir-los a altres carpetes com ara ~/.emcas-extensions o d'altres que volguem!

_**COM USAR-LO:**_

Per començar, només cal: `M-x identica`.

I ens demanarà l'usuari i la contrasenya...

Si volem veure les imatges dels usuaris, cal premer "i".

Per veure les rèpliques `C-c C-r`

Per veure la linia temporal general `C-c C-a`

Per veure la linia temporal de les amistats (és la que hi ha per defecte)  `C-c C-f`

Per veure la línia temporal d'un usuari `C-c C-u`

Per veure la línia temporal d'un grup `C-c C-g`

Per veure la línia temporal d'una etiqueta `C-c C-t`

Refrescar el buffer cal premer “g”.

Per escriure, només cal premer `C-c C-s` i a continuació escriure el text, quan acabem premer RET. (Si volem podem veure'l si actualitzem la línia temporal prement "g").

Per enviar un missatge a un usuari, premem `C-c C-d` i al minibuffer haurem d'escriure el nom d'usuari, i a continuació el missatge.

Per repetir un missatge, premem `C-c <RET>`

Amb f4 acursa els enllaços a través del servei ur1.ca

He llegit moltes pàgines per poder fer-ho, i en especial si se'n sap poc, costa... les fonts són:

[http://blog.nethazard.net/identica-mode-for-emacs/](http://blog.nethazard.net/identica-mode-for-emacs/)

[http://crysol.org/es/node/1394](http://crysol.org/es/node/1394) pensat per fer-ho amb Twitter

El wiki d'EMACS:

[http://www.emacswiki.org/emacs/Identica-mode](http://www.emacswiki.org/emacs/Identica-mode)
