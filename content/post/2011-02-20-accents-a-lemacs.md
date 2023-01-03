---
title: "Accents a l'Emacs"
date: "2011-02-20"
categories: 
  - "catala"
  - "emacs"
  - "org2blog"
---

Des de que he començat a usar Emacs, m'he trobat amb la dificultat d'escriure els accents. Al principi, si feia anar l'emacs des de consola amb: $ emacs -nw anava perfecte, però no era la solució!!! Al final, després de provar un munt de coses, he trobat que la culpa és que tinc instal·lat l'IBUS per escriure en xinès, i pel que sigui la codificació no acaba d'anar. La solució des de terminal era en mode gràfic: $ XMODIFIERS=@im=none emacs però no era qüestió d'anar obrint terminals per executar l'emacs per escriure amb accents.

Al final, gràcies a la pàgina [http://ur1.ca/3aql5](http://ur1.ca/3aql5) que resolvia el problema “<dead-acute> is undefined”

**LA SOLUCIÓ** definitiva: afegir a ~/.emacs la línia següent: (require 'iso-transl)

:)
