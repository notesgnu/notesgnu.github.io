---
title: "Corrector de català mentre escrivim a l'Emacs"
date: "2011-07-24"
categories: 
  - "catala"
  - "emacs"
  - "org2blog"
---

 

![](images/800px-Diccionari_catal%C3%A0_valenci%C3%A0_balear.jpg "Diccionari")

Des de que uso Emacs que m'han anat sorgint dubtes, problemes i solucions referents a l'ús del català. El primer problema que vaig tenir era que no era capaç d'escriure en accents fins que ho [vaig solucionar.](http://croniqueslinux.wordpress.com/category/catala/) La segona cosa era com fer anar un corrector en català, i també ho vaig [trobar.](http://croniqueslinux.wordpress.com/2011/02/24/corrector-catala-per-emacs/)

Ara resulta que m'he trobat que volia usar el corrector al "vol", és a dir, com en altres programes que es va posant en roig les paraules mal escrites. La solució, usar el mode **flyspell** que depén del diccionari de l'ordinador. El mode **flyspell-mode** quan l'he volgut usar m'he trobat que no hem reconeixia el diccionari català, i això que el tenia instal·lat. Quan he fet un canvi de diccionari:

M-x ispell-change-dictionary

Llavors m'ha saltat un error: _Check that emacs is using \`ispell' and not other application such as \`aspell'. See the value of the variable \`ispell-program-name'._

Ho he arreglat afegint al .emacs:

(setq-default ispell-program-name "aspell")

I ara ja funciona!

Si volem tenir funcionant el **flyspell** per defecte en iniciar Emacs, cal que afegim a .emacs:

(setq-default flyspell-mode t)

Ara ja no tinc res a envejar a cap editor de textos dels habituals ;-)

A més a més….

Si voleu usar Emacs per programar podeu fer ús també del flyspell:

M-x flyspell-prog-mode

Amb això, farà la correcció dels comentaris, però no marcarà les del llenguatge de programació i les variables.

Si volem usar **flyspell** amb LaTeX, podem escriure dins del .emacs:

(add-hook 'LaTeX-mode-hook 'flyspell-mode)

Recordeu que cal tenir instal·lat els aspell (o de la llengua que vulguem el diccionari), si no ho tenim cal:

zypper in aspell-ca
apt-get install aspell-ca

fonts: [Wikiemacs](http://www.emacswiki.org/emacs/FlySpell) [Article a Crysol](http://crysol.org/es/node/610) [Ispell, flyspell y abbrev](http://www.blackhats.es/wordpress/?p=18) [Explicació de Javier Valcarce](http://www.javiervalcarce.eu/wiki/Emacs#Correcci.C3.B3n_ortogr.C3.A1fica_y_diccionario)
