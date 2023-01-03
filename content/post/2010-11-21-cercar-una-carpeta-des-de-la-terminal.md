---
title: "Cercar una carpeta des de la terminal"
date: "2010-11-21"
categories: 
  - "terminal"
---

Usem la comanda FIND

$ find /on/busquem/ -type d -name NOMqueBusquem

si volem que ens reporti un document on surtin els resultats...

$ find **/on/busquem/** -type d -name **NOMqueBusquem** > trobats.txt
