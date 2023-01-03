---
title: "Corrector catala per Emacs"
date: "2011-02-24"
categories: 
  - "emacs"
  - "org2blog"
---

Avui estava escrivint un text en Català i m'he trobat que tenia faltes d'ortografia. El motiu ha estat que estava usant un teclat americà i no em posava els accents.  
La solució:  
instal·lar el paquet de llengua catalana…  
$ sudo apt-get install aspell-ca  
i ara dins de l'emacs, quan tenim el text acabat podem activar-ho amb:  
M-x ispell-buffer  
quan acabem fem C-g per sortir…

perfecte! :)
