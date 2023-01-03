---
title: "Instal·lar modes en Emacs 24"
date: "2013-04-05"
categories: 
  - "emacs"
---

Ja fa un temps que [Emacs](http://www.gnu.org/software/emacs/) va passar a la versió 24, i des del juny del 2012 que en podem gaudir de noves funcionalitats. Fins ara havia estat usant la versió anterior. Però avui m'he dedicat a provar la versió 24, exactament 24.3 que tenim des del passat 11 de març de 2013. ![http://upload.wikimedia.org/wikipedia/commons/0/08/EmacsIcon.svg](http://upload.wikimedia.org/wikipedia/commons/0/08/EmacsIcon.svg)

I una de les coses que he començat a fer és editar un document en Latex. Així que refent el document m'he trobat que no compilava. Habitualment uso el mode **AUCTeX**, però en obrir-lo en el nou Emacs24 m'he trobat que no funcionava.

Així que a cercar possibles solucions en la xarxa. I de sobte m'he enrecordat que **Emacs24** permet fer instal·lacions. Res més senzill que:

M-x package-install
>> prèmer tecla retorn!
auctex

I en breu ja tenim instal·lat el mode!

Si volem llistar els paquets:

M-x list-packages

I ara ja podem anar instal·lant els nous modes directament des del servidor d'**Emacs** que es troba a [http://elpa.gnu.org/](http://elpa.gnu.org/) i si volem podem fer un cop d'ull directament a la web per conèixer el repositori directament.

Per realitzar la instal·lació, podem posar-nos sobre un de la llista i clicar la tecla:

"i" per instal·lar,

"d" per suprimir,

"u" per desmarcar,

"r" per fer un refresc de la llista,

"x" per executar el que hem marcat...

A més a més, podem afegir altres repositoris, com ara el [marmalade](http://marmalade-repo.org/) o [melpa](http://melpa.milkbox.net), per afegir-lo res més senzill que incloure'l al nostre ~.emacs:

(require 'package)
(add-to-list 'package-archives 
 '("marmalade" . "http://marmalade-repo.org/packages/")
 '("melpa" . "http://melpa.milkbox.net/packages/"))
(package-initialize)

I ja està!

;-)

fonts:

- [http://www.gnu.org/software/emacs/](http://www.gnu.org/software/emacs/)
- [http://wikemacs.org/wiki/GNU\\\_Emacs\\\_24](http://wikemacs.org/wiki/GNU_Emacs_24)
- [http://wikemacs.org/wiki/Package.el](http://wikemacs.org/wiki/Package.el)
- [http://marmalade-repo.org/](http://marmalade-repo.org/)
