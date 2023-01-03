---
title: "Sincronitzar gnote amb dropbox"
date: "2010-11-21"
categories: 
  - "fedora"
  - "programari"
  - "terminal"
  - "ubuntu"
---

Fins fa poc usava poc el Tomboy, o d'altres programes de notes com ara el GNOTE. Però fa poc vaig llegir un article de com sincronitzar-ho entre ordinadors a través del dropbox.

He seguit els passos que explicaven en "Usemos linux" [http://ur1.ca/2e9r3](http://ur1.ca/2e9r3), però NO m'ha funcionat... el problema era que no em reconeixia ~/.gnote l'havia de canviar per ~/.local/share/gnote

Així que al final ho he fet d'aquesta manera:

Crear una carpeta Gnote dins de la carpeta Dropbox, $ mkdir ~/Dropbox/gnote

Copiar les notes que tenim a dins del Dropbox. $ cp ~/.local/share/gnote/\* ~/Dropbox/gnote/

Esborrem la carpeta local del gnote. $ rm -r ~/.local/share/gnote/

Creem un enllaç simbòlic on desem les notes del gnote i vagi a cercar-les al /dropbox/gnote/. $  ln -s ~/Dropbox/gnote/ ~/.local/share/gnote

:)
