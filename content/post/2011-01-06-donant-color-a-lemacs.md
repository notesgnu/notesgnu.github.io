---
title: "Donant color a l'Emacs"
date: "2011-01-06"
categories: 
  - "emacs"
---

Avui he decidit donar-li una mica de color a l'Emacs... per això he instal·lat el paquet _emacs-goodies-el_ que conté el **color-theme**.

A la pàgina del _[color-theme tenim](http://www.nongnu.org/color-theme/)_ tenim els pasos a seguir per fer-ho.

El primer que he fet ha estat instal·lar el paquet:

$ sudo apt-get install emacs-goodies-el

Després he executat l'emacs, i amb **M-x color-theme-select** he triat el color que més m'ha agradat!

Si volem deixar predifinit el tema de color desitjat, llavors he d'escriure o editar el ~/.emacs i afegir:

;;; Colors per a l'Emacs (require 'color-theme) (eval-after-load "color-theme" '(progn (color-theme-initialize) (color-theme-hober)))

Si volem canviar el color... hem de substituir (color-theme-nom\_del\_tema\_triat).

;)
