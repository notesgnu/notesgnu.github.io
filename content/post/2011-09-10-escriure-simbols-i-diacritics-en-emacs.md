---
title: "Escriure símbols i diacrítics en Emacs"
date: "2011-09-10"
categories: 
  - "catala"
  - "emacs"
---

![http://www.princeton.edu/~chaol/theme/emacs-logo.png](images/emacs-logo.png) Sóc usuari novell d´Emacs, i cada cop m'agrada més. Quan vaig estar a la Xina em vaig comprar un netbook (Asus Eeepc) i només té teclat americà. El primer que vaig fer va ser posar-li Gnu/Linux (Ubuntu) i configurar-li la possibilitat del "compose", així puc escriure usant la tecla que he predifinit (Alt-right) per poder composar lletres. En el cas d´Emacs no m'anava la tecla compose, així que la ç o les lletres accentuades eren una mica complicades d'escriure en català amb el preuat Emacs.

Això ha estat així fins que he llegit l'article [Diacritics in Emacs](http://www.masteringemacs.org/articles/2010/10/13/diacritics-in-emacs/) de la pàgina [masteringemacs.org](http://www.masteringemacs.org). Així que he pres unes notes i he fet proves en Emacs que escric a continuació. Emacs té suport compert per Unicode, i també diferents mètodes d'entrada permetent que Emacs pugui treballar amb diverses llengües. A l'emacs tenim tres mètodes per inserir símbols i diacrítics: Unicode Code Points, Character Composition i Multilingual Text Input.

### Unicode Code Points:

Per usar aquest mètode fem C-x 8 RET i escrivim el codi hex o el nom, també podem teclejar TAB per llistar les possibles opcions. Així podem escriure:

⌨ fent C-x 8 RET KEYBOARD 
⌢ fent C-x 8 RET FROWN

### Character Composition:

Una altra manera d'escriure usada, en especial per diacrítics, és usar el sistema semblant a l'anterior: **C-x 8** Per exemple, per escriure ç fem C-x 8 , c i per escriure ó fem C-x 8 ' o Per llistar possibilitats tenim l'opció C-x 8 C-h i per llistar tots els caracters accentuats **C-x 8 ' C-h**

C-x 8 ' SPC   '
C-x 8 ' '     ´
C-x 8 ' A     Á
C-x 8 ' i     í
C-x 8 ' y     ý

### Multilingual Text Input.

Per activar el mode d'entrada en altres llengües amb emacs només cal activar-ho i desactivar-lo amb C-\\ o M-x toggle-input-method. A la barra inferior quedarà marcat el mètode que estem usant, per exemple el mode que uso per escriure en català és "latin-1-prefix" i queda a sota marcat

\-1>U:\*\*- :

Qua s'activa podem escriure els accents de forma habitual com ara:

é ho fem amb 'e
è ho fem amb \`e
ç ho fem amb ~c
' ho fem amb 'SPC

Per poder canviar entre diferents modes d'escriure podem fer-ho teclejant amb C-x RET C-\\ o M-x set-input-method. Així per exemple podem triar escriure en:

xinès: C-x RET C-\\ i triant chinese-py i ja podem escriure en xinès 你好!
japonès: C-x RET C-\\ i triant japanese i ja podem escriure ひらがな
àrab: C-x RET C-\\ i triant arabic i ja podem escriure ع ث ر ة

i una llarga llista de llengües amb caracters diferents…

Fins i tot podem usar per escriure diacrítics amb llenguatge Tex, C-x RET C-\\ i triant tex i ja podem escriure:

\\\`a dóna à
\\"o dóna ö
\\=a dóna ā
\\o  dóna ø 
\\ss dóna ß
\\d{a} dóna ạ 

o fins i tot símbols matemàtics:

\\sum dóna ∑
\\div dóna ÷
\\frac12 dóna ½  
\\gamma dóna γ

A més a més, tenim que podem usar altres formes d'entrades com IPA, sgml, i un llarg etc. Només cal C-x RET C-\\ i TAB per a que surti una llista llarga de possibilitats.

font: [Diacritics in Emacs](http://www.masteringemacs.org/articles/2010/10/13/diacritics-in-emacs/)
